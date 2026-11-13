---
name: rendite-und-finanzierung
description: Renditekennzahlen und Finanzierungsrechnung für Immobilieninvestitionen – Kaufnebenkosten, Brutto- und Nettoanfangsrendite, Cashflow, Eigenkapitalrendite, Annuitätendarlehen, Tilgungsplan, Restschuld, Sensitivität. Nutzen bei Rendite, Cashflow, Finanzierung, Annuität, Tilgung, Kapitalanlage, „lohnt sich das".
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Rendite und Finanzierung

## Zweck

Die Frage „lohnt sich das?" wird mit unterschiedlichen Kennzahlen
unterschiedlich beantwortet. Dieser Skill legt fest, welche Kennzahl was
aussagt, wie sie gerechnet wird und wo die typischen Rechenfehler sitzen.

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

- Kapitalanlage-Prüfung, Ankaufsrechnung
- Finanzierungsstruktur und Tilgungsverlauf
- Vergleich mehrerer Objekte
- Frage nach Rendite, Cashflow, Eigenkapitalverzinsung

## Kaufnebenkosten (Deutschland)

| Position | Größenordnung | Hinweis |
|---|---|---|
| Grunderwerbsteuer | **je Bundesland unterschiedlich, 3,5 %–6,5 %** | Satz recherchieren, nie annehmen |
| Notar und Grundbuch | rund 1,5 %–2,0 % | GNotKG, wertabhängig |
| Maklerprovision | marktabhängig, häufig 3,57 % inkl. USt für den Käufer | Provisionsteilung nach §§ 656a ff. BGB beachten |
| Gutachten, Gebühren | fallweise | |

Faustzahl 9–12 % – aber im konkreten Fall immer aus dem tatsächlichen
Grunderwerbsteuersatz des Bundeslands rechnen. Österreich (Grunderwerbsteuer,
Eintragungsgebühr) und Schweiz (kantonale Handänderungssteuer) haben andere
Sätze.

## Kennzahlen

### Bruttoanfangsrendite

```
BAR = Jahresnettokaltmiete / Kaufpreis
```

Schnelle Vergleichszahl, aber ohne Nebenkosten und ohne Bewirtschaftung.
Kehrwert ist der bekannte **Faktor** (Kaufpreis / Jahresnettokaltmiete).

### Nettoanfangsrendite

```
NAR = Reinertrag / (Kaufpreis + Kaufnebenkosten)
```

Reinertrag = Jahresnettokaltmiete abzüglich nicht umlagefähiger
Bewirtschaftungskosten (Verwaltung, Instandhaltung, Mietausfallwagnis,
nicht umlagefähige Betriebskosten). Die ehrlichere Zahl.

### Cashflow

```
Cashflow vor Steuern = Reinertrag – Kapitaldienst (Zins + Tilgung)
Cashflow nach Steuern = Cashflow v. St. – Einkommensteuer auf das Ergebnis
```

Achtung: **Tilgung ist Vermögensaufbau, keine Kosten.** Ein negativer
Cashflow bei hoher Tilgung ist etwas anderes als ein negativer Cashflow bei
niedriger Miete. Beides getrennt ausweisen.

### Eigenkapitalrendite

```
EK-Rendite = Cashflow vor Steuern / eingesetztes Eigenkapital
```

Eigenkapital = Anzahlung **plus** Kaufnebenkosten, die üblicherweise nicht
mitfinanziert werden. Wer die Nebenkosten vergisst, rechnet die Rendite
systematisch zu hoch.

Vollständiger ist der **Gesamtertrag** aus Cashflow + Tilgungsanteil +
Wertänderung, bezogen auf das Eigenkapital – die Wertänderung ist dabei eine
Annahme und als solche zu kennzeichnen.

## Finanzierungsrechnung

### Annuitätendarlehen

```
Annuität = Darlehen × (Zinssatz + anfänglicher Tilgungssatz)

Zins(Jahr 1)    = Darlehen × Zinssatz
Tilgung(Jahr 1) = Annuität – Zins(Jahr 1)
```

Der Tilgungsanteil steigt jedes Jahr, der Zinsanteil fällt.

### Restschuld nach n Jahren

```
Restschuld(n) = D × q^n – A × (q^n – 1) / (q – 1)

D = Darlehen, A = Annuität, q = 1 + Zinssatz
```

### Zinsbindung und Anschlussrisiko

Die Restschuld am Ende der Zinsbindung ist die entscheidende Größe. Jede
Finanzierungsrechnung enthält ein **Anschlussszenario** mit einem höheren
Zinssatz – sonst ist sie unvollständig.

## Rechenbeispiel

