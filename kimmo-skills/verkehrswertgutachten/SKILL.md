---
name: verkehrswertgutachten
description: Aufbau, Gliederung und Formulierung eines Verkehrswertgutachtens nach § 194 BauGB und ImmoWertV 2021 – vom Auftrag über Verfahrensdurchführung bis zur Wertableitung, inklusive Kurzgutachten und Marktwerteinschätzung. Nutzen, wenn ein Gutachten, Wertermittlung oder Wertermittlungsbericht geschrieben werden soll.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE]
---

# Verkehrswertgutachten

## Zweck

Ein Gutachten ist nicht die Zahl am Ende, sondern die nachvollziehbare
Herleitung dorthin. Dieser Skill gibt Gliederung, Pflichtinhalte und
Formulierungsregeln vor.

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

- Vollgutachten, Kurzgutachten, Wertermittlungsbericht
- Marktwerteinschätzung / Kaufpreisindikation (reduzierte Form, klar bezeichnet)

## Der Wertbegriff

> **§ 194 BauGB:** Der Verkehrswert (Marktwert) wird durch den Preis bestimmt,
> der in dem Zeitpunkt, auf den sich die Ermittlung bezieht, im gewöhnlichen
> Geschäftsverkehr nach den rechtlichen Gegebenheiten und tatsächlichen
> Eigenschaften, der sonstigen Beschaffenheit und der Lage des Grundstücks oder
> des sonstigen Gegenstands der Wertermittlung ohne Rücksicht auf ungewöhnliche
> oder persönliche Verhältnisse zu erzielen wäre.

Daraus folgt für jedes Gutachten:

- **Stichtagsbezogen** – ein Verkehrswert gilt zum Stichtag, nicht „aktuell"
- **Gewöhnlicher Geschäftsverkehr** – keine Zwangslagen, keine
  Liebhaberpreise, keine Verwandtenpreise
- **Objektiv** – nicht der Wert für den Auftraggeber, sondern für den Markt

Abzugrenzen: **Beleihungswert** (nachhaltig, vorsichtig, BelWertV),
**Marktpreis** (tatsächlich gezahlt), **Kaufpreisindikation** (Einschätzung
ohne Gutachtenqualität), **Steuerwert** (BewG, eigene Regeln).

## Gliederung Vollgutachten

```
Deckblatt
  Objektbezeichnung, Aktenzeichen, Auftraggeber, Stichtag, Erstelldatum,
  Ersteller, Anzahl Seiten und Anlagen

1  Auftrag
   1.1 Auftraggeber und Auftragsdatum
   1.2 Bewertungsobjekt (Grundbuchbezeichnung)
   1.3 Zweck der Wertermittlung
   1.4 Wertermittlungsstichtag, Qualitätsstichtag
   1.5 Ortsbesichtigung: Datum, Umfang, Teilnehmer – oder Hinweis auf Verzicht
   1.6 Verwendete Unterlagen und Auskünfte
   1.7 Rechtsgrundlagen (§ 194 BauGB, ImmoWertV 2021, ImmoWertA)

2  Grundstücksbeschreibung
   2.1 Lage: Makrolage, Mikrolage, Infrastruktur, Immissionen
   2.2 Grundstück: Größe, Zuschnitt, Topografie, Erschließung
   2.3 Rechtliche Gegebenheiten
       Grundbuch Abt. I/II/III, Baulasten, Denkmalschutz, Altlasten,
       Erbbaurecht, Sanierungs-/Umlegungsvermerke
   2.4 Planungsrecht: B-Plan / § 34 / § 35 BauGB, GRZ/GFZ, zulässige Nutzung
   2.5 Gebäude: Baujahr, Bauweise, Ausstattung, Flächen mit Rechtsgrundlage,
       energetischer Zustand, Modernisierungen, Bauschäden und -mängel
   2.6 Nutzung: eigengenutzt / vermietet, Mietverhältnisse

3  Grundstücksmarkt
   3.1 Allgemeine Wertverhältnisse zum Stichtag
   3.2 Regionaler Markt, Angebot und Nachfrage
   3.3 Verwendete Marktdaten mit Quelle und Stand

4  Wertermittlung
   4.1 Wahl der Verfahren mit Begründung
   4.2 Bodenwertermittlung
   4.3 Verfahren 1 (vollständige Herleitung)
   4.4 Verfahren 2 (vollständige Herleitung)
   4.5 Besondere objektspezifische Grundstücksmerkmale
   4.6 Wertrelevanz von Rechten und Belastungen

5  Verkehrswert
   5.1 Gegenüberstellung der Verfahrensergebnisse
   5.2 Würdigung und Gewichtung mit Begründung
   5.3 Verkehrswert zum Stichtag
   5.4 Kontrollkennzahlen und Plausibilität
   5.5 Sensitivität kritischer Eingangsgrößen

6  Zusammenfassung (eine Seite, für sich lesbar)

7  Annahmen, Einschränkungen und Hinweise
   nicht geprüfte Sachverhalte, fehlende Unterlagen, Gültigkeitsdauer,
   Verwendungszweckbindung, Haftungshinweis

Anlagen
   Grundbuchauszug, Flurkarte, Grundrisse, Fotodokumentation,
   Bodenrichtwertauskunft, Berechnungen, Quellenverzeichnis
```

