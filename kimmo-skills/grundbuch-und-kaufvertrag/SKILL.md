---
name: grundbuch-und-kaufvertrag
description: Grundbuch lesen und Immobilienkaufverträge vorprüfen – Aufbau der drei Abteilungen, Rechte und Lasten und ihre Wertwirkung, Erbbaurecht, Kaufvertragsablauf, Auflassungsvormerkung, Fälligkeit, Gewährleistung, Bauträgerkauf nach MaBV. Nutzen bei Grundbuch, Kaufvertrag, Notar, Dienstbarkeit, Vormerkung, Abwicklung.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE]
---

# Grundbuch und Kaufvertrag

## Zweck

Das Grundbuch sagt, wem was gehört und was daran hängt. Der Kaufvertrag regelt,
wie es übergeht. Beides falsch zu lesen ist teuer. Dieser Skill gibt die
Struktur und die Prüfpunkte.

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

- Grundbuchauszug auswerten
- Kaufvertragsentwurf vorprüfen
- Fragen zu Rechten, Lasten, Vormerkung, Abwicklung
- Ablauf und Fristen des Erwerbs erklären

## Aufbau des Grundbuchs

| Teil | Inhalt | Bewertungsrelevanz |
|---|---|---|
| **Aufschrift** | Amtsgericht, Grundbuchbezirk, Blattnummer | Identifikation |
| **Bestandsverzeichnis** | Flur, Flurstück, Wirtschaftsart, Größe; herrschende Rechte | Objektabgrenzung, Fläche |
| **Abteilung I** | Eigentümer, Erwerbsgrund, Anteile | Verfügungsbefugnis, Erbengemeinschaft |
| **Abteilung II** | Lasten und Beschränkungen: Dienstbarkeiten, Wohnrecht, Nießbrauch, Reallast, Vorkaufsrecht, Erbbaurecht, Vormerkungen, Insolvenz-, Sanierungs-, Umlegungsvermerke, Zwangsversteigerungsvermerk | **hoch – regelmäßig wertrelevant** |
| **Abteilung III** | Grundpfandrechte: Hypothek, Grund- und Rentenschuld | für den Verkehrswert grundsätzlich **nicht** wertmindernd |

### Leseregeln

- **Gerötete (durchgestrichene) Einträge sind gelöscht.** Sie dürfen nicht als
  bestehende Rechte übernommen werden.
- Die Spalten „Veränderungen" und „Löschungen" gehören zwingend mitgelesen –
  der ursprüngliche Eintrag kann inhaltlich überholt sein.
- Der **Rang** entscheidet bei Zwangsversteigerung, welche Rechte bestehen
  bleiben. Ein Wohnrecht im ersten Rang ist etwas anderes als eines im fünften.
- Bezugsurkunden (Eintragungsbewilligungen) enthalten den eigentlichen Inhalt.
  Der Grundbucheintrag ist oft nur ein Schlagwort – für die Bewertung ist die
  **Bewilligung** anzufordern.
- **Baulasten stehen nicht im Grundbuch**, sondern im Baulastenverzeichnis der
  Bauaufsicht (in einigen Bundesländern nicht geführt – dort über
  Dienstbarkeiten geregelt).
- Ein Grundbuchauszug ist eine Momentaufnahme. Älter als 3 Monate: neu anfordern.

### Wertwirkung typischer Rechte

| Recht | Typische Wirkung |
|---|---|
| Wegerecht, Leitungsrecht | gering bis mittel wertmindernd, je nach Lage und Umfang |
| Wohnungsrecht, Nießbrauch | erheblich wertmindernd; kapitalisierter Wert über Barwert der ersparten Miete bzw. Nutzung und statistische Lebenserwartung |
| Vorkaufsrecht | vermarktungshemmend, meist geringe Wertwirkung |
| Reallast (z. B. Leibgeding) | Barwert der wiederkehrenden Leistung |
| Erbbaurecht | eigener Bewertungsgegenstand, siehe unten |
| Sanierungsvermerk | Genehmigungspflicht, ggf. Ausgleichsbetrag |
| Zwangsversteigerungsvermerk | Sondersituation, kein gewöhnlicher Geschäftsverkehr |

Die Bezifferung erfolgt nach ImmoWertV Teil 4 Abschnitt 2 – hergeleitet, nicht
pauschal geschätzt.

## Erbbaurecht

Zu erfassen: Erbbauzins und Anpassungsklausel, Restlaufzeit, Heimfallregelung,
Entschädigung bei Zeitablauf (Prozentsatz des Gebäudewerts), Zustimmungs-
vorbehalte bei Verkauf und Belastung.

Bewertet werden **Erbbaurecht** und **Erbbaugrundstück** getrennt (ImmoWertV
§§ 48–52: Vergleichswertverfahren oder finanzmathematischer Wert). Die
Restlaufzeit ist der dominierende Faktor: Unter etwa 30 Jahren wird die
Finanzierbarkeit für Erwerber zum Problem, was den Markt zusätzlich einengt.

## Ablauf eines Immobilienkaufs (Deutschland)

```
1  Einigung über Kaufpreis und Bedingungen
2  Notarentwurf; bei Verbraucherbeteiligung Regelfrist von 2 Wochen
   zwischen Entwurfsübermittlung und Beurkundung
3  Beurkundung durch den Notar (§ 311b BGB – ohne Beurkundung nichtig)
4  Eintragung der Auflassungsvormerkung zugunsten des Käufers
5  Einholung von Genehmigungen, Vorkaufsrechtsverzicht der Gemeinde,
   Löschungsunterlagen der Gläubiger
6  Fälligkeitsmitteilung des Notars
7  Kaufpreiszahlung
8  Besitzübergang: Besitz, Nutzen, Lasten und Gefahr
9  Grunderwerbsteuerbescheid, Zahlung, Unbedenklichkeitsbescheinigung
10 Eigentumsumschreibung in Abteilung I, Löschung der Vormerkung
```

