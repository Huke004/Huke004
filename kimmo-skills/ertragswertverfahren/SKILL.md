---
name: ertragswertverfahren
description: Wertermittlung von Renditeobjekten nach ImmoWertV 2021 §§ 27–34 – allgemeines, vereinfachtes und periodisches Ertragswertverfahren, Rohertrag, Bewirtschaftungskosten, Liegenschaftszinssatz, Barwertfaktor. Nutzen bei Mehrfamilienhäusern, Wohn- und Geschäftshäusern, Gewerbe und allen vermieteten Objekten.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE]
---

# Ertragswertverfahren

## Zweck

Bewertung aus der Ertragsfähigkeit: Was ist ein Objekt wert, das dauerhaft
Erträge abwirft? Rechtsgrundlage: ImmoWertV 2021, §§ 27–34.

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

- Mehrfamilienhäuser, Wohn- und Geschäftshäuser
- Gewerbeimmobilien: Büro, Einzelhandel, Logistik
- Vermietete Eigentumswohnungen (stützend zum Vergleichswert)
- Immer dort, wo der Markt in Renditen denkt

## Drei Verfahrensvarianten (§§ 28–30)

| Variante | Kern | Wann |
|---|---|---|
| **Allgemeines** (§ 28) | Bodenwertverzinsung wird vom Reinertrag abgezogen, der Gebäudereinertrag kapitalisiert, der Bodenwert addiert | Regelfall |
| **Vereinfachtes** (§ 29) | Gesamtreinertrag kapitalisiert, Bodenwert auf den Stichtag abgezinst addiert | wenn so vom Gutachterausschuss modelliert |
| **Periodisches** (§ 30) | periodenweise Erträge und Kosten, DCF-nah | ungleichmäßige Zahlungsströme, Gewerbe, Entwicklung |

**Modellkonformität (§ 10):** Die Variante muss zu dem Modell passen, in dem
der verwendete Liegenschaftszinssatz abgeleitet wurde. Ein Zinssatz aus dem
allgemeinen Verfahren darf nicht ins vereinfachte übernommen werden.

## Rechenschema – allgemeines Ertragswertverfahren

```
   Rohertrag (marktüblich erzielbar, p. a.)                    § 31
 – Bewirtschaftungskosten                                      § 32
 = Reinertrag
 – Bodenwertverzinsung (Bodenwert × Liegenschaftszinssatz)
 = Gebäudereinertrag
 × Barwertfaktor (Restnutzungsdauer, Liegenschaftszinssatz)    § 34
 = Gebäudeertragswert
 + Bodenwert
 = vorläufiger Ertragswert
 ± besondere objektspezifische Grundstücksmerkmale (boG)       §  8
 = Ertragswert
```

### Rohertrag (§ 31)

- Anzusetzen ist die **marktüblich erzielbare** Miete, nicht zwingend die
  Ist-Miete.
- Ist-Miete unter Marktniveau (Altmietvertrag, Mietpreisbremse,
  Kappungsgrenze) → die Differenz ist als boG oder über einen
  Übergangszeitraum zu berücksichtigen, nicht einfach wegzurechnen.
- Ist-Miete über Marktniveau → ebenfalls prüfen; Überzahlungen sind nicht
  dauerhaft kapitalisierbar.
- Nettokaltmiete, ohne umlagefähige Betriebskosten.
- Stellplätze, Werbeflächen, Antennenstandorte gehören dazu.
- Strukturellen Leerstand über den Rohertrag oder das Mietausfallwagnis
  abbilden – **nicht doppelt**.

### Bewirtschaftungskosten (§ 32)

Vier Positionen, Modellansätze in **Anlage 3** der ImmoWertV:

| Position | Übliche Erfassung |
|---|---|
| Verwaltungskosten | € je Wohneinheit/Jahr bzw. % vom Rohertrag |
| Instandhaltungskosten | € je m² Wohnfläche/Jahr bzw. je Einheit |
| Mietausfallwagnis | % vom Rohertrag |
| nicht umlagefähige Betriebskosten | tatsächlich/erfahrungsgemäß |

