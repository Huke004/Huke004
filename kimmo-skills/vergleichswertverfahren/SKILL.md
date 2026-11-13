---
name: vergleichswertverfahren
description: Wertermittlung über Vergleichspreise und Vergleichsfaktoren nach ImmoWertV 2021 §§ 24–26 sowie Bodenwertermittlung über Bodenrichtwerte. Nutzen bei Eigentumswohnungen, Reihenhäusern, unbebauten Grundstücken und überall dort, wo Kaufpreise vergleichbarer Objekte vorliegen.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE]
---

# Vergleichswertverfahren

## Zweck

Das marktnächste Verfahren: Der Wert wird aus tatsächlich gezahlten Kaufpreisen
hinreichend übereinstimmender Grundstücke abgeleitet. Rechtsgrundlage:
ImmoWertV 2021, §§ 24–26; Bodenwertermittlung Teil 4 Abschnitt 1.

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

- Eigentumswohnungen, Reihenhäuser, Doppelhaushälften in homogenen Lagen
- Unbebaute Grundstücke (fast immer)
- Standardisierte Objekte mit ausreichender Datenlage
- Als **Bodenwertermittlung** in nahezu jeder anderen Bewertung

**Nicht anwenden**, wenn keine belastbaren Vergleichspreise vorliegen. Dann
Sachwert- oder Ertragswertverfahren – nicht ersatzweise Angebotspreise nehmen.

## Zwei Wege

### Weg A: Vergleichspreise (§ 25)

1. **Vergleichsfälle beschaffen.** Quelle ist die Kaufpreissammlung des
   Gutachterausschusses. Angebotspreise aus Portalen sind **keine**
   Vergleichspreise.
2. **Auswahl:** hinreichende Übereinstimmung in Lage, Art, Größe, Ausstattung,
   Zustand, Baujahr, Grundstücksgröße, Rechtslage. Zeitlicher Bezug zum
   Stichtag.
3. **Anzahl:** Faustregel mindestens 5–8 auswertbare Fälle. Bei weniger ist die
   Aussagekraft zu relativieren; bei 1–2 Fällen ist es kein
   Vergleichswertverfahren mehr.
4. **Anpassung** der Vergleichspreise an das Bewertungsobjekt:
   - **zeitlich** über Indexreihen (§ 18)
   - **objektbezogen** über Umrechnungskoeffizienten (§ 19) für abweichende
     Merkmale (Grundstücksgröße, Geschossfläche, Baujahr, Wohnfläche)
   - **einzelfallbezogen** über begründete Zu-/Abschläge, wenn keine
     Koeffizienten vorliegen
5. **Auswertung:** Ausreißer prüfen und begründet ausschließen (nicht
   stillschweigend). Statistisches Maß bilden – Median ist bei kleiner
   Fallzahl robuster als der Mittelwert. Streuung ausweisen.
6. **Besondere objektspezifische Grundstücksmerkmale (boG)** nach § 8
   berücksichtigen: Baumängel, Instandhaltungsstau, Rechte und Lasten,
   überdurchschnittliche Ausstattung, Denkmalschutz. Diese werden **nach**
   dem Verfahren als Zu-/Abschlag angesetzt und einzeln hergeleitet.

### Weg B: Vergleichsfaktoren (§ 26)

Vom Gutachterausschuss abgeleitete Faktoren, angewandt auf eine Bezugsgröße:

- **Gebäudefaktor** je m² Wohnfläche
- **Ertragsfaktor** (Vervielfältiger auf den Jahresrohertrag)

```
Vergleichswert = Vergleichsfaktor × Bezugsgröße
```

Voraussetzung: **Modellkonformität** (§ 10). Der Faktor gilt nur mit dem
Flächenbegriff und den Modellannahmen, unter denen er abgeleitet wurde.

## Bodenwertermittlung

Der Boden wird stets so bewertet, als wäre er unbebaut (§ 40).

```
Bodenwert = angepasster Bodenrichtwert (€/m²) × Grundstücksfläche (m²)
```

Ablauf:

1. Bodenrichtwert der zutreffenden Zone zum Stichtag ermitteln
   (Gutachterausschuss / BORIS des Landes)
2. **Merkmale des Bodenrichtwertgrundstücks** feststellen (Anlage 5 ImmoWertV:
   Entwicklungszustand, Art und Maß der baulichen Nutzung, Grundstücksgröße,
   -tiefe, -breite, Erschließungszustand, beitragsrechtlicher Zustand)
3. Abweichungen des Bewertungsgrundstücks anpassen – über
   Umrechnungskoeffizienten (§ 19), sonst begründete Zu-/Abschläge
4. Sonderfälle:
   - **Erhebliche Überschreitung der marktüblichen Grundstücksgröße** (§ 41):
     die Übergröße wird abgestuft bewertet, nicht linear
   - **Bauerwartungsland / Rohbauland** (§ 42): abgestufte Bewertung nach
     Entwicklungszustand
   - **Liquidationsobjekte** (§ 43): nutzungsabhängiger Bodenwert abzüglich
     Freilegungskosten
   - Erschließungsbeiträge: geprüft, ob im Bodenrichtwert enthalten
     (beitragsfrei/beitragspflichtig) – häufige Fehlerquelle