## Kurzgutachten

Gleiche Logik, reduzierter Umfang: Abschnitte 1, 2 (gekürzt), 4, 5, 7. Der
reduzierte Umfang und seine Folgen für die Aussagekraft werden **ausdrücklich
benannt**. Ein Kurzgutachten wird nie als Vollgutachten bezeichnet.

## Wertableitung – der kritische Abschnitt

Die Verfahren liefern unterschiedliche Ergebnisse. Das ist normal. Die
Ableitung des Verkehrswerts daraus ist eine **begründete Würdigung**, kein
Rechenschritt.

```
Vergleichswertverfahren   495.000 €
Sachwertverfahren         468.000 €

Würdigung: Für Reihenmittelhäuser in der Siedlung … liegen mit 11 Kauffällen
der Jahre 2024–2026 belastbare Vergleichspreise vor. Der Markt orientiert sich
in diesem Segment an Vergleichspreisen je m² Wohnfläche; das
Sachwertverfahren dient der Kontrolle. Beide Ergebnisse liegen mit 5,5 %
Abweichung eng beieinander, was die Ableitung stützt. Der Verkehrswert wird
dem Vergleichswertverfahren folgend, unter leichter Berücksichtigung des
niedrigeren Sachwerts, mit 490.000 € angesetzt.
```

**Verboten:**

- arithmetisches Mitteln ohne Begründung
- „Gewichtung 60 : 40" ohne Herleitung, warum gerade so
- ein Verkehrswert außerhalb der Spanne der Verfahrensergebnisse ohne
  ausdrückliche Begründung

## Vorgehen

1. Auftragsrahmen festhalten: die vier Pflichtangaben, Adressat, Umfang
   (Objekt, Stichtag, Wertbegriff, Zweck)
2. Unterlagen auswerten, Lücken und Widersprüche dokumentieren
3. Objekt beschreiben sowie Makro- und Mikrolage bewerten
4. Grundstücksmarkt zum Stichtag darstellen
5. Verfahren wählen und begründen, Bodenwert ermitteln
6. Verfahren vollständig durchrechnen und dokumentieren
7. Verkehrswert begründet ableiten, plausibilisieren, Sensitivität ausweisen
8. Zusammenfassung schreiben, die für sich allein verständlich ist
9. Annahmen, Einschränkungen und Anlagen ergänzen
10. Qualitätskontrolle durchlaufen und den Entwurf zur Freigabe übergeben

## Regeln

- Der Verkehrswert ist stichtagsbezogen; ein Gutachten ohne durchgängig
  identischen Stichtag ist fehlerhaft.
