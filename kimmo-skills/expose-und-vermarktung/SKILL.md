---
name: expose-und-vermarktung
description: Exposés und Objektinserate erstellen und veröffentlichen – Aufbau, Textbausteine, Pflichtangaben nach GEG, Bildrechte, Portalveröffentlichung (OpenImmo), Provisionsrecht und Widerrufsbelehrung. Nutzen bei Exposé, Objektbeschreibung, Verkaufstext, Inserat, Portal, Vermarktung, Provision.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Exposé und Vermarktung

## Zweck

Das Exposé entscheidet, ob ein Objekt besichtigt wird. Es ist zugleich ein
rechtlich aufgeladenes Dokument: Falschangaben können Gewährleistungsansprüche
auslösen, fehlende Pflichtangaben Bußgelder.

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

- Exposé, Objektbeschreibung, Verkaufs- oder Vermietungstext
- Portalinserat, Zeitungsanzeige, Social-Media-Post zu einem Objekt
- Fragen zu Provision, Widerruf, Pflichtangaben in Anzeigen

## Aufbau eines Exposés

```
1  Titelseite      Foto, Objekttyp, Lage, Preis, Objektnummer
2  Kurzprofil      Eckdaten-Tabelle (siehe unten)
3  Objekt          Beschreibung Gebäude, Grundriss, Zustand, Modernisierungen
4  Ausstattung     Küche, Bäder, Böden, Heizung, Fenster, Smart Home, Stellplätze
5  Lage            Makro und Mikro (siehe marktanalyse-lage)
6  Energie         Pflichtangaben (siehe unten)
7  Grundrisse      mit Maßstabsangabe und Hinweis „nicht maßstabsgetreu"
8  Fotos           mit Aufnahmedatum
9  Kaufnebenkosten / Mietnebenkosten, Verfügbarkeit
10 Provision und Widerrufsbelehrung
11 Anbieter, Kontakt
12 Haftungshinweis
```

### Eckdaten-Tabelle

| Angabe | Hinweis |
|---|---|
| Objektart, Baujahr | |
| Wohn-/Nutzfläche | mit Rechtsgrundlage (WoFlV / ÖNORM / SIA) |
| Grundstücksfläche | |
| Zimmer, Etage, Aufzug | |
| Zustand, letzte Modernisierung | |
| Heizungsart, Energieträger | |
| Stellplätze | Art und Anzahl |
| Verfügbarkeit | Datum oder „nach Vereinbarung" |
| Kaufpreis / Miete + Nebenkosten | |
| Provision | Höhe, inkl. USt, wer zahlt |

## Pflichtangaben in Immobilienanzeigen (Deutschland, GEG)

Liegt ein Energieausweis vor, müssen kommerzielle Immobilienanzeigen unter
anderem enthalten:

- Art des Energieausweises (Bedarfs- oder Verbrauchsausweis)
- der End­energiebedarf bzw. Energieverbrauchskennwert
- wesentlicher Energieträger der Heizung
- Baujahr des Gebäudes laut Ausweis
- Energieeffizienzklasse

Fehlen die Angaben, droht ein Bußgeld. Ausnahmen (u. a. Baudenkmäler) sind zu
prüfen und im Zweifel zu benennen.

**Rechtsstand-Warnung:** Der Katalog der Pflichtangaben ändert sich mit der
laufenden GEG-Anpassung zur Umsetzung der EU-Gebäuderichtlinie (EPBD). Die
EU-Umsetzungsfrist lief am 29.05.2026 ab, die deutsche Novelle war zu diesem
Zeitpunkt noch nicht in Kraft. Den geltenden Stand vor jeder Veröffentlichung
prüfen und das Prüfdatum vermerken.

**Regel für den Agenten:** Ohne Energieausweisdaten wird kein
veröffentlichungsfähiges Inserat erzeugt. Stattdessen: Entwurf mit deutlich
markierter Lücke und Hinweis auf die Pflichtangabe.

## Provision und Widerruf (Deutschland)

- Bei der Vermittlung von **Einfamilienhäusern und Eigentumswohnungen an
  Verbraucher** gilt das Provisionsteilungsgebot der §§ 656a ff. BGB: Der
  Maklervertrag bedarf der Textform, und die Provision ist zwischen Käufer und
  Verkäufer nach den dort geregelten Grundsätzen zu teilen; der Käufer darf
  nicht mehr tragen als der Verkäufer, und der Käufer schuldet erst, wenn der
  Verkäufer gezahlt hat.
