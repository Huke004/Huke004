---
name: word-erstellen-formatieren
description: Word-Dokumente (.docx) erstellen und bearbeiten – Formatvorlagen, Überschriften, Tabellen, Bilder, Kopf-/Fußzeilen, Seitenzahlen, Inhaltsverzeichnis, Deckblatt, Querformat. Nutzen, wenn ein Word-Dokument produziert, ergänzt oder umformatiert werden soll.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Word-Dokumente erstellen und formatieren

## Zweck

Professionelle .docx-Dateien erzeugen, die man einem Kunden, einer Bank oder
einem Gericht vorlegen kann – mit korrekten Formatvorlagen, Seitenzahlen,
Inhaltsverzeichnis und Corporate Design.

## Grundregeln (gelten immer)

Diese Datei ist eigenständig nutzbar; sie setzt keine andere Datei voraus.
Die folgenden Regeln gelten für jede Aufgabe.

**Auftrag klären.** Bei Bewertungsaufgaben stehen vor jeder Zahl vier Angaben
fest: Bewertungsobjekt, Wertermittlungsstichtag, Wertbegriff (Verkehrswert,
Beleihungswert, Kaufpreisindikation) und Zweck. Fehlt mehr als eine davon,
gebündelt in einer Nachricht nachfragen statt zu raten.

**Zahlen kommen aus Quellen, nicht aus dem Gedächtnis.** Bodenrichtwerte,
Liegenschaftszinssätze, Normalherstellungskosten, Indexreihen, Mietspiegel,
Steuersätze und Rechtsstände werden recherchiert oder vom Nutzer geliefert.
Jede Zahl trägt Quelle und Stand, etwa `420 €/m², Stand 01.01.2026,
Gutachterausschuss <Ort>`. Zuständig sind in Deutschland die
Gutachterausschüsse (Bodenrichtwerte, Liegenschaftszinssätze, Sachwert- und
Vergleichsfaktoren, Kaufpreissammlung, Grundstücksmarktbericht), das
Statistische Bundesamt (Baupreis- und Verbraucherpreisindex), die Gemeinde
(Mietspiegel, Bauleitplanung, Baulasten) und das Grundbuchamt.

**Keine erfundenen Fakten.** Paragraphen, Urteile, Aktenzeichen, Normen und
Marktdaten werden nie konstruiert. Was unsicher ist, wird als unsicher
benannt: „ist beim … abzufragen". Angebotspreise aus Immobilienportalen sind
keine Kaufpreise und nie ein Vergleichspreis.

**Annahmen kennzeichnen.** Ein eingesetzter Wert ohne Quelle ist eine Annahme
und wird als solche markiert – auch wenn er üblich ist. Jede Analyse endet mit
einem Block „Annahmen und offene Punkte" samt fehlender Unterlagen.

**Rechenweg zeigen und prüfen.** Formel, Eingangsgrößen mit Quelle,
Zwischenergebnisse. Zinssätze als Dezimalzahl einsetzen (0,038 statt 3,8),
Einheiten mitführen, erst am Ende runden. Vor der Ausgabe einmal unabhängig
nachrechnen und gegen mindestens zwei Marktkennzahlen plausibilisieren
(€/m², Faktor, Bruttoanfangsrendite, Bodenwertanteil). Bei kritischen
Eingangsgrößen eine Sensitivität ausweisen statt eines Scheinpräzisen Werts.

**Personendaten sparsam.** Nur verarbeiten, was die Aufgabe braucht; Mieter
und Interessenten pseudonymisieren; besondere Kategorien nach Art. 9 DSGVO
(u. a. Gesundheit, Religion, Herkunft) gehören nie in Objektunterlagen. Keine
automatisierte Entscheidung über Personen und keine Rangfolge von Bewerbern.
Nach außen gehende KI-Texte im Prozess als KI-Entwurf kennzeichnen.

**Freigabe durch Menschen.** Der Agent liefert Entwurf und Zuarbeit, nicht die
Verantwortung. Menschliche Freigabe ist erforderlich bei Wertaussagen
gegenüber Dritten (Bank, Gericht, Finanzamt, Erbengemeinschaft), bei
rechtsverbindlichen Texten und Fristsachen, bei steuerlichen Gestaltungen und
bei allem, was veröffentlicht wird. Kein Dokument mit Unterschriftszeile,
Siegelfeld oder Sachverständigenformel; keine vorgetäuschte Berufs-
qualifikation. Fristen werden benannt mit dem Hinweis, dass ihre Wahrung nicht
beim Agenten liegt.

**Sprache und Format.** Deutsch, sachlich, ohne Werbefloskeln. Zahlen im
deutschen Format (1.234.567,89 €, 142,5 m²), Datum TT.MM.JJJJ. Verkehrswerte
auf volle 1.000 € runden, bei kleinen Objekten auf 5.000 €, und die Rundung
benennen.