- Mindestens zwei Verfahren, oder eine ausdrückliche Begründung, warum nur
  eines möglich ist.
- Die Ableitung des Verkehrswerts wird begründet, nie arithmetisch gemittelt.
- Jede Eingangsgröße mit Quelle und Stand; keine Zahl aus dem Modellwissen.
- Zahlen in Text, Tabellen und Zusammenfassung müssen deckungsgleich sein.
- Kurzgutachten wird als solches bezeichnet, mit Hinweis auf die begrenzte
  Aussagekraft.
- Kein Entwurf mit Unterschriftszeile, Siegelfeld oder Sachverständigenformel.
- Verwendungszweck und Adressat werden benannt; das Gutachten ist an diesen
  Zweck gebunden.

## Formulierungsregeln

- Sachlich, im Indikativ, ohne Werbesprache und ohne Weichmacher
  („traumhaft", „wohl eher", „vermutlich")
- Unsicherheit wird **benannt**, nicht sprachlich versteckt:
  „Da keine Innenbesichtigung stattgefunden hat, beruht die Einschätzung des
  Ausbauzustands auf Angaben des Eigentümers."
- Jede Zahl mit Quelle und Stand
- Stichtag durchgängig identisch
- Rundung: Verkehrswerte auf volle 1.000 €, bei kleineren Objekten auf 5.000 €;
  Rundung benennen
- Zahlen im Text und in den Tabellen müssen übereinstimmen

## Freigabe und Verantwortung

Ein Verkehrswertgutachten nach § 194 BauGB, das gegenüber Dritten verwendet
wird (Bank, Gericht, Finanzamt, Erbengemeinschaft, Betreuungsgericht), muss
von einer entsprechend qualifizierten Person verantwortet werden. Der Agent
liefert einen **Entwurf**, der fachlich geprüft und freigegeben werden muss.

Der Entwurf enthält daher:

- keine Unterschriftszeile, kein Siegelfeld, keine Sachverständigenformel
- den Vermerk „Entwurf – fachliche Prüfung und Freigabe erforderlich"
- den Übergabeblock mit den prüfbedürftigen Punkten

## Ausgabeformat

Word-Datei mit Kopfzeile (Aktenzeichen und Stichtag), Fußzeile „Seite X von Y",
Inhaltsverzeichnis, nummerierten Überschriften über Formatvorlagen, Tabellen mit
auf jeder Seite wiederholter Kopfzeile und Fotodokumentation mit
Bildunterschriften. Existiert eine Kanzlei- oder Bürovorlage, wird sie befüllt
und nicht optisch nachgebaut.

## Qualitätskontrolle

- [ ] Alle Gliederungspunkte belegt oder ihr Fehlen begründet
- [ ] Vier Pflichtangaben im Abschnitt 1 vollständig
- [ ] Stichtag durchgängig identisch
- [ ] Jede Eingangsgröße mit Quelle und Stand
- [ ] Mindestens zwei Verfahren oder Begründung, warum nur eines
- [ ] Wertableitung begründet, nicht gemittelt
- [ ] Verkehrswert innerhalb der Verfahrensspanne oder begründet außerhalb
- [ ] Zahlen in Text, Tabellen und Zusammenfassung deckungsgleich
- [ ] Kontrollkennzahlen und Sensitivität ausgewiesen
- [ ] Annahmen und Einschränkungen vollständig
- [ ] Entwurfsvermerk und Übergabeblock vorhanden
- [ ] Zusammenfassung für sich allein verständlich

## Grenzen

Kein bestellter Sachverständiger, keine gerichtsfeste Ausfertigung, keine
Bauschadensbeurteilung. Beleihungswertermittlung folgt der BelWertV und ist
nicht Gegenstand dieses Skills. In Österreich und der Schweiz gelten
eigene Regelwerke (LBG/ÖNORM bzw. SVKG-Standard/SIA).

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
