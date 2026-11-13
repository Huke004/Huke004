---
name: word-vorlagen-serienbrief
description: Word-Vorlagen mit Platzhaltern befüllen und Serienbriefe erzeugen – docxtpl/Jinja2, Schleifen über Tabellenzeilen, bedingte Absätze, Massenerstellung aus CSV/Excel. Nutzen bei Vorlage, Template, Platzhalter, Serienbrief, Massenerstellung von Dokumenten.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Word-Vorlagen und Serienbriefe

## Zweck

Wiederkehrende Dokumente – Gutachtenmäntel, Maklerverträge,
Besichtigungsbestätigungen, Absagen, Mieterhöhungen, Übergabeprotokolle –
werden nicht jedes Mal neu geschrieben, sondern aus einer Vorlage befüllt.
Das ist schneller, konsistenter und revisionssicher.

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

- Es existiert eine Vorlage mit Platzhaltern
- Ein Dokument soll für viele Empfänger/Objekte erzeugt werden
- Standarddokumente sollen als Vorlage angelegt werden

## Werkzeugwahl

| Fall | Werkzeug |
|---|---|
| Vorlage mit Platzhaltern, Schleifen, Bedingungen | **docxtpl** (Jinja2 in Word) – erste Wahl |
| Einfacher Text-Ersatz in bestehendem Dokument | python-docx, runweise ersetzen (Code unten) |
| Dokument komplett neu aufbauen | python-docx |
| Word-eigener Seriendruck (MERGEFIELD) | nur wenn der Kunde es so verlangt; sonst zu unflexibel |

Der einfache Text-Ersatz mit python-docx sieht so aus – runweise, damit die
Formatierung erhalten bleibt:

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

Dabei auch Tabellenzellen sowie Kopf- und Fußzeilen durchlaufen – sonst
bleiben dort Platzhalter stehen.

## Vorgehen mit docxtpl

### 1. Vorlage anlegen

In Word ein Dokument mit dem Zielformat gestalten und Platzhalter in
Jinja2-Syntax direkt in den Text schreiben:

```
{{ anrede }} {{ nachname }},

für das Objekt {{ objekt.strasse }} in {{ objekt.plz }} {{ objekt.ort }}
haben wir zum Stichtag {{ stichtag }} einen Verkehrswert von
{{ wert }} € ermittelt.
```

**Der wichtigste Praxistipp:** Word zerlegt Text beim Tippen in „Runs".
Schreibt man `{{ wert }}` mit zwischenzeitlicher Rechtschreibkorrektur oder
Formatwechsel, wird daraus im XML `{{ we` + `rt }}` und docxtpl findet den
Platzhalter nicht. Abhilfe: den Platzhalter in einem Rutsch tippen, oder
außerhalb schreiben und als **unformatierten Text** einfügen.

### 2. Schleifen über Tabellenzeilen

In einer Word-Tabelle wird die Zeile mit `{%tr %}`-Tags umschlossen:

| Zelle 1 | Zelle 2 | Zelle 3 |
|---|---|---|
| `{%tr for e in einheiten %}` | | |
| `{{ e.bezeichnung }}` | `{{ e.flaeche }}` | `{{ e.miete }}` |
| `{%tr endfor %}` | | |

Analog: `{%p ... %}` für ganze Absätze, `{%tc %}` für Spalten.

### 3. Bedingte Abschnitte

```
{%p if provisionspflichtig %}
Die Käuferprovision beträgt {{ provision }} % inkl. USt.
{%p endif %}
```

### 4. Befüllen

```python
from docxtpl import DocxTemplate, InlineImage
from docx.shared import Cm

tpl = DocxTemplate("vorlage_wertermittlung.docx")
ctx = {
    "anrede": "Sehr geehrte Frau",
    "nachname": "Meyer",
    "stichtag": "01.09.2026",
    "wert": eur(480000),                      # Formatierung vorher!
    "objekt": {"strasse": "Musterweg 12", "plz": "44801", "ort": "Bochum"},
    "einheiten": [
        {"bezeichnung": "WE 1, EG", "flaeche": "68,4 m²", "miete": eur(612)},
    ],
    "provisionspflichtig": True,
    "provision": "3,57",
    "ansicht": InlineImage(tpl, "objekt.jpg", width=Cm(14)),
}
tpl.render(ctx)
tpl.save("2026-0142_Wertermittlung_Meyer.docx")
```

Hilfsfunktion für deutsche Zahlen:

```python
def eur(x, nk=0):
    s = f"{x:,.{nk}f}"
    return s.replace(",", "X").replace(".", ",").replace("X", ".") + " €"
```

