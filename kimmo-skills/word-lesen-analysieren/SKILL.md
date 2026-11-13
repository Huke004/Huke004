---
name: word-lesen-analysieren
description: Word-Dateien (.docx, .dotx) auslesen und analysieren – Text, Tabellen, Kopf-/Fußzeilen, Formatvorlagen, Kommentare, Änderungsverfolgung, eingebettete Bilder und Metadaten. Nutzen, wenn ein Word-Dokument ausgewertet, verglichen, zusammengefasst oder in Daten überführt werden soll.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Word-Dateien lesen und analysieren

## Zweck

Ein .docx ist ein ZIP-Archiv mit XML-Dateien. Wer das weiß, kommt an alles
heran – auch an das, was normale Bibliotheken überspringen: Kommentare,
Änderungsverfolgung, Kopf- und Fußzeilen, Textfelder, Fußnoten. Dieser Skill
beschreibt, wie ein Dokument vollständig erfasst wird.

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

- „Fasse dieses Word-Dokument zusammen"
- „Was steht in der Tabelle auf Seite 3?"
- „Vergleiche diese beiden Vertragsfassungen"
- „Zieh die Objektdaten aus diesem Gutachten"
- Vorlagen (.dotx) analysieren, um sie zu befüllen

## Aufbau einer .docx

```
document.docx (ZIP)
├── [Content_Types].xml
├── docProps/core.xml          ← Titel, Autor, Erstell-/Änderungsdatum
├── docProps/app.xml           ← Seiten-, Wort-, Zeichenzahl
└── word/
    ├── document.xml           ← Haupttext
    ├── styles.xml             ← Formatvorlagen
    ├── numbering.xml          ← Listen
    ├── settings.xml           ← u. a. rsid, Änderungsverfolgung an/aus
    ├── header1.xml … footer3.xml
    ├── footnotes.xml, endnotes.xml
    ├── comments.xml           ← Kommentare
    └── media/                 ← eingebettete Bilder
```

**Wichtig:** `python-docx` liest standardmäßig **nicht** Kommentare,
Änderungsverfolgung, Textfelder und teilweise nicht Kopf-/Fußzeilen-Tabellen.
Für diese Inhalte direkt ins XML gehen.

## Vorgehen

### 1. Überblick verschaffen

```python
from docx import Document
doc = Document("gutachten.docx")

print(len(doc.paragraphs), "Absätze,", len(doc.tables), "Tabellen")
print(doc.core_properties.title, doc.core_properties.author,
      doc.core_properties.modified)

# Gliederung über Überschriften-Formatvorlagen
for p in doc.paragraphs:
    if p.style.name.startswith(("Heading", "Überschrift")):
        print(p.style.name, "|", p.text)
```

### 2. Text in Dokumentreihenfolge lesen

`doc.paragraphs` und `doc.tables` sind zwei getrennte Listen – die
Reihenfolge im Dokument geht dabei verloren. Für korrekte Reihenfolge über
den Body-XML-Baum iterieren:

```python
from docx.document import Document as _Doc
from docx.table import Table, _Cell
from docx.text.paragraph import Paragraph
from docx.oxml.table import CT_Tbl
from docx.oxml.text.paragraph import CT_P

def iter_block_items(parent):
    if isinstance(parent, _Doc):
        parent_elm = parent.element.body
    elif isinstance(parent, _Cell):
        parent_elm = parent._tc
    else:
        raise ValueError(type(parent))
    for child in parent_elm.iterchildren():
        if isinstance(child, CT_P):
            yield Paragraph(child, parent)
        elif isinstance(child, CT_Tbl):
            yield Table(child, parent)

for block in iter_block_items(doc):
    if isinstance(block, Paragraph):
        if block.text.strip():
            print(block.style.name, ":", block.text)
    else:
        for row in block.rows:
            print(" | ".join(c.text.strip() for c in row.cells))
```

### 3. Tabellen sauber auslesen

```python
import pandas as pd

def table_to_df(table):
    rows = [[c.text.strip() for c in r.cells] for r in table.rows]
    return pd.DataFrame(rows[1:], columns=rows[0]) if len(rows) > 1 else pd.DataFrame(rows)
```

Fallstricke:

- **Verbundene Zellen** erscheinen mehrfach mit gleichem Inhalt – vor der
  Auswertung deduplizieren
- Zahlen kommen als Text mit Tausenderpunkt und Komma:
  `float(t.replace(".", "").replace(",", "."))` – aber nur, wenn das Format
  wirklich deutsch ist
- Zeilenumbrüche in Zellen (`\n`) beim Zusammenführen beachten

