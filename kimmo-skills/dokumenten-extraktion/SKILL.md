---
name: dokumenten-extraktion
description: Daten aus Immobilienunterlagen herausholen – Grundbuchauszug, Teilungserklärung, Energieausweis, Mietvertrag, Nebenkostenabrechnung, Bauplan, Exposé, Scans und PDFs. Nutzen, wenn Unterlagen ausgewertet, digitalisiert oder in Objektdaten überführt werden sollen.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Dokumenten-Extraktion

## Zweck

Immobilienarbeit beginnt fast immer mit einem Stapel Unterlagen. Dieser Skill
beschreibt, wie aus diesen Dokumenten belastbare, strukturierte Daten werden –
und wie mit Unlesbarem, Widersprüchlichem und Veraltetem umzugehen ist.

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

- Der Nutzer lädt PDFs, Scans oder Fotos von Unterlagen hoch
- Objektdaten sollen aus vorhandenen Dokumenten gefüllt werden
- Ein Bestand an Altakten soll digitalisiert werden

## Vorgehen

### 1. Dokumenttyp erkennen und einordnen

| Dokument | Liefert |
|---|---|
| **Grundbuchauszug** | Eigentümer, Bestandsverzeichnis (Flur, Flurstück, Größe), Abt. II Lasten/Beschränkungen, Abt. III Grundpfandrechte |
| **Flurkarte / Liegenschaftskarte** | Zuschnitt, Lage, Nachbarbebauung, Grenzverlauf |
| **Teilungserklärung + Aufteilungsplan** | Miteigentumsanteile, Sondereigentum/Sondernutzungsrechte, Gemeinschaftsordnung |
| **Energieausweis** | Ausweisart, Kennwert, Klasse, Energieträger, Baujahr, Gültigkeit |
| **Baugenehmigung / Bauakte** | genehmigte Nutzung, Auflagen, Abweichungen vom Ist-Zustand |
| **Bauzeichnung / Grundriss** | Flächen, Raumaufteilung, Geschosse, Kellerart |
| **Wohnflächenberechnung** | Fläche und Rechtsgrundlage (WoFlV, DIN 277, ÖNORM, SIA) |
| **Mietvertrag** | Miete, Nebenkosten, Laufzeit, Anpassungsklausel, Kaution, Sonderrechte |
| **Nebenkostenabrechnung** | umlagefähige und nicht umlagefähige Kosten, Verbräuche |
| **WEG-Protokoll + Wirtschaftsplan** | Beschlüsse, Rücklage, Hausgeld, anstehende Maßnahmen, Sonderumlagen |
| **Erbbaurechtsvertrag** | Erbbauzins, Restlaufzeit, Anpassung, Heimfall, Entschädigung |
| **Kaufvertrag / Notarentwurf** | Kaufpreis, Übergang, Belastungen, Rücktritt, Fälligkeit |
| **Sanierungsnachweise, Rechnungen** | Modernisierungsjahre und -umfang |

### 2. Extraktion

- Zunächst **Textebene** des PDFs nutzen; nur bei Bild-PDFs OCR einsetzen
- Tabellen zeilenweise erfassen, Summen nachrechnen statt übernehmen
- Handschriftliche Einträge und Stempel gesondert markieren (`unsicher`)
- Bei Grundbuchauszügen: **gerötete (durchgestrichene) Einträge sind gelöscht**
  und dürfen nicht als bestehende Rechte übernommen werden
- Datum/Stand jedes Dokuments erfassen – ein zwei Jahre alter Grundbuchauszug
  ist kein Nachweis des aktuellen Standes

### 3. Zusammenführen und Widersprüche auflösen

Immobilienunterlagen widersprechen sich regelmäßig. Vorgehen:

1. Alle Werte je Größe nebeneinanderstellen (z. B. Wohnfläche laut Bauplan,
   laut Exposé, laut Mietvertrag, laut Wohnflächenberechnung)
2. Nach Belastbarkeit ordnen:
   **amtlich/vertraglich > fachliche Berechnung > Verkäufer-/Maklerangabe > Schätzung**
3. Abweichung **nicht mitteln**, sondern ausweisen und ihre Wertrelevanz benennen
4. Bei relevanter Abweichung: Nachmessung / Nachweis anfordern

### 4. Ausgabe

Ergebnis als strukturierter Objektdatensatz (JSON oder Tabelle) plus ein
Extraktionsbericht:

```
## Extraktion
| Größe | Wert | Quelle (Dokument, Seite) | Vertrauen |
|---|---|---|---|
| Wohnfläche | 142,5 m² | Wohnflächenberechnung 2015, S. 2 | hoch |
| Wohnfläche | 148 m² | Exposé Voreigentümer | niedrig – Angebotsangabe |

## Widersprüche
- Wohnfläche: 142,5 m² vs. 148 m² (Δ 3,7 %) → Berechnung maßgeblich, Exposé verworfen

## Nicht lesbar / unsicher
- Abt. II lfd. Nr. 2: handschriftlicher Zusatz nicht entzifferbar

## Fehlende Unterlagen
- Aktueller Grundbuchauszug (vorliegender Stand 03/2023)
```

## Regeln

- **Nichts ergänzen, was nicht im Dokument steht.** Eine unleserliche Stelle
  bleibt unleserlich und wird als solche gemeldet.
- Keine Zahl aus einem Dokument ohne Angabe von Dokument und Fundstelle.
- Grundbuch: Abteilung, laufende Nummer und Rangverhältnis mitführen –
  ein Recht in Abt. II wirkt anders als eine Grundschuld in Abt. III.
- Flächenangaben immer mit Rechtsgrundlage. „142 m²" ohne Basis ist wertlos.
- Personenbezogene Daten aus Dokumenten (Eigentümer, Mieter, Erben) nur
  übernehmen, soweit für die Aufgabe erforderlich – siehe
  den Datenschutzgrundsätzen dieses Skills.
- Bei Scans schlechter Qualität lieber Nacharbeit anfordern als raten.

## Qualitätskontrolle

- [ ] Jeder extrahierte Wert hat Dokument + Fundstelle
- [ ] Gerötete Grundbucheinträge ausgeschlossen
- [ ] Tabellensummen nachgerechnet
- [ ] Widersprüche explizit ausgewiesen, nicht geglättet
- [ ] Dokumentenstände erfasst und auf Aktualität geprüft
- [ ] Unsichere Stellen gekennzeichnet

## Grenzen

Ersetzt keine Grundbucheinsicht durch Berechtigte und keine sachverständige
Beurteilung von Bauzeichnungen oder Schäden. Rechtliche Würdigung von
Verträgen gehört zu Notar, Anwalt oder der fachlich zuständigen Person.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