```
Objekt: MFH, 8 WE, 612 m² Wohnfläche
Kaufpreis                                                    970.000 €
Kaufnebenkosten
  Grunderwerbsteuer NRW 6,5 %                                 63.050 €
  Notar und Grundbuch 1,5 %                                   14.550 €
  Maklerprovision 3,57 %                                      34.629 €
  Summe 11,57 %                                              112.229 €
Gesamtinvestition                                          1.082.229 €

Jahresnettokaltmiete                                          67.565 €
– nicht umlagefähige Bewirtschaftungskosten                   11.899 €
= Reinertrag                                                  55.666 €

Bruttoanfangsrendite   67.565 / 970.000                          6,97 %
Faktor                 970.000 / 67.565                          14,4
Nettoanfangsrendite    55.666 / 1.082.229                        5,14 %

Finanzierung
  Eigenkapital                                               300.000 €
  Darlehen                                                   782.229 €
  Zins 3,80 % · anfängliche Tilgung 2,00 % · Zinsbindung 10 Jahre
  Annuität  782.229 × 5,80 %                                  45.369 €/a
    davon Zins Jahr 1                                         29.725 €
    davon Tilgung Jahr 1                                      15.645 €

Cashflow vor Steuern   55.666 – 45.369                        10.297 €/a
Eigenkapitalrendite    10.297 / 300.000                          3,43 %
Vermögenszuwachs Jahr 1 (Cashflow + Tilgung)                  25.941 €
  bezogen auf Eigenkapital                                       8,65 %

Nach 10 Jahren
  Restschuld                                                 596.131 €
  getilgt                                                    186.098 €

Anschlussszenario Zins 5,5 % bei gleicher Annuität
  Zins Jahr 11  596.131 × 5,5 %                               32.787 €
  Tilgung                                                     12.582 €
  → Cashflow sinkt, Tilgungsdauer verlängert sich deutlich

Sensitivität
  Miete –10 %          → Cashflow    3.540 €/a
  Zins +1,5 %-Punkte   → Kapitaldienst steigt um rd. 11.700 €/a
  Leerstand 3 Monate einer Einheit → Cashflow rd. –2.100 €/a
```

## Vorgehen

1. Kaufpreis und Kaufnebenkosten mit dem tatsächlichen Grunderwerbsteuersatz
   des Bundeslands bzw. Kantons ermitteln
2. Rohertrag und nicht umlagefähige Bewirtschaftungskosten ansetzen,
   Reinertrag bilden
3. Renditekennzahlen rechnen (BAR, Faktor, NAR)
4. Finanzierung strukturieren: Eigenkapital inklusive Nebenkosten, Darlehen,
   Zins, Tilgung, Zinsbindung
5. Cashflow, Eigenkapitalrendite und Vermögenszuwachs getrennt ausweisen
6. Restschuld am Ende der Zinsbindung und Anschlussszenario rechnen
7. Sensitivität über Miete, Zins und Leerstand
8. Annahmen sammeln und das Ergebnis einordnen

## Regeln

- **Grunderwerbsteuersatz recherchieren**, nicht schätzen – die Spanne
  zwischen den Bundesländern beträgt fast das Doppelte.
- Kaufnebenkosten gehören ins Eigenkapital, nicht in die Finanzierung
  (außer, sie werden ausdrücklich mitfinanziert).
- Tilgung getrennt vom Aufwand ausweisen.
- Instandhaltungsrücklage ansetzen – auch wenn der Verkäufer sagt, es sei
  „alles gemacht".
- Bei Eigentumswohnungen: nicht umlagefähiges Hausgeld und Zuführung zur
  Erhaltungsrücklage abziehen.
- Wertsteigerungsannahmen sind Annahmen. Eine Rechnung, die nur durch
  angenommene Wertsteigerung funktioniert, ist als solche zu benennen.
- Jede Rechnung mit Sensitivität (Miete, Zins, Leerstand).
- Steuerliche Effekte nur als Größenordnung, mit Verweis auf
  den Steuerberater.

## Ausgabeformat

Tabelle mit den Blöcken Investition / Ertrag / Kennzahlen / Finanzierung /
Cashflow / Szenarien, dazu ein Absatz Einordnung und der Annahmenblock.
Bei mehreren Objekten: Vergleichstabelle mit identischen Annahmen.

Für wiederkehrende Rechnungen empfiehlt sich eine Tabellenkalkulation mit
offenen Eingabefeldern statt eines Fließtextergebnisses.

## Qualitätskontrolle

- [ ] Grunderwerbsteuersatz des richtigen Bundeslands/Kantons
- [ ] Kaufnebenkosten im Eigenkapital berücksichtigt
- [ ] Reinertrag nach Abzug nicht umlagefähiger Kosten, nicht Rohertrag
- [ ] Tilgung nicht als Kosten behandelt
- [ ] Zinssatz als Dezimalzahl in den Formeln
- [ ] Restschuld am Ende der Zinsbindung berechnet
- [ ] Anschlussszenario mit höherem Zins gerechnet
- [ ] Sensitivität für Miete, Zins und Leerstand
- [ ] Wertsteigerungsannahmen gekennzeichnet

## Grenzen

Keine Finanzierungs- oder Anlageberatung, keine Bonitätsprüfung, keine
Bankkonditionen. Steuerliche Wirkungen sind überschlägig und ersetzen keine
steuerliche Beratung; sie gehört zum Steuerberater.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
