---
name: sachwertverfahren
description: Wertermittlung über Herstellungskosten nach ImmoWertV 2021 §§ 35–39 – NHK 2010, Bruttogrundfläche, Baupreisindex, Regionalfaktor, Alterswertminderung, Sachwertfaktor. Nutzen bei Ein- und Zweifamilienhäusern, eigengenutzten und Sonderobjekten ohne belastbare Vergleichs- oder Ertragsdaten.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE]
---

# Sachwertverfahren

## Zweck

Bewertung über die Herstellungskosten der baulichen Anlagen zuzüglich
Bodenwert, marktangepasst über den Sachwertfaktor. Rechtsgrundlage:
ImmoWertV 2021, §§ 35–39, Anlage 4 (NHK 2010).

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

- Ein- und Zweifamilienhäuser, insbesondere freistehend
- Eigengenutzte Objekte, bei denen der Markt nicht in Renditen denkt
- Objekte ohne ausreichende Vergleichsdaten
- Sonderobjekte mit geringer Marktgängigkeit

**Nicht als alleiniges Verfahren** bei Renditeobjekten – dort führt der
Ertragswert.

## Rechenschema

```
   Bruttogrundfläche (BGF, DIN 277)
 × Normalherstellungskosten (NHK 2010, Anlage 4, €/m² BGF)
 × Baupreisindex-Anpassung (Stichtag / 2010)
 × Regionalfaktor
 = Herstellungskosten (Neubauwert)
 × Alterswertminderungsfaktor                                   § 38
 = vorläufiger Sachwert der baulichen Anlagen                   § 36
 + vorläufiger Sachwert der Außenanlagen und sonstigen Anlagen  § 37
 + Bodenwert                                                    §§ 40 ff.
 = vorläufiger Sachwert
 × objektspezifisch angepasster Sachwertfaktor                  § 39
 ± besondere objektspezifische Grundstücksmerkmale (boG)        §  8
 = Sachwert
```

## Die einzelnen Größen

### Bruttogrundfläche (BGF)

- Nach **DIN 277**, Summe der Grundflächen aller Grundrissebenen, Außenmaß
- **Nicht** Wohnfläche. Ein EFH mit 142 m² Wohnfläche hat typischerweise
  deutlich mehr BGF – Keller, Wandflächen, Treppen, Dachgeschoss zählen mit.
- Aus Bauzeichnungen ermitteln, nicht aus der Wohnfläche hochrechnen. Ist eine
  Näherung unvermeidlich, wird sie als Annahme gekennzeichnet.
- Anrechnung nach Bereichen a/b/c (überdeckt/nicht überdeckt) beachten.

### Normalherstellungskosten (NHK 2010, Anlage 4)

- Kostenkennwerte in €/m² BGF, **einschließlich Baunebenkosten und
  Umsatzsteuer**, Preisstand 2010
- Gegliedert nach Gebäudeart (Ein-/Zweifamilienhäuser, Mehrfamilienhäuser,
  Gewerbe usw.) und **Standardstufe 1–5**
- Die Standardstufe wird über den Gebäudestandard-Katalog der Anlage 4
  hergeleitet (Außenwände, Dach, Fenster, Innenwände, Böden, Sanitär, Heizung,
  Elektro) – nicht pauschal „Standard 3" ansetzen
- Korrekturfaktoren der Anlage 4 (u. a. Gebäudeart/Bauform) berücksichtigen

**Der konkrete Kennwert wird aus Anlage 4 entnommen, nie aus dem Gedächtnis.**

### Baupreisindex

NHK 2010 sind auf das Jahr 2010 bezogen und werden mit dem Preisindex für den
Neubau von Wohngebäuden (Statistisches Bundesamt) auf den Stichtag
fortgeschrieben:

```
Anpassungsfaktor = Index(Stichtag) / Index(2010)
```

