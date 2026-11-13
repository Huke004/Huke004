---
name: bewertung-oesterreich-schweiz
description: Immobilienbewertung in Österreich (LBG, ÖNORM B 1802) und der Schweiz (SVKG/SEK-SVIT, DCF, SIA) – Verfahren, Begriffe, Datenquellen und Unterschiede zum deutschen Recht. Nutzen bei Objekten in AT oder CH oder wenn nach österreichischen bzw. Schweizer Standards gefragt wird.
version: 2.0.0
stand: 2026-09
geltungsbereich: [AT, CH]
---

# Bewertung in Österreich und der Schweiz

## Zweck

Die drei DACH-Länder rechnen ähnlich und regeln unterschiedlich. Wer deutsche
ImmoWertV-Begriffe auf ein Wiener oder Zürcher Objekt anwendet, produziert
formal falsche Gutachten. Dieser Skill markiert die Unterschiede.

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

Sobald das Objekt in Österreich oder der Schweiz liegt oder der Auftraggeber
nach diesen Standards fragt.

**Erste Handlung:** Land klären. Danach Bundesland bzw. Kanton – beide Länder
regeln vieles subnational.

---

## Österreich

### Rechtsrahmen

- **Liegenschaftsbewertungsgesetz (LBG)** – der gesetzliche Rahmen für die
  Bewertung von Liegenschaften, insbesondere in gerichtlichen Verfahren
- **ÖNORM B 1802 ff.** – technische Regeln der Liegenschaftsbewertung;
  B 1802-1 zum Sachwertverfahren, weitere Teile zu den übrigen Verfahren
- **ÖNORM B 1800** – Flächenermittlung (nicht WoFlV, nicht DIN 277!)
- Ergänzend: Bewertungsgesetz für steuerliche Zwecke, Grundbuchsgesetz

### Verfahren

Dieselbe Trias, andere Bezeichnungen und Details:

| Verfahren | Besonderheit AT |
|---|---|
| **Vergleichswertverfahren** | nach LBG grundsätzlich vorrangig, wenn ausreichend Vergleichsdaten vorliegen |
| **Ertragswertverfahren** | Kapitalisierung des nachhaltigen Reinertrags; Kapitalisierungszinssatz statt „Liegenschaftszinssatz"; Bodenwertverzinsung analog |
| **Sachwertverfahren** | Bodenwert + Bauwert (Herstellungswert abzüglich Wertminderung wegen Alters) + Außenanlagen; Marktanpassung über Marktanpassungsfaktor |

### Begriffliche Fallen

| Deutschland | Österreich |
|---|---|
| Verkehrswert (§ 194 BauGB) | Verkehrswert nach LBG – ähnliche Definition, eigene Rechtsgrundlage |
| Wohnfläche nach WoFlV | Nutzfläche nach ÖNORM B 1800 / MRG – andere Anrechnung |
| Bodenrichtwert | keine flächendeckenden amtlichen Bodenrichtwerte in gleicher Form; Ableitung aus Kaufpreissammlung und Immobilienpreisspiegel |
| Gutachterausschuss | kein Pendant; Datenbeschaffung über Grundbuch/Kaufpreissammlung und Verbandsstatistiken |
| ImmoWertV-Anlagen (GND, NHK) | ÖNORM-Ansätze und Baukostenkennwerte |

### Datenquellen

- Grundbuch und Grundstücksdatenbank (BEV) – auch für Kaufpreise
- Immobilienpreisspiegel der Wirtschaftskammer
- Flächenwidmungs- und Bebauungsplan der Gemeinde
- Richtwerte nach dem Richtwertgesetz (je Bundesland) für Mietrecht im
  Anwendungsbereich des MRG

### Mietrechtliche Besonderheit mit Wertfolge

Im Vollanwendungsbereich des **MRG** sind Mieten durch Richtwert- bzw.
Kategoriemietzins begrenzt. Das begrenzt den nachhaltigen Rohertrag und ist im
Ertragswertverfahren zwingend zu berücksichtigen – die erzielbare Miete ist
dort nicht die Marktmiete.

---

## Schweiz

### Rechtsrahmen

- Kein Bundesgesetz zur Verkehrswertermittlung wie ImmoWertV oder LBG
- Maßgeblich sind **Branchenstandards**: der Schweizer Bewertungsstandard
  (SVKG/SEK-SVIT), ergänzend internationale Standards (IVS, RICS) im
  institutionellen Bereich
