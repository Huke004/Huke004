---
name: word-review-kommentare
description: Word-Dokumente prüfen und kommentieren – Änderungsverfolgung lesen und auswerten, Kommentare extrahieren, Versionen vergleichen, redaktionelle und fachliche Prüfung von Verträgen und Gutachten. Nutzen bei Korrekturlesen, Review, Vertragsprüfung, Änderungen nachvollziehen.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Word: Review, Kommentare und Änderungsverfolgung

## Zweck

Der Alltag in Maklerbüros und Sachverständigenbüros besteht zu einem großen
Teil aus Dokumenten, die hin- und hergehen: Notarentwürfe, Gutachtenentwürfe,
Mietverträge, Kaufvertragsfassungen. Dieser Skill regelt, wie der Agent solche
Dokumente prüft, Änderungen nachvollzieht und Rückmeldungen gibt.

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

- „Was hat der Notar in Fassung 3 geändert?"
- „Lies die Kommentare und arbeite sie ein"
- „Prüfe diesen Vertragsentwurf"
- „Korrekturlesen"

## Vorgehen

### 1. Zustand feststellen – immer zuerst

```python
import zipfile
xml = zipfile.ZipFile(pfad).read("word/document.xml").decode("utf-8")
offen_ins  = xml.count("<w:ins ")
offen_del  = xml.count("<w:del ")
hat_kommentare = "word/comments.xml" in zipfile.ZipFile(pfad).namelist()
```

Ergebnis dem Nutzer **vor der inhaltlichen Arbeit** melden:

> Das Dokument enthält 23 nicht angenommene Einfügungen, 11 Löschungen und
> 6 Kommentare. Soll ich mit angenommenen oder abgelehnten Änderungen arbeiten?

Wird darauf nicht geantwortet: mit angenommenen Änderungen arbeiten und dies
ausdrücklich vermerken.

### 2. Änderungen mit Autor und Datum auslesen

```python
from lxml import etree
W = "http://schemas.openxmlformats.org/wordprocessingml/2006/main"

tree = etree.fromstring(zipfile.ZipFile(pfad).read("word/document.xml"))
for tag, art in ((f"{{{W}}}ins", "Einfügung"), (f"{{{W}}}del", "Löschung")):
    for node in tree.iter(tag):
        autor = node.get(f"{{{W}}}author")
        datum = node.get(f"{{{W}}}date")
        text = "".join(t.text or "" for t in node.iter())
        print(f"{art} | {autor} | {datum} | {text.strip()[:120]}")
```

### 3. Kommentare mit Bezugstext

`comments.xml` enthält die Kommentartexte, `document.xml` die Ankerstellen
(`w:commentRangeStart` / `w:commentRangeEnd` mit gleicher `w:id`). Für
brauchbares Review beides zusammenführen – ein Kommentar ohne Bezugstext ist
nicht bewertbar.

```python
z = zipfile.ZipFile(pfad)
komm = {}
if "word/comments.xml" in z.namelist():
    ct = etree.fromstring(z.read("word/comments.xml"))
    for c in ct.iter(f"{{{W}}}comment"):
        komm[c.get(f"{{{W}}}id")] = {
            "autor": c.get(f"{{{W}}}author"),
            "datum": c.get(f"{{{W}}}date"),
            "text": "".join(t.text or "" for t in c.iter(f"{{{W}}}t")),
        }
```

### 4. Versionsvergleich

Der zuverlässigste Weg ist Words eigener Vergleich (`Überprüfen → Vergleichen`).
Programmatisch: absatzweiser Diff mit Kontext.

```python
import difflib
from docx import Document

def absaetze(p): return [x.text.strip() for x in Document(p).paragraphs if x.text.strip()]

sm = difflib.SequenceMatcher(None, absaetze("v2.docx"), absaetze("v3.docx"))
for op, i1, i2, j1, j2 in sm.get_opcodes():
    if op != "equal":
        print(f"[{op}]")
        for line in absaetze("v2.docx")[i1:i2]: print("  – ", line[:200])
        for line in absaetze("v3.docx")[j1:j2]: print("  + ", line[:200])
```

**Ein Diff ist kein Review.** Jede Änderung wird eingeordnet:
redaktionell / inhaltlich / rechtlich relevant / wirtschaftlich relevant.

### 5. Fachliche Prüfung

Prüfraster je Dokumentart:

**Kaufvertragsentwurf** (Prüfung durch den Agenten = Vorprüfung, kein Rechtsrat)
- Kaufpreis, Fälligkeit, Fälligkeitsvoraussetzungen
- Übergang von Besitz, Nutzen, Lasten und Gefahr – Datum stimmig?
- Vertragsgegenstand: Grundbuchbezeichnung, Flurstücke, Miteigentumsanteil vollständig?
- Übernahme/Löschung von Rechten in Abt. II und III
- Gewährleistungsausschluss, Ausnahmen (Arglist, übernommene Beschaffenheiten)
- Zusicherungen zu Wohnfläche, Energieausweis, Mietverhältnissen, Altlasten
- mitverkauftes Zubehör
- Vorkaufsrechte, Genehmigungen (WEG-Verwalter, Sanierungsgebiet)
- Kostentragung, Vollzug, Vollmachten
- Rücktritts- und Vertragsstrafenregelungen

**Gutachtenentwurf**
- Vollständigkeit gegen die Gliederung aus `verkehrswertgutachten`
- Stichtag durchgängig identisch
- Zahlen in Text, Tabellen und Zusammenfassung deckungsgleich
- jede Eingangsgröße mit Quelle
- Annahmen und Einschränkungen ausgewiesen

**Mietvertrag**
Parteien, Mietsache und Fläche, Laufzeit, Miethöhe und
Anpassungsmechanik (Staffel oder Index), Betriebskostenumlage und Schlüssel,
Kaution, Schönheitsreparaturen- und Kleinreparaturklausel, Kündigungsregeln

### 6. Rückmeldung erzeugen

Als strukturierte Liste, nicht als Fließtext:

```
## Review <Dokument>, Fassung <n> vom <Datum>

### Wirtschaftlich relevant
1. § 4 Abs. 2 – Fälligkeit jetzt „14 Tage nach Mitteilung" statt „nach Vorliegen
   der Löschungsbewilligung". Wirkung: Zahlungspflicht vor Lastenfreiheit.
   → klärungsbedürftig durch Notar/Anwalt

### Rechtlich relevant
2. …

### Redaktionell
7. § 9 – „Vertragsobjekt" vs. „Kaufgegenstand" uneinheitlich

### Offene Kommentare
- [MW, 28.08.2026] zu § 6: „Bitte Zubehörliste ergänzen" – noch nicht umgesetzt

### Nicht geprüft
- Steuerliche Auswirkungen der Kaufpreisaufteilung
```

Kommentare, die eingearbeitet werden sollen, werden **einzeln abgearbeitet und
als erledigt/offen/strittig markiert** – nie stillschweigend übergangen.

## Regeln

- **Nie Änderungen anderer annehmen oder ablehnen**, ohne dass der Nutzer das
  ausdrücklich beauftragt hat. Änderungsverfolgung ist Beweismittel.
- Bei Verträgen den **Wortlaut zitieren**, nicht paraphrasieren.
- Rechtliche Bewertung bleibt beim Anwalt/Notar – der Agent benennt
  Auffälligkeiten und deren mögliche Wirkung.
- Autorennamen aus Änderungsverfolgung sind Personendaten – im Review nur
  verwenden, soweit für die Nachvollziehbarkeit nötig.
- Vor Weitergabe an Dritte prüfen, ob Metadaten und Änderungsverfolgung
  entfernt werden sollen (Word: `Dokument prüfen`) – dort stehen oft interne
  Kommentare und frühere Kalkulationen.

## Neue Kommentare einfügen

Kommentare programmatisch zu schreiben ist mit python-docx nicht vorgesehen
und über direktes XML fehleranfällig. Praktikable Wege:

1. Rückmeldung als separates Review-Dokument (empfohlen)
2. Änderungen als sichtbare Markierung im Text (Hervorhebung + eckige Klammern)
3. Bearbeitung im Word-Add-in/Automatisierung auf dem Rechner des Nutzers

## Qualitätskontrolle

- [ ] Zustand (offene Änderungen, Kommentare) vor der Arbeit gemeldet
- [ ] Jede Änderung eingeordnet, nicht nur aufgelistet
- [ ] Kommentare mit Bezugstext ausgewertet, Status je Kommentar gesetzt
- [ ] Zitate wörtlich, mit Fundstelle
- [ ] Rechtliche Bewertung als solche abgegrenzt
- [ ] Hinweis auf Metadatenbereinigung vor Weitergabe

## Grenzen

Keine Rechtsberatung, keine abschließende Vertragsprüfung. Kein
Seitenzahlenbezug, da die Paginierung einer .docx erst beim Rendern entsteht.
Word-eigener
Dokumentvergleich bleibt bei komplexen Umstellungen überlegen.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