Achtung: Die Indexreihe hat inzwischen ein anderes Basisjahr. Beide Werte
müssen aus **derselben** Reihe stammen, sonst ist der Faktor falsch. Der
Anpassungsfaktor ist seit 2021 deutlich gestiegen – ein veralteter Faktor ist
einer der größten Fehler im Sachwertverfahren.

### Regionalfaktor

Vom Gutachterausschuss abgeleiteter Faktor für das regionale Baukostenniveau.
Liegt keiner vor, ist das zu vermerken und der Faktor 1,0 als Annahme zu setzen.

### Alterswertminderungsfaktor (§ 38)

```
Alterswertminderungsfaktor = Restnutzungsdauer / Gesamtnutzungsdauer
```

Lineares Modell nach ImmoWertV. GND aus Anlage 1, RND nach Anlage 2 inklusive
Modernisierungsmodell: Modernisierungselemente (Dach, Fassade/Dämmung,
Fenster, Leitungen, Heizung, Bäder, Innenausbau, Grundriss) werden bepunktet;
daraus folgt der Modernisierungsgrad und daraus eine verlängerte
Restnutzungsdauer. Belege für die Modernisierungen sind erforderlich.

### Außenanlagen (§ 37)

Einfriedungen, Wege, Terrassen, Garagen ohne eigene NHK-Position, Bepflanzung,
Ver- und Entsorgungsanschlüsse. Entweder gesondert kalkuliert oder – wenn im
Modell des Gutachterausschusses so vorgesehen – pauschal als Prozentsatz der
Herstellungskosten der baulichen Anlagen. Beide Wege nicht mischen.

### Sachwertfaktor (§§ 21, 39)

- Der entscheidende Marktanpassungsschritt: Er überführt die Kostenbetrachtung
  in den Marktwert und liegt je nach Lage und Marktlage deutlich unter oder
  über 1,0.
- Wird vom Gutachterausschuss aus Kaufpreisen abgeleitet, abhängig von
  vorläufigem Sachwert und Bodenrichtwertniveau.
- **Modellkonformität (§ 10) ist hier besonders kritisch:** Der Faktor gilt nur,
  wenn BGF-Ermittlung, NHK-Ansatz, Indexierung, GND/RND und Außenanlagen genauso
  angesetzt werden wie im Modell des Gutachterausschusses. Eigene „Verbesserungen"
  machen den Faktor unbrauchbar.
- Liegt kein Sachwertfaktor vor, ist das Ergebnis ein **Kostenwert, kein
  Marktwert** – und muss so bezeichnet werden.

## Rechenbeispiel Einfamilienhaus

```
Objekt: freistehendes EFH, Bj. 1978, Wofl. 142,5 m², BGF 240 m²
Grundstück 520 m², Bodenrichtwert 420 €/m² (zonenangepasst)
GND 80 Jahre (Anlage 1) · Alter 48 Jahre
Modernisierungen 2015 (Heizung, Fenster, Bäder) → RND nach Anlage 2: 40 Jahre

Bodenwert                       520 m² × 420 €/m²      =   218.400 €

NHK 2010, EFH freistehend, Standardstufe 3 (Anlage 4)  =       835 €/m² BGF
  (Beispielwert – im Einsatz aus Anlage 4 entnehmen)
× Baupreisindexanpassung Stichtag/2010                 =     1,785
× Regionalfaktor (GAA)                                 =      0,95
= angepasster Kostenkennwert                           =  1.415,95 €/m² BGF

Herstellungskosten  240 m² × 1.415,95 €/m²             =   339.828 €
× Alterswertminderungsfaktor  40 / 80 = 0,50           =   169.914 €
+ Außenanlagen (gesondert kalkuliert)                  =     8.000 €
+ Bodenwert                                            =   218.400 €
= vorläufiger Sachwert                                 =   396.314 €

× Sachwertfaktor (GAA 2026, Sachwertniveau/BRW-Zone)   =      1,05
= marktangepasster vorläufiger Sachwert                =   416.130 €

boG:
– Wegerecht zugunsten Flurstück 118 (Abt. II Nr. 2),
  Herleitung siehe Abschnitt …                         =  – 15.000 €
= Sachwert                                             =   401.130 €
  gerundet auf volle 5.000 €                           =   400.000 €

Kontrollkennzahlen
  €/m² Wohnfläche       400.000 / 142,5                =   2.807 €/m²
  Bodenwertanteil       218.400 / 396.314              =    55,1 %
Sensitivität
  Sachwertfaktor 0,95 → rd. 361.000 €  |  1,15 → rd. 441.000 €
  RND 35 statt 40 Jahre → rd. 379.000 €
```