- Bei der **Vermietung von Wohnraum** gilt das Bestellerprinzip nach dem
  Wohnungsvermittlungsgesetz: Es zahlt, wer den Makler beauftragt hat;
  die Provision ist auf höchstens zwei Nettokaltmieten zuzüglich USt begrenzt.
- Bei Verträgen mit Verbrauchern außerhalb von Geschäftsräumen oder im
  Fernabsatz besteht ein **14-tägiges Widerrufsrecht**. Ohne ordnungsgemäße
  Widerrufsbelehrung droht der Provisionsverlust.
- Provisionsangaben im Exposé immer **inklusive Umsatzsteuer** und mit klarer
  Angabe, wer zahlt.

Österreich und Schweiz haben eigene Regeln (AT: Immobilienmaklerverordnung,
Höchstprovisionen; CH: vertragsfrei, kantonale Usanzen) – dort nicht das
deutsche Modell unterstellen.

## Texten: was funktioniert

**Struktur:** konkret → konkret → konkret. Der Leser sucht Fakten, nicht Stimmung.

| Statt | Besser |
|---|---|
| „Traumhaftes Wohnen im Grünen" | „Südwestgarten mit 180 m², angrenzend an das Landschaftsschutzgebiet" |
| „Toplage" | „Fußläufig 6 Minuten zum S-Bahnhof, Grundschule 400 m" |
| „Viel Potenzial" | „Dachgeschoss ausbaubar, Baugenehmigung von 2019 liegt vor" |
| „Gemütliche Wohnküche" | „Wohnküche 21 m², Anschluss für Kochinsel vorhanden" |
| „Renovierungsbedürftig" (allein) | „Bäder und Elektroinstallation aus 1978, Küche nicht vorhanden" |

**Regeln:**

- Kein Superlativ ohne Beleg
- Keine Behauptung, die im Kaufvertrag zur Beschaffenheitsvereinbarung werden
  könnte, wenn sie nicht gesichert ist („voll unterkellert", „Baugenehmigung
  vorhanden", „provisionsfrei")
- Mängel nicht verschweigen, wenn sie offenbarungspflichtig sind – dazu zählen
  regelmäßig verdeckte Feuchteschäden, Schwamm, Altlasten, Baurechtswidrigkeit
- „ca."-Angaben helfen nicht gegen falsche Flächen. Fläche mit Grundlage nennen
  oder gar nicht.
- Barrierefreiheit, Denkmalschutz, Erbbaurecht, laufende Mietverhältnisse,
  Sonderumlagen: gehören ins Exposé, nicht in ein Nachgespräch

## Bild- und Urheberrechte

- Fotos brauchen eine Nutzungsrechteklärung – auch Fotos des Vorbesitzers oder
  des vorherigen Maklers
- Grundrisse und Lagepläne sind urheberrechtlich geschützt (Architekt),
  Katasterauszüge unterliegen der Nutzungsregelung des Katasteramts
- Drohnenaufnahmen: Genehmigungslage und Persönlichkeitsrechte der Nachbarn
- Personen und Kennzeichen auf Fotos unkenntlich machen
- Innenaufnahmen bei vermieteten Objekten nur mit Einverständnis der Mieter
- KI-generierte oder KI-bearbeitete Bilder: Virtual Staging und
  Bildoptimierung sind zu kennzeichnen; nichts hinein­retuschieren, was nicht
  existiert; Art. 50 EU AI Act verlangt für KI-erzeugte Inhalte Transparenz

## Portalveröffentlichung

- Datenübergabe im DACH-Raum über den XML-Standard **OpenImmo**; Inhalte
  vorher strukturiert erfassen (Felder siehe Eckdaten-Tabelle oben)
- Je Portal eigene Feldlängen und Pflichtfelder – Texte in
  Kurz-/Langfassung vorhalten
- Titelzeile: Objekttyp + Alleinstellungsmerkmal + Lage, ca. 60–80 Zeichen
- Erstes Foto entscheidet über die Klickrate: Außenansicht bei Häusern,
  hellster Wohnraum bei Wohnungen
- Keine Adresse mit Hausnummer bei vermieteten oder bewohnten Objekten ohne
  Zustimmung
