---
name: qualitaetssicherung
description: Selbstprüfung vor jeder Auslieferung – Rechenprüfung, Plausibilisierung, Konsistenz, Halluzinationskontrolle, Vollständigkeit. Immer aktiv, wird vor der letzten Antwort ausgeführt.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Qualitätssicherung

## Zweck

Ein zweiter Durchgang über das eigene Ergebnis, bevor es den Nutzer erreicht.
Die häufigsten Fehler von KI-Agenten in der Immobilienarbeit sind nicht
sprachlich, sondern rechnerisch, quellenbezogen und in der Einheitenführung.
Dieser Skill fängt sie ab.

## Wann anwenden

Vor jeder Antwort der Klassen Analyse und Produktion. Bei einfachen Auskünften
genügt Prüfpunkt „Fakten" und „Rechtsstand".

## Vorgehen

Fünf Durchgänge, in dieser Reihenfolge:

### 1. Rechenprüfung

- Jede Rechnung **einmal unabhängig nachrechnen** – möglichst mit einem anderen
  Weg (Überschlag, Rückrechnung, Einheitenprobe), nicht durch erneutes Ablesen
- Einheitenprobe: Passen die Einheiten auf beiden Seiten der Gleichung?
  (Rohertrag in €/Jahr, Miete oft in €/Monat → Faktor 12 geprüft?)
- Rundung erst am Ende, nie in Zwischenschritten
- Prozente: Bezugsgröße explizit? (10 % Abschlag *worauf*?)
- Barwertfaktor / Vervielfältiger: Zinssatz als Dezimalzahl eingesetzt (0,045
  statt 4,5)?

**Faustprobe Ertragswert:** Ergibt sich ein Vervielfältiger, der grob zu
`1 / Liegenschaftszinssatz` passt (bei langer Restnutzungsdauer)? Weicht er
stark ab, ist meist die Restnutzungsdauer oder der Zins falsch eingesetzt.

### 2. Plausibilisierung am Markt

Jedes Wertergebnis gegen mindestens zwei Kennzahlen spiegeln:

- **€/m² Wohnfläche** – liegt es im Korridor der Lage?
- **Faktor** (Kaufpreis / Jahresnettokaltmiete) – plausibel für Objektart und Lage?
- **Bodenwertanteil** am Gesamtwert – bei EFH in guter Lage oft 30–60 %,
  ein Anteil von 5 % oder 95 % ist ein Warnsignal
- **Bruttoanfangsrendite** – passt sie zum Liegenschaftszinssatz?

Bei Auffälligkeit: nicht glätten, sondern die Ursache suchen und benennen.

### 3. Konsistenzprüfung

- Wird dieselbe Fläche im ganzen Dokument gleich genannt?
- Stimmen Zahlen im Text mit Zahlen in Tabellen und Zusammenfassung überein?
- Ist der Stichtag überall derselbe?
- Werden Wohnfläche, Nutzfläche, Bruttogrundfläche und Grundstücksfläche
  sauber auseinandergehalten?
- Passt das Ergebnis der Zusammenfassung zum Ergebnis der Herleitung?

### 4. Halluzinationskontrolle

Jede der folgenden Angaben im Text markieren und prüfen, ob sie belegt ist:

- Paragraphen, Gesetzesnamen, Normen (DIN, ÖNORM, SIA)
- Gerichtsurteile und Aktenzeichen
- Bodenrichtwerte, Liegenschaftszinssätze, Normalherstellungskosten, Indizes
- Mietspiegelwerte
- Fristen und Prozentsätze aus dem Steuerrecht
- Namen von Institutionen und Zuständigkeiten

Nicht belegbar → umformulieren zu „ist beim … abzufragen" oder streichen.
**Eine unsichere Angabe wird nie durch eine plausibel klingende ersetzt.**

### 5. Vollständigkeit gegen den Auftrag

- Wurde jede Teilfrage beantwortet?
- Liegt das Ergebnis im gewünschten Format vor (Datei statt Chattext)?
- Ist der Annahmenblock vorhanden?
- Fehlt ein Eskalationshinweis, der nötig wäre?

## Regeln

- Die Prüfung wird **durchgeführt, nicht behauptet.** Kein „ich habe alles
  geprüft" ohne die Durchgänge.
- Findet die Prüfung einen Fehler, wird korrigiert und **erneut ab Durchgang 1**
  geprüft, nicht nur die Fehlerstelle.
- Bei Unsicherheit über das eigene Ergebnis: Unsicherheit im Ergebnis benennen,
  nicht kaschieren. Eine Wertspanne ist ehrlicher als ein Scheinpräziser Wert.
- Rechenintensive Aufgaben nach Möglichkeit **programmatisch** lösen (Skript,
  Tabellenkalkulation) statt im Kopf – und das Skript als Beleg mitliefern.

## Ausgabeformat

Die Prüfung selbst erscheint nicht in der Antwort. Sichtbar werden nur ihre
Ergebnisse:

- korrigierte Zahlen
- Plausibilitätseinordnung („Der Wert entspricht rund 3.100 €/m² und liegt
  damit im oberen Drittel des für die Lage üblichen Korridors")
- offene Punkte
- ggf. Wertspanne statt Punktwert

## Qualitätskontrolle

- [ ] Alle fünf Durchgänge gelaufen
- [ ] Mindestens eine unabhängige Nachrechnung je Rechnung
- [ ] Zwei Marktkennzahlen zur Plausibilisierung herangezogen
- [ ] Keine unbelegte Zahl, kein unbelegter Paragraph im Text

## Grenzen

Ersetzt keine fachliche Freigabe durch einen Menschen
und keine Prüfung durch einen zweiten Sachverständigen.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
