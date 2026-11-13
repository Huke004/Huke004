---
name: steuern-und-afa
description: Steuerliche Grundlagen bei Immobilien – Abschreibung (lineare, degressive und Sonder-AfA), Kaufpreisaufteilung, Werbungskosten, Spekulationsfrist, Grunderwerbsteuer, Grundsteuer, Erbschaft- und Schenkungsteuer. Nutzen bei Steuer, AfA, Abschreibung, Spekulationsfrist, Kaufpreisaufteilung, Erbschaft, Grundsteuer.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE]
---

# Steuern und AfA bei Immobilien

> **Keine Steuerberatung.** Der Agent stellt Strukturen und Größenordnungen
> dar, damit der Nutzer die richtigen Fragen stellen kann. Jede konkrete
> Gestaltung gehört zum Steuerberater.
> Steuersätze und Fristen werden **recherchiert**, nicht erinnert.

## Zweck

Steuern entscheiden über die Nachsteuerrendite einer Immobilie und über die
Struktur von Kauf, Halten und Verkauf. Dieser Skill ordnet die Themen und
markiert, wo Beratungsbedarf entsteht.

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

- Fragen zu Abschreibung, Werbungskosten, Kaufpreisaufteilung
- Verkaufsüberlegungen und Haltefristen
- Nebenkostenkalkulation (Grunderwerbsteuer)
- Übertragung, Erbfall, Schenkung
- Grundsteuer nach der Reform

## Abschreibung (AfA) auf Gebäude – Stand 2026

Abgeschrieben wird nur das **Gebäude**, nie der Grund und Boden.

| Fall | Satz | Bemerkung |
|---|---|---|
| Wohngebäude, Fertigstellung vor 1925 | 2,5 % linear | 40 Jahre |
| Wohngebäude, Fertigstellung 1925 bis 2022 | 2,0 % linear | 50 Jahre |
| Wohngebäude, Fertigstellung ab 01.01.2023 | 3,0 % linear | 33 Jahre |
| Betriebsgebäude im Betriebsvermögen (Bauantrag nach 31.03.1985) | 3,0 % linear | |
| **Degressive AfA** für neue Wohngebäude | 5 % vom jeweiligen Restwert | Baubeginn bzw. Erwerb im Zeitraum 01.10.2023 bis 30.09.2029; Wechsel zur linearen AfA möglich |
| **Sonder-AfA § 7b EStG** für neuen Mietwohnraum | zusätzlich 5 % p. a. über 4 Jahre | an Effizienzanforderungen (EH40/QNG) und Baukostengrenzen gebunden |
| **Denkmal-AfA §§ 7h/7i EStG** | 9 % über 8 Jahre, dann 7 % über 4 Jahre | nur auf begünstigte Sanierungskosten, Bescheinigung der Denkmalbehörde erforderlich |
| Kürzere tatsächliche Nutzungsdauer | nach Nachweis | Gutachten erforderlich; die Anforderungen sind streng |

Voraussetzungen, Fristen und Grenzen dieser Regelungen ändern sich häufig –
**vor jeder Aussage den aktuellen Stand prüfen und datieren.**

## Kaufpreisaufteilung

Die Aufteilung des Kaufpreises auf Grund und Boden, Gebäude und Inventar
bestimmt die AfA-Bemessungsgrundlage und damit über Jahrzehnte die
Steuerwirkung.

- Eine im Kaufvertrag vereinbarte Aufteilung wird von der Finanzverwaltung
  grundsätzlich anerkannt, wenn sie wirtschaftlich vernünftig und nicht
  offensichtlich unzutreffend ist
- Andernfalls greift die Aufteilung nach dem Verhältnis der Verkehrswerte;
  die Finanzverwaltung stellt dafür eine Arbeitshilfe bereit, die der BFH
  jedoch nicht als allein maßgeblich ansieht – ein **Sachverständigengutachten
  zur Aufteilung** ist der belastbarere Weg
- Ein hoher Bodenanteil (teure Lage) senkt die AfA erheblich
- Inventar (Küche, Möbel) gesondert und realistisch ausweisen: kürzere
  Abschreibungsdauer und keine Grunderwerbsteuer auf diesen Teil

**Hier liegt der größte Hebel** – und ein häufiges Feld für Beanstandungen.
Der Agent bereitet die Aufteilung nachvollziehbar vor, die Abstimmung erfolgt
mit dem Steuerberater.

## Werbungskosten bei Vermietung

Sofort abziehbar: Zinsen (nicht die Tilgung), Verwaltungskosten,
Erhaltungsaufwand, Grundsteuer, Versicherungen, nicht umlegbare
Betriebskosten, Fahrtkosten, Kontoführung, Steuerberatung für die Anlage V.

Abzugrenzen:

- **Erhaltungsaufwand** (sofort abziehbar) vs. **Herstellungskosten** (nur
  über die AfA)
- **Anschaffungsnahe Herstellungskosten** (§ 6 Abs. 1 Nr. 1a EStG): Übersteigen
  Instandsetzungs- und Modernisierungsaufwendungen innerhalb von **drei Jahren
  nach Anschaffung 15 % der Anschaffungskosten des Gebäudes** (ohne USt), gelten
  sie als Herstellungskosten und sind nur abzuschreiben. Die klassische Falle
  beim „Sanieren nach Kauf".
- Größerer Erhaltungsaufwand kann auf zwei bis fünf Jahre verteilt werden

## Veräußerung

- **Private Veräußerungsgeschäfte (§ 23 EStG):** Gewinne aus dem Verkauf von
  Immobilien im Privatvermögen sind steuerpflichtig, wenn zwischen Anschaffung
  und Veräußerung **nicht mehr als zehn Jahre** liegen