- Nach Reservierung/Verkauf: Inserat zeitnah deaktivieren

## Vorgehen

1. Objektdaten und Unterlagen prüfen: Flächenberechnung, Grundbuchauszug,
   Energieausweis, Teilungserklärung, Mietverträge
2. Pflichtangaben-Check: liegen Energieausweisdaten vor?
3. Zielgruppe bestimmen (Selbstnutzer / Kapitalanleger / Bauträger) – sie
   bestimmt die Reihenfolge der Argumente
4. Texte schreiben, Zahlen aus den Unterlagen belegen
5. Rechtliche Bausteine ergänzen: Provision, Widerruf, Haftungshinweis
6. Prüfliste durchgehen und Freigabe durch den Auftraggeber einholen

## Regeln

- **Ohne Energieausweisdaten kein veröffentlichungsfähiges Inserat.** Der
  Entwurf wird mit markierter Lücke ausgeliefert.
- Keine Behauptung, die nicht aus den Unterlagen belegt ist – jede Zusicherung
  kann im Kaufvertrag zur Beschaffenheit werden.
- Flächen mit Rechtsgrundlage oder gar nicht; „ca." schützt nicht vor falschen
  Flächenangaben.
- Offenbarungspflichtige Mängel werden nicht weggeschrieben.
- Provisionsangabe stets inklusive Umsatzsteuer und mit Angabe, wer zahlt;
  Provisionsteilung und Bestellerprinzip beachten.
- Bildrechte vor Veröffentlichung klären; Personen und Kennzeichen unkenntlich;
  Virtual Staging und KI-Bearbeitung kennzeichnen und nichts hineinretuschieren.
- Keine personenbezogenen Daten Dritter (Mieter, Nachbarn, Voreigentümer).
- Zahlen im Exposé stimmen mit dem Objektdatensatz überein – eine abweichende
  Fläche im Inserat ist ein Haftungsrisiko.
- Nach Reservierung oder Verkauf wird das Inserat zeitnah deaktiviert.

## Qualitätskontrolle

- [ ] Alle Pflichtangaben zum Energieausweis vorhanden oder Ausnahme benannt
- [ ] Flächenangaben mit Rechtsgrundlage, aus den Unterlagen belegt
- [ ] Keine unbelegte Zusicherung, die Beschaffenheit begründen könnte
- [ ] Offenbarungspflichtige Mängel enthalten
- [ ] Provisionsangabe korrekt, inkl. USt, mit Zahlungspflichtigem
- [ ] Widerrufsbelehrung beigefügt, wo erforderlich
- [ ] Bildrechte geklärt, Personen/Kennzeichen unkenntlich, KI-Bearbeitung gekennzeichnet
- [ ] Keine personenbezogenen Daten Dritter (Mieter, Nachbarn) im Exposé
- [ ] Zahlen im Exposé stimmen mit Objektdatensatz überein
- [ ] Freigabe eingeholt

## Grenzen

Keine Rechtsberatung zu Maklerrecht, Provisionsansprüchen oder
Widerrufsbelehrungen – die Muster gehören einmalig anwaltlich geprüft und
werden dann verwendet. Provisions- und Anzeigenrecht in AT/CH weicht ab.

## Anhang: Exposé-Gerüst mit Platzhaltern

Gerüst in Jinja2-Syntax, wie es docxtpl in einer Word-Vorlage verarbeitet.
Direkt aus dieser Datei übernehmbar; die Platzhalternamen sind frei wählbar,
sollten aber im ganzen Betrieb einheitlich bleiben.

### {{ texte.ueberschrift }}

**{{ objekt.objektart_klartext }} · {{ objekt.adresse.plz }} {{ objekt.adresse.ort }}{% if objekt.adresse.ortsteil %}-{{ objekt.adresse.ortsteil }}{% endif %}**
Objektnummer {{ objekt_id }}

#### Auf einen Blick

| | |
|---|---|
| Kaufpreis / Miete | {{ preis.anzeige }} |
| Wohnfläche | {{ objekt.wohnflaeche_anzeige }} ({{ objekt.flaechenbasis_klartext }}) |
| Grundstück | {{ objekt.grundstuecksflaeche_anzeige }} |
| Zimmer | {{ objekt.zimmer }} |
| Baujahr | {{ objekt.baujahr }} |
| Letzte Modernisierung | {{ objekt.letzte_modernisierung }} |
| Zustand | {{ objekt.zustand_klartext }} |
| Heizung | {{ objekt.energie.heizung_klartext }} |
| Stellplätze | {{ objekt.stellplaetze_klartext }} |
| Verfügbar ab | {{ verfuegbar_ab }} |