## Wann anwenden

- Gutachten, Berichte, Exposés, Anschreiben, Protokolle als Word-Datei
- Bestehende Dokumente ergänzen oder umformatieren
- Kundenvorlage befüllen

**Nicht anwenden bei:** Serienbrief und Platzhalter-Vorlagen – dafür eignet
sich docxtpl mit Jinja2-Platzhaltern besser als python-docx.
Reinen Textentwürfen ohne Dateiwunsch → einfach als Text antworten.

## Goldene Regel

> **Vorlage vor Code.** Existiert eine Kundenvorlage (.docx/.dotx), wird sie
> geöffnet und befüllt – nicht ein neues Dokument gebaut und optisch
> nachgeahmt. Nur so stimmen Schriften, Farben, Abstände, Kopfzeile und
> Nummerierung.

```python
from docx import Document
doc = Document("firmenvorlage.dotx")   # erbt alle Stile
```

Ohne Vorlage: `Document()` und die Basisstile anpassen (siehe unten).

## Vorgehen

### 1. Struktur zuerst

Gliederung festlegen, dann Inhalte, dann Feinformat. Überschriften **immer
über Formatvorlagen**, nie über manuelles Fettsetzen – sonst funktioniert kein
Inhaltsverzeichnis und keine Navigation.

```python
doc.add_heading("Verkehrswertermittlung", level=0)   # Titel
doc.add_heading("1  Auftrag und Zweck", level=1)
doc.add_heading("1.1  Bewertungsobjekt", level=2)
doc.add_paragraph("Das Bewertungsobjekt liegt …")
```

Bei deutschsprachigen Vorlagen heißen die Stile oft `Überschrift 1` statt
`Heading 1`. Robust:

```python
def heading(doc, text, level):
    for name in (f"Heading {level}", f"Überschrift {level}"):
        if name in [s.name for s in doc.styles]:
            p = doc.add_paragraph(text, style=name)
            return p
    return doc.add_heading(text, level=level)
```

### 2. Basisformat setzen (nur ohne Vorlage)

```python
from docx.shared import Pt, Cm, RGBColor
from docx.enum.text import WD_ALIGN_PARAGRAPH

normal = doc.styles["Normal"]
normal.font.name = "Calibri"
normal.font.size = Pt(11)
pf = normal.paragraph_format
pf.space_after = Pt(6)
pf.line_spacing = 1.15

for section in doc.sections:
    section.top_margin = Cm(2.5)
    section.bottom_margin = Cm(2.0)
    section.left_margin = Cm(2.5)
    section.right_margin = Cm(2.0)
```

### 3. Tabellen

```python
t = doc.add_table(rows=1, cols=3)
t.style = "Table Grid"          # bzw. "Tabellenraster" / Vorlagenstil
hdr = t.rows[0].cells
for cell, text in zip(hdr, ("Position", "Fläche m²", "Wert €")):
    cell.text = text
    cell.paragraphs[0].runs[0].font.bold = True

for pos, flaeche, wert in daten:
    r = t.add_row().cells
    r[0].text = pos
    r[1].text = f"{flaeche:,.1f}".replace(",", "X").replace(".", ",").replace("X", ".")
    r[2].text = f"{wert:,.0f} €".replace(",", ".")
    for c in (r[1], r[2]):
        c.paragraphs[0].alignment = WD_ALIGN_PARAGRAPH.RIGHT
```

Kopfzeile auf jeder Seite wiederholen (nur über XML):

```python
from docx.oxml.ns import qn
from docx.oxml import OxmlElement

tr = t.rows[0]._tr
trPr = tr.get_or_add_trPr()
tblHeader = OxmlElement("w:tblHeader")
tblHeader.set(qn("w:val"), "true")
trPr.append(tblHeader)
```

Spaltenbreiten müssen in **jeder Zelle** gesetzt werden, sonst ignoriert Word sie:

```python
for row in t.rows:
    for cell, w in zip(row.cells, (Cm(8), Cm(3), Cm(4))):
        cell.width = w
```

### 4. Bilder

```python
doc.add_picture("objekt_ansicht.jpg", width=Cm(15))
cap = doc.add_paragraph("Abb. 1: Straßenansicht, aufgenommen am 14.08.2026")
cap.style = doc.styles["Caption"] if "Caption" in [s.name for s in doc.styles] else cap.style
cap.alignment = WD_ALIGN_PARAGRAPH.CENTER
```

Immer nur `width` **oder** `height` setzen – sonst wird das Bild verzerrt.
Bildrechte vor der Verwendung klären; Personen und Kennzeichen unkenntlich machen.

### 5. Kopf-/Fußzeile mit Seitenzahl „Seite X von Y"

Seitenzahlen sind Word-Feldfunktionen und müssen als XML eingefügt werden:

```python
from docx.oxml.ns import qn
from docx.oxml import OxmlElement

def add_field(paragraph, instr):
    run = paragraph.add_run()
    for typ, text in (("begin", None), ("instrText", instr), ("end", None)):
        el = OxmlElement(f"w:fld{'Char' if typ != 'instrText' else ''}"
                         if typ != "instrText" else "w:instrText")
        if typ == "instrText":
            el.set(qn("xml:space"), "preserve")
            el.text = text
        else:
            el.set(qn("w:fldCharType"), typ)
        run._r.append(el)

footer = doc.sections[0].footer
p = footer.paragraphs[0]
p.alignment = WD_ALIGN_PARAGRAPH.CENTER
p.add_run("Seite ")
add_field(p, "PAGE")
p.add_run(" von ")
add_field(p, "NUMPAGES")
```

Kopfzeile mit Aktenzeichen und Stichtag:

```python
h = doc.sections[0].header.paragraphs[0]
h.text = "Verkehrswertermittlung · Az. 2026-0142 · Stichtag 01.09.2026"
```

### 6. Inhaltsverzeichnis

Ein TOC-Feld wird eingefügt, aber erst von Word beim Öffnen gefüllt:

```python
p = doc.add_paragraph()
add_field(p, r'TOC \o "1-3" \h \z \u')
```

Damit der Nutzer nicht überrascht ist: **Hinweis mitgeben**, dass das
Verzeichnis in Word mit `Strg+A`, `F9` aktualisiert wird. Alternativ das
Verzeichnis statisch aus den Überschriften erzeugen (ohne Seitenzahlen) oder
das Dokument einmal durch LibreOffice laufen lassen:

```bash
soffice --headless --convert-to docx:"MS Word 2007 XML" bericht.docx
```

### 7. Seitenumbruch, Abschnitt, Querformat

```python
from docx.enum.section import WD_SECTION, WD_ORIENT
from docx.enum.text import WD_BREAK

doc.paragraphs[-1].runs[-1].add_break(WD_BREAK.PAGE)

s = doc.add_section(WD_SECTION.NEW_PAGE)
s.orientation = WD_ORIENT.LANDSCAPE
s.page_width, s.page_height = s.page_height, s.page_width   # beides tauschen!
```

### 8. Bestehendes Dokument gezielt ändern

```python
def replace_in_paragraph(p, old, new):
    if old not in p.text:
        return
    for run in p.runs:                     # zuerst runweise: Format bleibt
        if old in run.text:
            run.text = run.text.replace(old, new)
            return
    p.runs[0].text = p.text.replace(old, new)   # Fallback: Format geht verloren
    for r in p.runs[1:]:
        r.text = ""
```

Auch Tabellen, Kopf- und Fußzeilen durchlaufen – sonst bleiben Platzhalter stehen.

## Regeln

- **Nie das Original überschreiben.** Neue Datei mit sprechendem Namen:
  `<Vorgang>_<Dokumentart>_<JJJJ-MM-TT>.docx`
- Formatvorlagen statt Direktformatierung; direkte Formatierung nur für
  einzelne Hervorhebungen.
- Deutsche Zahlenformatierung im Text: `1.234.567,89 €`, `142,5 m²`.
- Keine leeren Absätze zur Abstandserzeugung – `space_after` verwenden.
- Nach dem Erzeugen die Datei **wieder öffnen und stichprobenartig prüfen**
  (Absatzzahl, Tabellen, Platzhalter, Überschriftenhierarchie).
- Bei Gutachten und Berichten: Aktenzeichen, Stichtag und Seitenzahl in
  Kopf-/Fußzeile; Vertraulichkeitsvermerk, falls vereinbart.

## Ausgabeformat

Fertige .docx-Datei plus eine Zeile, was sie enthält, plus – falls ein
TOC-Feld gesetzt wurde – der Hinweis zur Aktualisierung.

## Qualitätskontrolle

- [ ] Vorlage verwendet, falls vorhanden
- [ ] Überschriften über Formatvorlagen, Hierarchie lückenlos
- [ ] Alle Platzhalter ersetzt (auch in Tabellen, Kopf-/Fußzeilen)
- [ ] Seitenzahlen und Kopfzeile gesetzt
- [ ] Tabellen: Kopfzeile wiederholt, Spaltenbreiten in allen Zellen
- [ ] Bilder unverzerrt, mit Bildunterschrift
- [ ] Datei nach dem Schreiben erneut geöffnet und geprüft
- [ ] Zahlen im deutschen Format

## Grenzen

python-docx kann keine Seitenzahlen berechnen, keine TOC-Seitenzahlen füllen
und kein PDF erzeugen. Für PDF: Konvertierung über LibreOffice oder Word.
Komplexe Layouts (mehrspaltig mit Textfluss, Randnotizen) sind besser über
eine vorbereitete Vorlage zu lösen.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