**Regel:** Ansätze aus Anlage 3 oder aus dem Modell des Gutachterausschusses
verwenden – nicht die tatsächlichen Kosten eines einzelnen Jahres, es sei
denn, sie sind marktüblich und dauerhaft. Instandhaltungsstau gehört **nicht**
in die laufenden Kosten, sondern als boG in den Abzug.

### Liegenschaftszinssatz (§§ 21, 33)

- Wird vom Gutachterausschuss aus Kaufpreisen abgeleitet – nicht selbst
  „gefühlt" festlegen.
- Objektspezifische Anpassung (§ 33) ist möglich und begründungspflichtig
  (Lage, Objektart, Restnutzungsdauer, Mieterstruktur, Drittverwendungs-
  fähigkeit).
- Größenordnungen als grobe Orientierung – **immer durch die Quelle ersetzen**:
  Wohnen in guten Lagen niedriger, Gewerbe und Spezialimmobilien höher.
- Der Zinssatz wirkt hebelartig: 0,5 Prozentpunkte verändern den Wert leicht um
  10 %. Deshalb gehört zu jedem Ertragswert eine **Sensitivitätsangabe**.

### Barwertfaktor (§ 34)

Rentenbarwertfaktor bei nachschüssiger Zahlung:

```
V = (q^n − 1) / (q^n × (q − 1))        mit q = 1 + p, p = Liegenschaftszinssatz

n = Restnutzungsdauer in Jahren
```

Kontrolle: Für große n nähert sich V dem Wert 1/p. Bei p = 4,0 % ist
1/p = 25,0 – ein Barwertfaktor von 40 kann dann nicht stimmen.

## Vereinfachtes Ertragswertverfahren (§ 29)

```
   Reinertrag × Barwertfaktor (RND, LZ)
 + Bodenwert × Abzinsungsfaktor  (1 / q^n)
 = vorläufiger Ertragswert
```

## Periodisches Ertragswertverfahren / DCF (§ 30)

Für ungleichmäßige Zahlungsströme: Auslaufende Mietverträge, Leerstands-
abbau, Sanierungsphasen, Projektentwicklung, Staffel- und Indexmieten.

```
Wert = Σ ( CFt / q^t )  für t = 1..T   +   Restwert(T) / q^T
```

- Detailplanungsphase üblicherweise 10 Jahre
- Restwert über Kapitalisierung des nachhaltigen Reinertrags am Ende der
  Planungsphase
- Diskontierungssatz und Kapitalisierungssatz sind **nicht identisch** und
  werden getrennt begründet
- Der Restwert dominiert das Ergebnis oft zu über 50 % – seine Herleitung ist
  der kritischste Teil, nicht der Cashflow der ersten Jahre

## Rechenbeispiel Mehrfamilienhaus

```
Objekt: MFH, 8 WE, 612 m² Wofl., Bj. 1972, RND 32 Jahre
Bodenwert:  480 m² × 310 €/m² = 148.800 €
Liegenschaftszinssatz (GAA 2026, Zone …): 3,8 %

Rohertrag (marktüblich)         612 m² × 9,20 €/m² × 12 =   67.564,80 €/a
– Verwaltung        8 WE × 320 €/a                     =    2.560,00 €
– Instandhaltung    612 m² × 11,50 €/m²·a              =    7.038,00 €
– Mietausfallwagnis 2,0 % vom Rohertrag                =    1.351,30 €
– nicht umlagefähige Betriebskosten                    =      950,00 €
= Bewirtschaftungskosten                                   11.899,30 €
= Reinertrag                                               55.665,50 €/a

– Bodenwertverzinsung  148.800 € × 3,8 %               =    5.654,40 €
= Gebäudereinertrag                                        50.011,10 €/a

Barwertfaktor  q = 1,038 ; n = 32
  q^32 = 3,2985
  V = (3,2985 − 1) / (3,2985 × 0,038) = 2,2985 / 0,12534 = 18,338

Gebäudeertragswert  50.011,10 × 18,338                 =  917.087 €
+ Bodenwert                                            =  148.800 €
= vorläufiger Ertragswert                              = 1.065.887 €

boG:
– Instandhaltungsstau Dach und Stränge (Kostenschätzung
  120.000 €, marktüblich zu ca. 80 % preiswirksam)     =  – 96.000 €
= Ertragswert                                          =  969.887 €
  gerundet                                             =  970.000 €

Kontrollkennzahlen
  Faktor (Wert / Jahresnettokaltmiete)  969.887 / 67.565 = 14,4
  Bruttoanfangsrendite                                    7,0 %
  €/m² Wohnfläche                                       1.585 €/m²
Sensitivität Liegenschaftszinssatz (Barwertfaktor und Bodenwertverzinsung
jeweils neu gerechnet)
  3,3 % → V = 19,581 → rd. 1.047.000 €
  4,3 % → V = 17,210 → rd.   901.000 €
  Spanne rd. ±8 % bei ±0,5 Prozentpunkten
```

