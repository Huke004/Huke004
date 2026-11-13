---
name: objektdaten-erfassung
description: Strukturierte Aufnahme eines Bewertungsobjekts – Unterlagenliste, Flächenbegriffe, Zustand, Restnutzungsdauer, Rechte und Lasten, Besichtigungsprotokoll. Erster Schritt jeder Bewertung; nutzen bei Objektaufnahme, Datenerhebung, „was brauche ich für die Bewertung".
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Objektdatenerfassung

## Zweck

Vor jeder Wertermittlung steht die Frage, was überhaupt bewertet wird und auf
welcher Datengrundlage. Dieser Skill definiert die Mindestdaten, die
Unterlagenliste und die typischen Stolperfallen bei Flächen und Zustand.

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

Immer als erster Schritt eines Bewertungsauftrags, und wenn der Nutzer nach
benötigten Unterlagen fragt.

## Die vier Pflichtangaben

Ohne diese vier wird nicht gerechnet:

1. **Wertermittlungsobjekt** – was genau? Grundstück, Gebäude, Miteigentums-
   anteil, Erbbaurecht, Teilfläche? Grundbuchbezeichnung.
2. **Wertermittlungsstichtag** – Zeitpunkt, auf den sich die allgemeinen
   Wertverhältnisse beziehen. Getrennt davon der **Qualitätsstichtag** (Zustand
   des Grundstücks), der bei rückwirkenden Bewertungen abweichen kann.
3. **Wertbegriff** – Verkehrswert (§ 194 BauGB) / Marktwert, Beleihungswert,
   Kaufpreisindikation, Versicherungswert. Nicht dasselbe, nicht austauschbar.
4. **Zweck** – Kauf/Verkauf, Finanzierung, Erbauseinandersetzung, Scheidung,
   Steuer, Gericht. Der Zweck bestimmt Tiefe, Form und Freigabestufe.

## Unterlagenliste

### Immer

- Aktueller Grundbuchauszug (alle drei Abteilungen), nicht älter als 3 Monate
- Flurkarte / Liegenschaftskarte
- Bauzeichnungen (Grundrisse, Schnitte, Ansichten)
- Wohn-/Nutzflächenberechnung mit Angabe der Rechtsgrundlage
- Baujahr, Modernisierungsnachweise (Rechnungen, Jahr, Gewerk)
- Energieausweis
- Auskunft Baulastenverzeichnis (nicht in allen Bundesländern geführt)
- Auskunft Altlastenkataster
- Bebauungsplan / Bauauskunft (§ 34/§ 35 BauGB), Denkmalschutzstatus
- Grundsteuerbescheid, Erschließungsstand

### Bei Eigentumswohnungen zusätzlich

- Teilungserklärung mit Gemeinschaftsordnung und Aufteilungsplan
- Abgeschlossenheitsbescheinigung
- Protokolle der Eigentümerversammlungen der letzten 3 Jahre
- Wirtschaftspläne und Jahresabrechnungen der letzten 3 Jahre
- Stand der Erhaltungsrücklage, beschlossene und absehbare Sonderumlagen
- Verwaltervertrag, Beschlusssammlung

### Bei vermieteten Objekten zusätzlich

- Mietverträge oder Mieterliste (siehe `mieterliste.schema.json`)
- Nebenkostenabrechnungen der letzten 2 Jahre
- Aufstellung Instandhaltungsaufwand der letzten 5 Jahre
- Leerstandsflächen und -dauer

### Bei Erbbaurecht zusätzlich

- Erbbaurechtsvertrag, Erbbauzins, Anpassungsklausel, Restlaufzeit,
  Heimfallregelung, Entschädigungsregelung

## Flächenbegriffe – der häufigste Fehler

| Begriff | Grundlage | Was zählt |
|---|---|---|
| **Wohnfläche** (DE) | WoFlV | Wohnräume; Balkon/Terrasse i. d. R. zu 25 %, max. 50 %; Räume unter 1 m Höhe zählen nicht, 1–2 m zur Hälfte |
| **Wohnfläche (alt)** | II. BV | ältere Verträge – abweichende Anrechnung |
| **Nutzfläche / BGF / NGF** | DIN 277 | für Gewerbe und Sachwertverfahren; BGF ist Außenmaß aller Geschosse |
| **Nutzfläche AT** | ÖNORM B 1800 | eigene Anrechnungsregeln |
| **Fläche CH** | SIA 416 | GF, HNF, NF – nicht mit BGF gleichsetzen |