### 4. Kopf-/Fußzeilen, Fußnoten, Kommentare

```python
for section in doc.sections:
    for part in (section.header, section.first_page_header,
                 section.even_page_header, section.footer):
        for p in part.paragraphs:
            if p.text.strip():
                print(p.text)
```

Kommentare und Fußnoten über das XML:

```python
import zipfile
from lxml import etree

NS = {"w": "http://schemas.openxmlformats.org/wordprocessingml/2006/main"}

with zipfile.ZipFile("gutachten.docx") as z:
    for name in ("word/comments.xml", "word/footnotes.xml"):
        if name in z.namelist():
            tree = etree.fromstring(z.read(name))
            for node in tree.iter(f"{{{NS['w']}}}p"):
                text = "".join(t.text or "" for t in node.iter(f"{{{NS['w']}}}t"))
                if text.strip():
                    print(name, "->", text)
```

### 5. Änderungsverfolgung erkennen

```python
with zipfile.ZipFile("vertrag.docx") as z:
    xml = z.read("word/document.xml").decode("utf-8")
ins = xml.count("<w:ins ")     # Einfügungen
dele = xml.count("<w:del ")    # Löschungen
print(f"{ins} Einfügungen, {dele} Löschungen offen")
```

Sind Änderungen offen, **niemals stillschweigend weiterarbeiten** – erst
melden, dann klären, ob mit angenommenen oder abgelehnten Änderungen
gearbeitet werden soll.

### 6. Formatvorlagen und Vorlagenanalyse (.dotx)

```python
for s in doc.styles:
    print(s.type, "|", s.name, "|", "builtin" if s.builtin else "custom")
```

Vor dem Befüllen einer Kundenvorlage immer erst die vorhandenen Stile
inventarisieren – eigene Formatierung ist der häufigste Grund, warum ein
generiertes Dokument „nicht nach uns aussieht".

### 7. Zwei Fassungen vergleichen

```python
import difflib
a = [p.text for p in Document("v1.docx").paragraphs if p.text.strip()]
b = [p.text for p in Document("v2.docx").paragraphs if p.text.strip()]
for line in difflib.unified_diff(a, b, "v1", "v2", lineterm="", n=1):
    print(line)
```

Für Verträge zusätzlich absatzweise vergleichen und **jede inhaltliche
Änderung einzeln benennen** – ein Diff ist kein Ergebnis, die Einordnung ist es.

## Regeln

- Bevor Inhalte zusammengefasst werden: prüfen, ob Kopf-/Fußzeilen, Fußnoten
  oder Kommentare relevante Angaben enthalten (in Gutachten fast immer:
  Aktenzeichen, Stichtag, Seitenzahl, Vertraulichkeitsvermerk).
- Bei Verträgen und Gutachten **nie paraphrasieren, wo es auf den Wortlaut
  ankommt** – zitieren mit Fundstelle (Abschnitt, Absatz).
- Zahlen aus Tabellen nachrechnen, nicht nur ablesen (siehe `qualitaetssicherung`).
- Passwortgeschützte oder beschädigte Dateien nicht „reparieren", sondern melden.
- Bei Dokumenten mit Personendaten: nur übernehmen, was die Aufgabe braucht.

## Ausgabeformat

Bei Analyseaufträgen:

```
## Dokumentprofil
Titel · Autor · zuletzt geändert · Seiten/Wörter · Änderungsverfolgung: ja/nein · Kommentare: n

## Gliederung
(Überschriftenbaum)

## Kerninhalte
(je Abschnitt 1–3 Sätze)

## Tabellen
(je Tabelle: Zweck, Zeilen/Spalten, auffällige Werte)

## Auffälligkeiten
- offene Änderungen, Widersprüche, Platzhalter, fehlende Angaben
```

## Qualitätskontrolle

- [ ] Text in Dokumentreihenfolge gelesen (Absätze und Tabellen zusammengeführt)
- [ ] Kopf-/Fußzeilen, Fußnoten, Kommentare geprüft
- [ ] Änderungsverfolgung geprüft und ggf. gemeldet
- [ ] Verbundene Zellen beim Tabellenauslesen berücksichtigt
- [ ] Zahlen nachgerechnet
- [ ] Zitate mit Fundstelle

## Grenzen

Kein Seitenumbruch-genauer Zugriff: „Seite 3" ist in .docx nicht zuverlässig
bestimmbar, da die Paginierung erst beim Rendern entsteht. Bei Seitenbezug
nachfragen oder über Überschriften referenzieren. Für .doc (Altformat) vorher
konvertieren (z. B. LibreOffice `--convert-to docx`).

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