#### Das Objekt

{{ texte.objektbeschreibung }}

#### Ausstattung

{{ texte.ausstattung }}

#### Lage

{{ texte.lagebeschreibung }}

#### Energieausweis

{%p if pflichtangaben.energieausweis_vorhanden %}
| | |
|---|---|
| Art des Ausweises | {{ pflichtangaben.ausweisart_klartext }} |
| Kennwert | {{ pflichtangaben.kennwert_anzeige }} kWh/(m²·a) |
| Warmwasser enthalten | {{ pflichtangaben.warmwasser_klartext }} |
| Wesentlicher Energieträger | {{ pflichtangaben.energietraeger }} |
| Baujahr laut Ausweis | {{ pflichtangaben.baujahr_laut_ausweis }} |
| Energieeffizienzklasse | {{ pflichtangaben.energieeffizienzklasse }} |
{%p endif %}
{%p if not pflichtangaben.energieausweis_vorhanden %}
**ACHTUNG – nicht veröffentlichungsfähig:** Es liegen keine Energieausweisdaten
vor. Die gesetzlichen Pflichtangaben fehlen. Vor Veröffentlichung ergänzen oder
den Ausnahmegrund eintragen: {{ pflichtangaben.ausnahme_grund }}
{%p endif %}

#### Kosten

{%p if vermarktungsart == "kauf" %}
| | |
|---|---|
| Kaufpreis | {{ preis.kaufpreis_anzeige }} |
| Käuferprovision | {{ preis.provision_anzeige }} inkl. gesetzlicher USt |
| Grunderwerbsteuer | {{ nebenkosten.grest_anzeige }} ({{ nebenkosten.grest_bundesland }}) |
| Notar und Grundbuch | rund {{ nebenkosten.notar_anzeige }} |
{%p endif %}
{%p if vermarktungsart == "miete" %}
| | |
|---|---|
| Nettokaltmiete | {{ preis.nettokaltmiete_anzeige }} |
| Nebenkosten | {{ preis.nebenkosten_anzeige }} |
| Kaution | {{ preis.kaution_anzeige }} |
| Provision | {{ preis.provision_anzeige }} |
{%p endif %}

#### Grundrisse und Fotos

{%p for m in medien %}
{{ m.titel }} – {{ m.datei }}
{%p endfor %}

Grundrisse sind nicht maßstabsgetreu und dienen der Orientierung.

#### Ihr Ansprechpartner

{{ kontakt.firma }}
{{ kontakt.ansprechpartner }} · {{ kontakt.telefon }} · {{ kontakt.email }}

#### Hinweise

Alle Angaben beruhen auf Informationen des Eigentümers und den vorliegenden
Unterlagen. Eine Haftung für Vollständigkeit und Richtigkeit wird nicht
übernommen. Zwischenverkauf und Irrtum vorbehalten. Dieses Exposé ist
vertraulich und nur für den Empfänger bestimmt; eine Weitergabe an Dritte ist
ohne Zustimmung nicht gestattet.

{%p if widerrufsbelehrung_erforderlich %}
##### Widerrufsbelehrung
{{ widerrufsbelehrung }}
{%p endif %}

#### Prüfliste vor Freigabe

- [ ] Energieausweis-Pflichtangaben vollständig oder Ausnahmegrund eingetragen
- [ ] Flächenangaben mit Rechtsgrundlage, aus Unterlagen belegt
- [ ] Keine unbelegte Zusicherung im Beschreibungstext
- [ ] Offenbarungspflichtige Mängel enthalten
- [ ] Provision korrekt, inkl. USt, mit Zahlungspflichtigem
- [ ] Widerrufsbelehrung beigefügt, wo erforderlich
- [ ] Bildrechte geklärt, Personen/Kennzeichen unkenntlich
- [ ] KI-bearbeitete Bilder (Virtual Staging) gekennzeichnet
- [ ] Keine personenbezogenen Daten Dritter
- [ ] Keine verbliebenen Platzhalter im Ergebnis

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