**Regeln:**

- Jede Flächenangabe bekommt ihre Grundlage. „142 m²" ohne Basis ist unbrauchbar.
- Das Sachwertverfahren rechnet mit **BGF**, das Vergleichswertverfahren bei
  Wohnnutzung meist mit **Wohnfläche**. Nicht vermischen.
- Weicht die Angabe des Verkäufers von der Berechnung ab: Berechnung nutzen,
  Abweichung ausweisen. Bei > 3 % Abweichung Nachweis anfordern.
- Bei Eigentumswohnungen: Miteigentumsanteil ≠ Wohnflächenanteil.

## Alter, Gesamt- und Restnutzungsdauer

Nach ImmoWertV 2021 (§ 4, Anlagen 1 und 2):

- **Gesamtnutzungsdauer (GND)** nach Anlage 1 modellhaft je Gebäudeart
  (freistehende Ein-/Zweifamilienhäuser und Mehrfamilienhäuser: 80 Jahre;
  andere Gebäudearten abweichend – Anlage 1 heranziehen, nicht schätzen).
- **Restnutzungsdauer (RND)** = GND ./. Alter, verlängert um den Effekt
  wesentlicher Modernisierungen.
- Für Modernisierungen enthält **Anlage 2** ein Punktemodell: Modernisierungs-
  elemente (u. a. Dach, Fenster, Leitungen, Heizung, Wärmedämmung, Bäder,
  Innenausbau, Grundriss) werden bepunktet, daraus folgt der Modernisierungsgrad
  und daraus eine modifizierte RND.