- **Ausnahme Eigennutzung:** steuerfrei bei Nutzung zu eigenen Wohnzwecken im
  Zeitraum zwischen Anschaffung/Fertigstellung und Veräußerung oder in den
  beiden vorangegangenen Kalenderjahren zuzüglich des Veräußerungsjahres
- **Gewerblicher Grundstückshandel:** Wer innerhalb von etwa fünf Jahren mehr
  als drei Objekte veräußert, gerät regelmäßig in den gewerblichen
  Grundstückshandel – mit Gewerbesteuer, Bilanzierungspflichten und Wegfall
  der Zehnjahresfrist. Die „Drei-Objekt-Grenze" ist eine Indizregel der
  Rechtsprechung, keine feste Norm.
- Bei degressiver AfA und Sonder-AfA: die in Anspruch genommene Abschreibung
  erhöht den steuerpflichtigen Veräußerungsgewinn innerhalb der Frist

## Erwerbs- und laufende Steuern

- **Grunderwerbsteuer:** Landessteuer, Sätze zwischen 3,5 % und 6,5 % je
  Bundesland – Satz immer recherchieren. Bemessungsgrundlage ist die
  Gegenleistung; gesondert ausgewiesenes Inventar mindert sie.
- **Grundsteuer:** seit 2025 auf Basis der reformierten Bewertung; Bundesmodell
  und abweichende Ländermodelle, Hebesätze der Gemeinden. Belastungen können
  sich gegenüber der alten Rechtslage deutlich verschoben haben – für
  Kalkulationen den konkreten Bescheid heranziehen, nicht schätzen.
- **Umsatzsteuer:** Wohnraumvermietung ist umsatzsteuerfrei; bei
  Gewerbevermietung kann zur Umsatzsteuer optiert werden, was den
  Vorsteuerabzug ermöglicht und einen Berichtigungszeitraum von zehn Jahren
  auslöst.

## Übertragung, Erbschaft und Schenkung

- Bewertung des Grundbesitzes für Erbschaft- und Schenkungsteuer erfolgt nach
  dem **Bewertungsgesetz** (typisierte Vergleichs-, Ertrags- und
  Sachwertverfahren) – dieser Steuerwert ist **nicht der Verkehrswert**
- Ein **Verkehrswertgutachten** kann als Nachweis eines niedrigeren gemeinen
  Werts dienen (§ 198 BewG) – ein häufiger und sinnvoller Auftragsanlass
- Persönliche Freibeträge sind vom Verwandtschaftsgrad abhängig und alle zehn
  Jahre erneut nutzbar; Begünstigungen für vermietete Wohnimmobilien und das
  Familienheim beachten
- Vorbehaltsnießbrauch mindert den Steuerwert und ist ein gängiges
  Gestaltungsmittel – Gestaltung nur mit Steuerberater und Notar

## Vorgehen

1. Sachverhalt einordnen: Privatvermögen oder Betriebsvermögen? Eigennutzung
   oder Vermietung? Erwerb, Halten oder Veräußerung?
2. Relevante Regelungen benennen und **Stand recherchieren**
3. Größenordnung rechnen, ausdrücklich als überschlägig gekennzeichnet
4. Gestaltungsfragen auflisten, die der Steuerberater klären muss
5. Fristen benennen (Zehnjahresfrist, Dreijahresfrist, Zehnjahresfrist bei
   Schenkungen) mit dem Hinweis, dass ihre Überwachung nicht beim Agenten liegt

## Regeln

- Keine Sätze, Freibeträge oder Fristen aus dem Gedächtnis. Recherchieren,
  Quelle und Datum nennen.
- Keine Steuergestaltung empfehlen; Optionen darstellen und die Prüfung
  zuweisen.
- Nachsteuerrechnungen immer mit dem individuellen Steuersatz als Annahme
  kennzeichnen.
- Steuerwert, Verkehrswert und Kaufpreis sauber auseinanderhalten.
- Keine Aussagen zu Modellen, die auf Steuervermeidung durch unzutreffende
  Sachverhaltsdarstellung hinauslaufen (z. B. überhöhter Inventaranteil).

## Ausgabeformat

```
## Steuerliche Einordnung
Sachverhalt · Vermögenssphäre · Nutzung

## Einschlägige Regelungen
| Thema | Regelung | Stand geprüft am | Quelle |

## Überschlägige Wirkung
(Rechnung mit gekennzeichneten Annahmen)

## Fristen

## Für den Steuerberater
- offene Frage 1
- offene Frage 2
```

## Qualitätskontrolle

- [ ] Alle Sätze, Fristen und Beträge recherchiert und datiert
- [ ] Grund und Boden nicht abgeschrieben
- [ ] Kaufpreisaufteilung thematisiert, wo relevant
- [ ] 15-%-Grenze bei Sanierung nach Kauf geprüft
- [ ] Zehnjahresfrist und Eigennutzungsausnahme korrekt dargestellt
- [ ] Grunderwerbsteuersatz des richtigen Bundeslands
- [ ] Steuerwert ≠ Verkehrswert klargestellt
- [ ] Verweis auf Steuerberater enthalten

## Grenzen

Keine Steuerberatung im Sinne des Steuerberatungsgesetzes. Keine Erstellung
von Steuererklärungen, keine verbindlichen Auskünfte, keine Gestaltungs-
beratung. Gilt für Deutschland; AT und CH haben grundlegend andere Systeme
(u. a. Immobilienertragsteuer in Österreich, Grundstückgewinnsteuer und
Eigenmietwert in der Schweiz).

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