## Vorgehen

1. Verfahrensvariante wählen – passend zum Modell des verwendeten
   Liegenschaftszinssatzes (§ 10 Modellkonformität)
2. Bodenwert ermitteln (`vergleichswertverfahren`)
3. Marktüblich erzielbaren Rohertrag bestimmen und mit der Ist-Miete abgleichen
4. Bewirtschaftungskosten nach Anlage 3 bzw. GAA-Modell ansetzen
5. Reinertrag, Bodenwertverzinsung und Gebäudereinertrag rechnen
6. Restnutzungsdauer und Liegenschaftszinssatz belegen, Barwertfaktor bilden
   und gegen 1/p plausibilisieren
7. Gebäudeertragswert und vorläufigen Ertragswert bilden
8. Besondere objektspezifische Grundstücksmerkmale ansetzen
9. Kontrollkennzahlen (Faktor, Bruttoanfangsrendite, €/m²) und Sensitivität
   über Zinssatz und Miete rechnen

## Regeln

- **Marktmiete, nicht Ist-Miete** – und die Differenz sichtbar behandeln.
- Bewirtschaftungskosten aus dem Modell, nicht aus einem Zufallsjahr.
- Instandhaltungsstau als boG, nicht in den laufenden Kosten.
- Liegenschaftszinssatz aus der Quelle, Anpassung begründet.
- Restnutzungsdauer nach ImmoWertV Anlage 1 (Gesamtnutzungsdauer) und
  Anlage 2 (Punktemodell für Modernisierungen) hergeleitet, nicht geschätzt.
- Zinssatz als Dezimalzahl in die Formel (0,038 – nicht 3,8).
- Zu jedem Ertragswert eine Sensitivität über Zinssatz und Miete.
- Verfahrensvariante und Datenmodell müssen zusammenpassen (§ 10).

## Qualitätskontrolle

- [ ] Rohertrag: marktüblich, Nettokaltmiete, alle Ertragsquellen erfasst
- [ ] Leerstand nicht doppelt berücksichtigt
- [ ] Bewirtschaftungskosten modellkonform, Anlage 3 bzw. GAA-Modell
- [ ] Barwertfaktor gegen 1/p plausibilisiert
- [ ] Bodenwert nicht doppelt (Verzinsung abgezogen **und** addiert – korrekt!)
- [ ] boG separat ausgewiesen und hergeleitet
- [ ] Faktor, Bruttoanfangsrendite und €/m² als Kontrolle berechnet
- [ ] Sensitivität ausgewiesen

## Grenzen

Gilt für Deutschland; in Österreich und der Schweiz gelten eigene Regelwerke
(LBG/ÖNORM bzw. SVKG-Standard mit DCF). Betreiber- und
Spezialimmobilien (Hotel, Pflege, Freizeit) erfordern zusätzlich eine
Betreiberanalyse – dort ist der Ertragswert ohne Prüfung des Betreiberkonzepts
nicht belastbar.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