- Bei durchgreifender Sanierung („Kernsanierung") kann die RND neu ansetzen –
  das ist begründungspflichtig und braucht Belege.
- RND wird **nicht frei geschätzt.** Der Ansatz wird hergeleitet und belegt.

> Achtung Modellkonformität (§ 10 ImmoWertV): Marktdaten wie Liegenschaftszins-
> sätze und Sachwertfaktoren gelten nur in dem Modell, in dem der
> Gutachterausschuss sie abgeleitet hat. Wer sie verwendet, muss GND, RND,
> Bewirtschaftungskosten und Flächenbegriffe **genauso** ansetzen wie dort.
> Ein „besserer" eigener Ansatz macht die abgeleiteten Daten unbrauchbar.

## Rechte und Lasten

- **Abteilung II** (Dienstbarkeiten, Wohnrechte, Nießbrauch, Vorkaufsrechte,
  Reallasten, Erbbaurecht, Sanierungsvermerk) – meist wertrelevant
- **Abteilung III** (Grundpfandrechte) – für den Verkehrswert grundsätzlich
  **nicht** wertmindernd, da sie beim Verkauf abgelöst werden
- **Baulasten** stehen nicht im Grundbuch, sondern im Baulastenverzeichnis
- Gerötete (durchgestrichene) Grundbucheinträge sind gelöscht und werden nicht
  als bestehende Rechte übernommen

Jedes Recht bekommt eine Einschätzung: wertmindernd / werterhöhend / neutral /
unklar – und, wenn möglich, eine Bezifferung (ImmoWertV Teil 4 Abschnitt 2).

## Besichtigung

Wird besichtigt, gehört ins Protokoll: Datum, Wetter, anwesende Personen,
Umfang (innen/außen, alle Einheiten?), Fotodokumentation, festgestellte Schäden
und Instandhaltungsstau, Eindruck von Lage und Umfeld.

Wird **nicht** besichtigt, ist das im Ergebnis ausdrücklich zu vermerken – es
begrenzt die Aussagekraft erheblich.

## Vorgehen

1. Vier Pflichtangaben klären
2. Unterlagen anfordern bzw. vorhandene auswerten – je Angabe mit Dokument,
   Fundstelle und Stand
3. Objektdatensatz nach `objekt.schema.json` füllen
4. Lücken- und Widerspruchsliste erzeugen
5. Verfahrenswahl vorbereiten (siehe unten)

## Verfahrenswahl

| Objekt | führendes Verfahren | stützend |
|---|---|---|
| Eigentumswohnung | Vergleichswert | Ertragswert (wenn vermietet) |
| Reihenhaus, DHH in homogener Lage | Vergleichswert | Sachwert |
| Freistehendes EFH | Sachwert oder Vergleichswert (je Datenlage) | jeweils das andere |
| Mehrfamilienhaus | Ertragswert | Sachwert |
| Wohn-/Geschäftshaus, Gewerbe | Ertragswert / DCF | Vergleichswert je m² |
| Unbebautes Grundstück | Vergleichswert (Bodenrichtwert) | Residualwert bei Entwicklung |
| Spezialimmobilie ohne Markt | Sachwert | Liquidationswert |

Mehrere Verfahren sind der Regelfall. Die Gewichtung wird begründet, nicht
gemittelt.

## Regeln

- Ohne die vier Pflichtangaben wird nicht gerechnet.
- Jede Flächenangabe trägt ihre Rechtsgrundlage; Wohnfläche und BGF werden
  nie gleichgesetzt oder ineinander umgerechnet, ohne das zu kennzeichnen.
- GND und RND werden nach Anlage 1 und Anlage 2 hergeleitet, nicht geschätzt.
- Modellkonformität (§ 10 ImmoWertV) wird vor der Verfahrenswahl geprüft:
  Wer Daten des Gutachterausschusses nutzt, übernimmt dessen Modellannahmen.
- Abteilung III mindert den Verkehrswert grundsätzlich nicht; Abteilung II und
  Baulasten werden einzeln bewertet.
- Gerötete Grundbucheinträge sind gelöscht und werden nicht übernommen.
- Fehlt eine Unterlage, wird das benannt – mit der Auswirkung auf das Ergebnis,
  nicht durch eine stille Annahme ersetzt.
- Ohne Ortsbesichtigung wird das im Ergebnis vermerkt.

## Ausgabeformat

```
## Bewertungsobjekt
Grundbuch <…>, Flur <…>, Flurstück <…>, <Adresse>
Objektart · Baujahr · Grundstück <…> m² · Wohnfläche <…> m² (WoFlV)

## Auftragsrahmen
Stichtag · Qualitätsstichtag · Wertbegriff · Zweck · Besichtigung ja/nein

## Datengrundlage
(Tabelle: Größe | Wert | Quelle | Stand | Vertrauen)

## Fehlende Unterlagen
(mit Auswirkung auf das Ergebnis)

## Widersprüche
## Vorgeschlagene Verfahren mit Begründung
```

## Qualitätskontrolle

- [ ] Vier Pflichtangaben geklärt
- [ ] Jede Flächenangabe mit Rechtsgrundlage
- [ ] GND/RND nach Anlage 1/2 hergeleitet, nicht geschätzt
- [ ] Modellkonformität mit den verwendeten Marktdaten geprüft
- [ ] Abt. II und Baulasten ausgewertet, Abt. III korrekt behandelt
- [ ] Besichtigungsstatus dokumentiert
- [ ] Fehlende Unterlagen mit Auswirkung benannt

## Grenzen

Keine Bauzustandsbeurteilung (Bausachverständiger), keine Schadensbewertung,
keine Prüfung der Standsicherheit. Die Durchführung der Wertermittlungs-
verfahren selbst ist nicht Gegenstand dieser Datei.

## Anhang: Objektaufnahmebogen

Vorlage für die strukturierte Objektaufnahme – als Checkliste im Gespräch oder
als Gerüst für ein Word-Dokument. Jede Zeile bekommt neben dem Wert die
**Quelle** und den **Stand**. Unbekanntes bleibt leer und wandert in die Liste
der fehlenden Unterlagen; es wird nicht geschätzt.

#### 0 Auftragsrahmen

| Feld | Wert | Quelle |
|---|---|---|
| Vorgangsnummer | | |
| Auftraggeber | | |
| Wertermittlungsstichtag | | |
| Qualitätsstichtag | | |
| Wertbegriff | Verkehrswert / Beleihungswert / Kaufpreisindikation | |
| Zweck | | |
| Ortsbesichtigung | ja/nein, Datum, Umfang | |

#### 1 Identifikation

| Feld | Wert | Quelle |
|---|---|---|
| Adresse | | |
| Amtsgericht / Grundbuch von / Blatt | | Grundbuchauszug |
| Gemarkung / Flur / Flurstück | | |
| Grundstücksfläche (m²) | | Grundbuch / Katasterauszug |
| Objektart | | |
| Bei ETW: Miteigentumsanteil | | Teilungserklärung |
| Sondernutzungsrechte | | Teilungserklärung |

#### 2 Gebäude

| Feld | Wert | Quelle |
|---|---|---|
| Baujahr | | |
| Gebäudeart / Bauweise | | |
| Geschosse, Keller, Dachgeschoss | | |
| Wohnfläche (m²) + Rechtsgrundlage | | Wohnflächenberechnung |
| Nutzfläche (m²) | | |
| Bruttogrundfläche (m² DIN 277) | | Bauzeichnung |
| Zimmerzahl | | |
| Stellplätze (Art, Anzahl) | | |
| Gesamtnutzungsdauer (Anlage 1) | | |
| Restnutzungsdauer (Anlage 2, Herleitung) | | |

##### Modernisierungen

| Jahr | Gewerk | Umfang | Beleg |
|---|---|---|---|
| | Dach | | |
| | Fassade / Dämmung | | |
| | Fenster | | |
| | Heizung | | |
| | Leitungen (Wasser, Abwasser, Elektro) | | |
| | Bäder | | |
| | Innenausbau / Böden | | |
| | Grundriss | | |

##### Zustand und Mängel

| Bauteil | Zustand | Festgestellte Mängel | Geschätzter Aufwand |
|---|---|---|---|

#### 3 Energie

| Feld | Wert | Quelle |
|---|---|---|
| Ausweisart (Bedarf/Verbrauch) | | Energieausweis |
| Kennwert kWh/(m²·a) | | |
| Effizienzklasse | | |
| Energieträger | | |
| Heizungsart, Baujahr | | |
| Ausstellung / gültig bis / Reg.-Nr. | | |

#### 4 Recht und Planung

| Feld | Wert | Quelle |
|---|---|---|
| Abt. II – Lasten und Beschränkungen (lfd. Nr., Inhalt, Rang) | | Grundbuch + Bewilligung |
| Abt. III – Grundpfandrechte | | Grundbuch |
| Baulasten | | Baulastenverzeichnis |
| Altlasten / Altlastenverdacht | | Altlastenkataster |
| Denkmalschutz | | Denkmalliste |
| Planungsrecht (B-Plan / § 34 / § 35) | | Bauaufsicht |
| GRZ / GFZ / zulässige Nutzung | | |
| Erschließung, Beitragsstand | | Gemeinde |
| Erbbaurecht (Zins, Restlaufzeit, Heimfall, Entschädigung) | | Erbbaurechtsvertrag |

#### 5 Nutzung und Erträge

| Einheit | Nutzung | Fläche m² | Nettokaltmiete/Monat | €/m² | Vertragsbeginn | Anpassung | Bemerkung |
|---|---|---|---|---|---|---|---|

| Feld | Wert |
|---|---|
| Jahresnettokaltmiete Ist | |
| Jahresnettokaltmiete marktüblich | |
| Leerstand (Fläche, Dauer) | |

#### 6 Bei Eigentumswohnungen

| Feld | Wert | Quelle |
|---|---|---|
| Anzahl Einheiten in der WEG | | Teilungserklärung |
| Hausgeld / Monat, davon nicht umlagefähig | | Wirtschaftsplan |
| Erhaltungsrücklage (Stand, €/m²) | | Jahresabrechnung |
| Beschlossene Maßnahmen / Sonderumlagen | | Beschlusssammlung |
| Nutzungsbeschränkungen | | Gemeinschaftsordnung |

#### 7 Marktdaten

| Feld | Wert | Quelle | Stand |
|---|---|---|---|
| Bodenrichtwert (€/m², Zone) | | | |
| Merkmale des Bodenrichtwertgrundstücks | | | |
| Liegenschaftszinssatz | | | |
| Sachwertfaktor | | | |
| Vergleichs-/Umrechnungsfaktoren | | | |
| Indexreihe | | | |

#### 8 Offene Punkte

##### Fehlende Unterlagen
- … (benötigt für …)

##### Widersprüche
- … (Quelle A: … / Quelle B: … → maßgeblich: … weil …)

##### Annahmen
- …

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