## Rechenbeispiel Eigentumswohnung

```
Bewertungsobjekt: 3-Zi-ETW, 78,4 m² Wofl., Bj. 1996, 2. OG mit Aufzug, Balkon

Vergleichsfälle (Kaufpreissammlung GAA, 2025/2026), auf Stichtag indexiert:
  Fall 1   82,0 m²   279.000 €   3.402 €/m²   → Index +1,5 %  → 3.453 €/m²
  Fall 2   75,5 m²   252.000 €   3.338 €/m²   → Index +2,8 %  → 3.431 €/m²
  Fall 3   79,0 m²   268.000 €   3.392 €/m²   → Index +0,9 %  → 3.423 €/m²
  Fall 4   71,2 m²   248.500 €   3.491 €/m²   → Index +2,1 %  → 3.564 €/m²
  Fall 5   85,3 m²   281.000 €   3.294 €/m²   → Index +1,5 %  → 3.343 €/m²
  Fall 6   76,8 m²   275.000 €   3.581 €/m²   → EG ohne Aufzug, Abschlag -4 %
                                                              → 3.438 €/m²

  Median der angepassten Werte: 3.434 €/m²
  Spanne: 3.343 – 3.564 €/m² (±3 %)

  Vorläufiger Vergleichswert = 3.434 €/m² × 78,4 m² = 269.226 €

boG:
  – Instandhaltungsstau Bad (Kostenschätzung, marktüblich anteilig): –8.000 €
  + überdurchschnittliche Erhaltungsrücklage: nicht angesetzt (im Markt
    regelmäßig nicht preisrelevant, Begründung: …)

  Vergleichswert = 261.226 € → gerundet 261.000 €
  Wertspanne bei Streuung der Vergleichsfälle: 255.000 – 272.000 €
```

## Vorgehen

1. Bodenwert ermitteln (immer, auch wenn ein anderes Verfahren führt)
2. Datenlage prüfen: Liegen Vergleichspreise aus der Kaufpreissammlung vor?
   Wenn nein → Weg B oder anderes Verfahren, und das begründen
3. Vergleichsfälle auswählen und dokumentieren
4. Zeitlich (Indexreihe) und objektbezogen (Umrechnungskoeffizienten,
   begründete Zu-/Abschläge) anpassen
5. Auswerten: Median bzw. Mittelwert, Streuung, Ausreißerbehandlung
6. Vorläufigen Vergleichswert bilden
7. Besondere objektspezifische Grundstücksmerkmale ansetzen und herleiten
8. Ergebnis runden, Kontrollkennzahlen bilden, Spanne angeben

## Regeln

- **Angebotspreise ≠ Kaufpreise.** Portaldaten dienen der Markteinschätzung,
  nie als Vergleichspreis. Wird mangels Alternative damit gearbeitet, ist das
  deutlich zu kennzeichnen und mit einem begründeten Abschlag zu versehen.
- Vergleichsfälle **einzeln dokumentieren**: Datum, Lage (anonymisiert), Fläche,
  Baujahr, Preis, vorgenommene Anpassungen.
- Anpassungen **nachvollziehbar herleiten**, nicht pauschal „–5 % wegen Lage".
- Ausreißer nur mit Begründung entfernen.
- Bei kleiner Fallzahl **Spanne statt Punktwert**.
- Modellkonformität bei Faktoren und Koeffizienten prüfen (§ 10).
- Zeitliche Anpassung nur über offizielle Indexreihen.

## Ausgabeformat

```
## Vergleichswertverfahren
### Datengrundlage (Quelle, Zeitraum, Anzahl Fälle)
### Vergleichsfälle (Tabelle mit Anpassungen)
### Auswertung (Median/Mittel, Streuung, Ausreißerbehandlung)
### Vorläufiger Vergleichswert
### Besondere objektspezifische Grundstücksmerkmale
### Vergleichswert und Wertspanne
```

## Qualitätskontrolle

- [ ] Vergleichspreise aus Kaufpreissammlung, nicht aus Angeboten
- [ ] Fallzahl ausreichend, sonst Spanne und Hinweis
- [ ] Zeitliche Anpassung über Indexreihe belegt
- [ ] Jede objektbezogene Anpassung hergeleitet
- [ ] Ausreißerbehandlung begründet
- [ ] boG separat, nicht in den Vergleichspreisen versteckt
- [ ] €/m² plausibel gegen Markt (siehe `qualitaetssicherung`)
- [ ] Modellkonformität bei Faktoren geprüft

## Grenzen

Gilt für Deutschland. In Österreich (LBG, ÖNORM B 1802) und der Schweiz
(SVKG-Standard, SIA 416) gelten eigene Regelwerke und Flächenbegriffe.
Ohne Zugang zur Kaufpreissammlung ist ein belastbares Vergleichswertverfahren
nicht möglich – das ist dem Auftraggeber mitzuteilen, nicht zu überspielen.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