**Regel:** Formatieren in Python, nicht in der Vorlage. Die Vorlage bekommt
fertige Strings – so bleiben Zahlenformat und Rundung an einer Stelle.

### 5. Serienerstellung aus Tabelle

```python
import pandas as pd, pathlib, re

df = pd.read_excel("interessenten.xlsx")
out = pathlib.Path("ausgabe"); out.mkdir(exist_ok=True)
protokoll = []

for _, row in df.iterrows():
    tpl = DocxTemplate("vorlage_absage.docx")     # je Durchlauf neu laden!
    ctx = row.to_dict()
    ctx["anrede"] = "Sehr geehrte Frau" if row["geschlecht"] == "w" else "Sehr geehrter Herr"
    tpl.render(ctx)
    name = re.sub(r"[^\w\-]", "_", f"{row['nachname']}_{row['objekt_id']}")
    ziel = out / f"{name}.docx"
    tpl.save(ziel)
    protokoll.append({"datei": ziel.name, "empfaenger": row["nachname"], "status": "erstellt"})

pd.DataFrame(protokoll).to_csv(out / "_protokoll.csv", index=False)
```

`DocxTemplate` **muss in jeder Iteration neu geladen werden** – ein einmal
gerendertes Objekt lässt sich nicht erneut rendern.

### 6. Vorlage aus einem Bestandsdokument ableiten

1. Musterdokument öffnen und vollständig lesen – auch Kopf- und Fußzeilen,
   Fußnoten und Tabellen
2. Variable Stellen identifizieren: Namen, Adressen, Daten, Beträge, Flächen,
   Aktenzeichen, wiederkehrende Blöcke
3. Diese durch Platzhalter ersetzen, Blöcke in Schleifen fassen
4. Kontext-Schema dokumentieren (welche Felder, welcher Typ, was ist Pflicht)
5. Mit Testdaten rendern und mit dem Original vergleichen

## Standardvorlagen für die Immobilienpraxis

Sinnvolle Vorlagen für den Agenten:

- Wertermittlung / Kurzgutachten (Mantel + Bausteine)
- Maklervertrag und Widerrufsbelehrung
- Besichtigungsbestätigung / Nachweis der Objektnachweisung
- Absage an Interessenten (DSGVO-konform, ohne Begründungsdetails)
- Reservierungsvereinbarung
- Mieterhöhungsverlangen (Vergleichsmiete / Mietspiegel)
- Wohnungsübergabeprotokoll
- Objektaufnahmebogen
- Verkäufer-Statusbericht (Vermarktungsstand)

## Regeln

- **Keine rechtsverbindliche Vorlage ohne juristische Prüfung.** Der Agent
  befüllt Vorlagen; erstellt er eine neue rechtsrelevante Vorlage, geht sie in
  die anwaltliche Prüfung.
- Nie mit leerem Platzhalter ausliefern. Fehlende Werte führen zum Abbruch mit
  Fehlerliste, nicht zu `{{ nachname }}` im fertigen Brief.
- Anrede und Geschlecht nie raten. Fehlt die Angabe: neutrale Anrede
  („Guten Tag, Frau/Herr …" ist keine Lösung – dann „Sehr geehrte Damen und Herren").
- Dateinamen ohne Umlaute und Sonderzeichen, mit Vorgangsnummer und Datum.
- Protokolldatei über jeden Serienlauf – wer hat wann was bekommen.
- Personendaten in Serienläufen: Zweckbindung und Löschfristen beachten
  (siehe Grundregeln, Personendaten).

## Qualitätskontrolle

- [ ] Testrender mit einem Datensatz vor dem Serienlauf
- [ ] Keine verbliebenen `{{ }}` im Ergebnis (programmatisch prüfen!)
- [ ] Pflichtfelder vollständig, Abbruch statt Lücke
- [ ] Zahlen- und Datumsformat deutsch
- [ ] Anrede korrekt
- [ ] Protokolldatei erzeugt
- [ ] Stichprobe: erstes, mittleres und letztes Dokument geöffnet

Prüfskript:

```python
from docx import Document
import re, pathlib
for f in pathlib.Path("ausgabe").glob("*.docx"):
    txt = "\n".join(p.text for p in Document(f).paragraphs)
    if re.search(r"\{\{|\{%", txt):
        print("Platzhalter übrig:", f.name)
```

## Grenzen

docxtpl kann keine Seitenzahlen berechnen und kein Inhaltsverzeichnis füllen.
Sehr komplexe Vorlagen mit verschachtelten Tabellen sind fehleranfällig – dort
lieber mehrere kleine Vorlagen und ein zusammensetzender Schritt.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