## Vorgehen

1. Bodenwert ermitteln (`vergleichswertverfahren`)
2. BGF nach DIN 277 aus den Bauzeichnungen ermitteln
3. Gebäudeart und Standardstufe nach Anlage 4 herleiten, NHK-Kennwert entnehmen
4. Kennwert mit Baupreisindex auf den Stichtag fortschreiben und mit dem
   Regionalfaktor anpassen
5. Herstellungskosten bilden, Alterswertminderungsfaktor (RND/GND) anwenden
6. Außenanlagen ansetzen – gesondert oder pauschal, nicht beides
7. Vorläufigen Sachwert bilden und mit dem Sachwertfaktor marktanpassen
8. Besondere objektspezifische Grundstücksmerkmale ansetzen
9. Runden, Kontrollkennzahlen und Sensitivität (Sachwertfaktor, RND) rechnen

## Regeln

- **BGF, nicht Wohnfläche.** Die Verwechslung ist der häufigste Fehler und
  verfälscht das Ergebnis um 40 % und mehr.
- NHK-Kennwert und Standardstufe aus Anlage 4 herleiten und belegen.
- Baupreisindex aktuell und aus einer einheitlichen Reihe.
- Alterswertminderung linear nach ImmoWertV – keine Restwertkurven aus
  anderen Regelwerken einmischen.
- Sachwertfaktor ist Pflicht für einen Marktwert. Ohne ihn: als Kostenwert
  bezeichnen.
- Modellkonformität über alle Rechenschritte prüfen.
- boG **nach** dem Sachwertfaktor ansetzen, nicht davor.
- Instandhaltungsstau nicht doppelt (einmal über die RND, einmal als boG).

## Ausgabeformat

```
## Sachwertverfahren
### Bodenwert (Herleitung)
### Gebäude: BGF, Gebäudeart, Standardstufe, NHK, Index, Regionalfaktor
### Alterswertminderung: GND, Alter, Modernisierung, RND, Faktor
### Außenanlagen
### Vorläufiger Sachwert
### Marktanpassung: Sachwertfaktor mit Quelle und Modellbezug
### Besondere objektspezifische Grundstücksmerkmale
### Sachwert, Rundung, Kontrollkennzahlen, Sensitivität
```

## Qualitätskontrolle

- [ ] BGF nach DIN 277 aus Zeichnungen, nicht aus Wohnfläche geschätzt
- [ ] Standardstufe hergeleitet, NHK-Kennwert belegt
- [ ] Baupreisindex aktuell, gleiche Indexreihe für beide Werte
- [ ] GND aus Anlage 1, RND nach Anlage 2 hergeleitet
- [ ] Alterswertminderungsfaktor = RND/GND, plausibel (0 < f ≤ 1)
- [ ] Außenanlagen einmal, nicht doppelt
- [ ] Sachwertfaktor vorhanden und modellkonform
- [ ] boG nach der Marktanpassung
- [ ] €/m², Bodenwertanteil und Sensitivität berechnet

## Grenzen

Gilt für Deutschland; in Österreich und der Schweiz gelten eigene Regelwerke
(ÖNORM B 1802 bzw. Realwert nach SVKG-Standard). Der Sachwert ist
kein Herstellungskostenangebot und kein Versicherungswert – der Versicherungswert
folgt eigenen Regeln (gleitender Neuwert, Wert 1914).

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