Die **Auflassungsvormerkung** ist der zentrale Käuferschutz: Sie sichert den
Anspruch auf Eigentumsübertragung gegen spätere Verfügungen und Belastungen.
Ohne sie wird nicht gezahlt.

## Prüfpunkte im Kaufvertragsentwurf

Der Agent führt eine **Vorprüfung** durch – die rechtliche Würdigung bleibt
bei Notar und Anwalt.

- **Vertragsgegenstand:** Grundbuchbezeichnung, Flurstücke, bei ETW auch
  Miteigentumsanteil und Sondernutzungsrechte vollständig?
- **Kaufpreis:** Betrag, Aufteilung auf Grund und Boden / Gebäude / Inventar
  (bestimmt die AfA-Bemessungsgrundlage, steuerlich prüfen lassen), Zahlungsweg
- **Fälligkeit:** Welche Voraussetzungen müssen vorliegen? Vormerkung
  eingetragen, Löschungsunterlagen vollständig, Genehmigungen erteilt?
- **Besitzübergang:** Datum; Übergang von Nutzen, Lasten und Gefahr;
  Nutzungsentschädigung bei Abweichung
- **Rechte in Abt. II:** Welche werden übernommen, welche gelöscht? Wer trägt
  die Kosten?
- **Abt. III:** Lastenfreistellung geregelt?
- **Gewährleistung:** Ausschluss für Sachmängel ist üblich; Ausnahmen für
  Arglist und für ausdrücklich vereinbarte Beschaffenheiten
- **Beschaffenheitsvereinbarungen:** Wohnfläche, Baugenehmigung, Nutzbarkeit,
  Altlastenfreiheit, Energieausweis – alles, was der Verkäufer zusichert, wird
  hier verbindlich – Achtung bei Aussagen aus dem Exposé
- **Mietverhältnisse:** „Kauf bricht nicht Miete" (§ 566 BGB) – bestehende
  Mietverträge, Kautionen und Betriebskostenabrechnungen regeln
- **Inventar/Zubehör:** Liste, gesonderter Preis
- **Rücktritt und Vertragsstrafe:** Voraussetzungen, Fristen
- **Vollmachten und Kosten:** Wer trägt was
- **Bauträgerkauf:** Zusätzlich die MaBV-Regeln – Zahlungen nur nach
  Baufortschritt in den vorgesehenen Raten, Sicherheiten, Baubeschreibung,
  Abnahme des Sondereigentums und des Gemeinschaftseigentums getrennt

## Vorgehen

1. Aktualität des Grundbuchauszugs prüfen (nicht älter als 3 Monate)
2. Bestandsverzeichnis und alle drei Abteilungen auswerten, gelöschte
   Einträge ausschließen, Ränge erfassen
3. Bezugsurkunden zu unklaren Eintragungen anfordern
4. Baulasten, Altlasten und Denkmalschutz separat abfragen
5. Wertwirkung der Rechte einzeln einschätzen und, wo möglich, beziffern
6. Kaufvertragsentwurf gegen das Prüfraster durchgehen, Wortlaut zitieren
7. Auffälligkeiten und Klärungsbedarf für Notar und Anwalt zusammenstellen
8. Fristen benennen und dem Nutzer zuweisen

## Regeln

- Der Agent prüft, ordnet ein und benennt Risiken – er beurteilt nicht
  rechtsverbindlich und ersetzt keine notarielle Beratung.
- Wortlaut zitieren, nicht paraphrasieren; Fundstelle (Paragraph, Absatz) nennen.
- Gerötete Einträge nie als bestehend übernehmen.
- Grundbuchdaten enthalten Personendaten – nur verwenden, soweit erforderlich
  (siehe Grundregeln, Personendaten).
- Keine Aussage zur Wirksamkeit einer Klausel ohne Verweis auf anwaltliche
  Prüfung.
- Bei Fristen: Frist nennen und ausdrücklich darauf hinweisen, dass ihre
  Wahrung nicht durch den Agenten erfolgt.

## Ausgabeformat

```
## Grundbuchauswertung
Bestandsverzeichnis · Abt. I · Abt. II (je Recht: Inhalt, Rang, Wertwirkung) · Abt. III
Gelöschte Einträge: ausgeschlossen
Nicht im Grundbuch geprüft: Baulasten, Altlasten

## Kaufvertrag – Vorprüfung
| Prüfpunkt | Regelung im Entwurf | Bewertung | Klärungsbedarf |

## Offene Punkte für Notar/Anwalt
```

## Qualitätskontrolle

- [ ] Alle drei Abteilungen ausgewertet, gelöschte Einträge ausgeschlossen
- [ ] Bezugsurkunden angefordert, wo der Eintrag nicht selbsterklärend ist
- [ ] Rangverhältnisse erfasst
- [ ] Baulasten separat geprüft
- [ ] Auszug aktuell (< 3 Monate)
- [ ] Alle Prüfpunkte des Vertragsrasters abgearbeitet
- [ ] Wortlautzitate mit Fundstelle
- [ ] Rechtliche Würdigung als Klärungsbedarf ausgewiesen, nicht behauptet

## Grenzen

Keine Rechtsberatung, keine Grundbucheinsicht durch den Agenten (nur
Berechtigte mit berechtigtem Interesse), keine Prüfung der Wirksamkeit von
Klauseln. Gilt für Deutschland; AT und CH haben abweichende Register- und
Vertragspraxis.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