- **SIA-Normen** für Flächen und Baukosten, insbesondere **SIA 416**
  (Flächen und Volumen) und SIA 416/1 (Kennzahlen)
- Grundbuch und Bewertung sind **kantonal** organisiert

### Verfahren

| Verfahren | Anwendung CH |
|---|---|
| **DCF** | Standard bei Rendite- und institutionellen Objekten; explizite Cashflow-Planung, Diskontierungs- und Kapitalisierungssatz getrennt |
| **Vergleichs-/hedonische Modelle** | verbreitet bei Wohneigentum (EFH, Stockwerkeigentum), statistisch gestützt |
| **Realwert** | Landwert + Zeitbauwert + Umgebung; entspricht in etwa dem Sachwert |
| **Ertragswert** | Kapitalisierung des Nettoertrags |
| **Mischwert** | gewichtete Kombination aus Real- und Ertragswert, bei Banken verbreitet – Gewichtung ist bankspezifisch |

### Begriffliche Fallen

| Deutschland | Schweiz |
|---|---|
| Eigentumswohnung | **Stockwerkeigentum** mit Wertquote |
| Wohnfläche | Flächen nach SIA 416 (GF, HNF, NF) – nicht gleichzusetzen |
| Grundbuchamt bundesweit einheitlich | kantonal, teilweise unterschiedliche Registerpraxis |
| Bodenrichtwert | keine amtlichen Bodenrichtwerte; Landwert aus Vergleich oder Residualmethode |
| Verkehrswert | Marktwert / Verkehrswert; daneben **amtlicher Wert / Steuerwert**, der deutlich abweicht und keine Marktaussage ist |

### Datenquellen

- Kantonale Grundbuchämter, Handänderungsstatistiken
- Bundesamt für Statistik (BFS), kantonale Statistikstellen
- Marktindizes privater Anbieter (Wüest Partner, IAZI, FPRE)
- Bau- und Zonenordnung der Gemeinde

### Steuer- und Nebenkostenrahmen

Handänderungssteuer, Grundstückgewinnsteuer und Eigenmietwert sind kantonal
sehr unterschiedlich und für Investitionsrechnungen relevant. Sie sind
kantonal zu recherchieren, nie zu schätzen.

---

## Vorgehen

1. Land und Kanton/Bundesland feststellen
2. Passenden Standard wählen und **im Gutachten benennen**
3. Flächenbegriff des jeweiligen Landes verwenden – und die Rechtsgrundlage
   angeben
4. Datenquellen des jeweiligen Landes nutzen (siehe Tabellen oben)
5. Bei grenzüberschreitendem Vergleich: Unterschiede der Verfahren
   ausdrücklich benennen, keine Zahlen ohne Umrechnung der Bezugsgrößen
   gegenüberstellen

## Regeln

- **Keine ImmoWertV-Paragraphen auf AT/CH-Objekte anwenden.** Kein „§ 194 BauGB"
  in einem Schweizer Gutachten.
- Flächen niemals zwischen WoFlV, ÖNORM B 1800 und SIA 416 gleichsetzen.
- Der Schweizer **amtliche Wert** ist kein Marktwert – Verwechslung führt zu
  gravierenden Fehlern.
- Bei AT-Objekten im MRG-Vollanwendungsbereich die Mietzinsbeschränkung prüfen.
- Kantonale und bundeslandspezifische Regeln immer recherchieren, nie aus der
  Nachbarregion übertragen.
- Währung CHF nicht mit EUR mischen; Umrechnungskurs mit Datum angeben.

## Qualitätskontrolle

- [ ] Land und Kanton/Bundesland festgestellt
- [ ] Angewandter Standard im Dokument benannt
- [ ] Flächenbegriff korrekt und mit Rechtsgrundlage
- [ ] Keine deutschen Rechtsnormen auf AT/CH übertragen
- [ ] Datenquellen des jeweiligen Landes verwendet
- [ ] Währung und ggf. Umrechnung sauber ausgewiesen

## Grenzen

Dieser Skill gibt einen strukturellen Überblick, keine vollständige Darstellung
der beiden Rechtsordnungen. Für Gutachten in AT/CH ist eine im jeweiligen Land
qualifizierte Person einzubinden. Der
konkrete Normtext von LBG, ÖNORM und SVKG-Standard ist zu beschaffen; er wird
hier nicht wiedergegeben.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
