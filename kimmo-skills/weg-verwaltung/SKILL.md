---
name: weg-verwaltung
description: Wohnungseigentum und WEG-Verwaltung – Teilungserklärung, Sondereigentum und Gemeinschaftseigentum, Beschlüsse und Beschlusssammlung, Wirtschaftsplan und Jahresabrechnung, Erhaltungsrücklage, Sonderumlagen, bauliche Veränderungen. Nutzen bei WEG, Eigentümerversammlung, Hausgeld, Teilungserklärung, Beschluss, Rücklage.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE]
---

# Wohnungseigentum und WEG-Verwaltung

## Zweck

Beim Kauf einer Eigentumswohnung kauft man eine Beteiligung an einer
Gemeinschaft mit. Deren Zustand – Rücklage, Beschlusslage, anstehende
Maßnahmen – ist oft wertrelevanter als die Wohnung selbst. Dieser Skill gibt
das Prüfraster.

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

- Ankaufsprüfung einer Eigentumswohnung
- Bewertung einer ETW (Ergänzung zu `vergleichswertverfahren`)
- Auswertung von Protokollen, Wirtschaftsplänen, Jahresabrechnungen
- Fragen zu Beschlüssen, Hausgeld, Sonderumlagen, baulichen Veränderungen

## Grundbegriffe

| Begriff | Bedeutung |
|---|---|
| **Sondereigentum** | Die Wohnung selbst: Räume, nicht tragende Innenwände, Bodenbeläge, Innentüren, Sanitärobjekte – wie in Teilungserklärung und Aufteilungsplan abgegrenzt |
| **Gemeinschaftseigentum** | Alles, was der Konstruktion oder gemeinschaftlichen Nutzung dient: Dach, Fassade, tragende Wände, Fenster (in der Regel!), Treppenhaus, Leitungen bis zur Abzweigung, Heizungsanlage |
| **Sondernutzungsrecht** | Alleinnutzung an Gemeinschaftseigentum (Gartenanteil, Stellplatz, Kellerraum) – kein Eigentum |
| **Miteigentumsanteil (MEA)** | Bruchteil am Gemeinschaftseigentum; bestimmt in der Regel Kostenverteilung und Stimmrecht |
| **Teilungserklärung** | Begründungsurkunde; enthält Aufteilungsplan und meist die Gemeinschaftsordnung |
| **Gemeinschaftsordnung** | „Satzung" der Gemeinschaft: Kostenverteilung, Nutzungsbeschränkungen, Stimmrecht, Verwaltung |
| **Erhaltungsrücklage** | Ansparung für Instandhaltung des Gemeinschaftseigentums (früher: Instandhaltungsrücklage) |
| **Beschlusssammlung** | Fortlaufende Sammlung aller Beschlüsse – **das wichtigste Dokument der Ankaufsprüfung** |

**Häufigster Irrtum:** Fenster und Wohnungseingangstür gehören regelmäßig zum
Gemeinschaftseigentum, auch wenn sie nur einer Wohnung dienen. Was im
Einzelfall gilt, steht in der Teilungserklärung – dort nachsehen, nicht raten.

## Prüfraster Ankauf einer ETW

### Unterlagen

- Teilungserklärung mit Gemeinschaftsordnung und Aufteilungsplan
- Abgeschlossenheitsbescheinigung
- **Beschlusssammlung** (vollständig)
- Protokolle der letzten 3 Eigentümerversammlungen
- Wirtschaftspläne und Jahresabrechnungen der letzten 3 Jahre
- Stand der Erhaltungsrücklage zum Stichtag
- Verwaltervertrag, Angaben zum Verwalter
- Hausgeldabrechnung der Einheit, offene Forderungen
- ggf. Beschlüsse zu baulichen Veränderungen an der Einheit

### Auswertung

| Prüfpunkt | Worauf achten |
|---|---|
| **Rücklage** | Höhe absolut und je m² Wohnfläche; Verhältnis zu Baujahr und Sanierungsstand. Eine niedrige Rücklage bei altem Bestand ist eine verdeckte Verbindlichkeit. |
| **Beschlossene Maßnahmen** | Bereits beschlossene Sanierungen binden den Erwerber wirtschaftlich – auch wenn die Umlage erst später fällig wird |
| **Sonderumlagen** | beschlossen, angekündigt oder absehbar? |
| **Instandhaltungsstau** | Dach, Fassade, Fenster, Stränge, Heizung, Aufzug, Balkone, Tiefgarage – Alter und Zustand |
| **Kostenverteilung** | Abweichungen vom MEA-Schlüssel in der Gemeinschaftsordnung? Einzelne Einheiten mit Sonderregelungen? |
| **Streitigkeiten** | laufende Beschlussanfechtungen, Rechtsstreite, Hausgeldrückstände anderer Eigentümer |
| **Nutzungsbeschränkungen** | Vermietungsverbote, Ferienvermietung, Tierhaltung, gewerbliche Nutzung |
| **Verwalter** | Bestellung wirksam und aktuell? Qualität der Abrechnungen? |
| **Zahlungsmoral** | Hausgeldrückstände in der Gemeinschaft insgesamt |

### Wertwirkung

Für die Bewertung der Einheit relevant:

- Anteilige Erhaltungsrücklage – nach herrschender Praxis kein einfach
  hinzuzurechnender Vermögenswert, aber ein preisbildender Faktor, dessen
  Behandlung im Gutachten zu begründen ist
- Absehbarer Sanierungsbedarf am Gemeinschaftseigentum als besonderes
  objektspezifisches Grundstücksmerkmal (Abschlag, hergeleitet aus dem
  anteiligen Kostenanteil)
- Nutzungsbeschränkungen, die die Marktgängigkeit einschränken

## Beschlüsse und Versammlung

- Beschlüsse werden in der Eigentümerversammlung gefasst; die Versammlung ist
  seit der WEG-Reform 2020 **unabhängig von der Zahl der vertretenen Anteile
  beschlussfähig**
- Beschlüsse sind **anfechtbar innerhalb eines Monats** ab Beschlussfassung;
  Klagebegründung binnen zwei Monaten
- Beschlüsse wirken auch gegen Rechtsnachfolger – deshalb ist die
  Beschlusssammlung beim Ankauf Pflichtlektüre
- **Bauliche Veränderungen** (§ 20 WEG): Beschluss mit einfacher Mehrheit
  möglich; wer sie verlangt und wem sie zugutekommen, bestimmt die
  Kostentragung
- **Privilegierte Maßnahmen** (§ 20 Abs. 2 WEG): auf Verlangen eines
  Eigentümers zu gestatten, u. a. Barrierereduzierung, Laden elektrisch
  betriebener Fahrzeuge, Einbruchsschutz, Glasfaseranschluss – die Kosten
  trägt der Verlangende
- Der **Verwalter** hat seit der Reform erweiterte Vertretungsbefugnisse; die
  Bestellung eines zertifizierten Verwalters kann verlangt werden

## Vorgehen

1. Unterlagen vollständig anfordern – Lücken sind selbst ein Befund
2. Protokolle chronologisch auswerten, Beschlüsse extrahieren
3. Rücklagenentwicklung über drei Jahre darstellen
4. Anstehende und absehbare Maßnahmen mit geschätzter Kostenbeteiligung listen
5. Wirtschaftliche Gesamteinschätzung und Wertrelevanz ableiten
6. Rechtsfragen zu Beschlüssen und Gemeinschaftsordnung an Anwalt (Stufe 3)

## Regeln

- Sondereigentum und Gemeinschaftseigentum nie nach Gefühl abgrenzen – immer
  Teilungserklärung und Aufteilungsplan heranziehen.
- Beschlusssammlung vollständig verlangen; „liegt nicht vor" ist ein Risiko,
  das benannt gehört.
- Rücklagenhöhe immer ins Verhältnis setzen (€/m², Baujahr, Sanierungsstand),
  nie als absolute Zahl bewerten.
- Beschlossene Maßnahmen wirtschaftlich beim Erwerber berücksichtigen.
- Keine Aussage zur Wirksamkeit von Beschlüssen oder Klauseln der
  Gemeinschaftsordnung – das ist Rechtsberatung.
- Namen anderer Eigentümer und deren Zahlungsverhalten sind Personendaten:
  nur aggregiert verarbeiten (siehe Grundregeln, Personendaten).

## Ausgabeformat

```
## WEG-Prüfung <Objekt>, Einheit <Nr.>
### Struktur
MEA · Sondernutzungsrechte · Anzahl Einheiten · Baujahr · Verwalter

### Beschlusslage (letzte 3 Jahre)
| Datum | Beschluss | Wirtschaftliche Folge für die Einheit |

### Rücklage
| Jahr | Stand | €/m² | Zuführung |

### Instandhaltungsstau und geplante Maßnahmen
| Bauteil | Zustand/Alter | geschätzte Kosten gesamt | Anteil der Einheit |

### Nutzungsbeschränkungen
### Risiken und fehlende Unterlagen
### Wertrelevanz
```

## Qualitätskontrolle

- [ ] Teilungserklärung und Aufteilungsplan ausgewertet
- [ ] Beschlusssammlung vollständig oder Lücke benannt
- [ ] Rücklage je m² und im Verhältnis zum Baujahr eingeordnet
- [ ] Beschlossene und absehbare Maßnahmen mit Kostenanteil beziffert
- [ ] Abweichende Kostenverteilungsschlüssel geprüft
- [ ] Nutzungsbeschränkungen erfasst
- [ ] Rechtsfragen als solche ausgewiesen
- [ ] Personendaten aggregiert

## Grenzen

Keine Rechtsberatung zum WEG, keine Beurteilung der Wirksamkeit von
Beschlüssen, keine Bausubstanzbeurteilung. Kostenschätzungen für Maßnahmen am
Gemeinschaftseigentum sind Größenordnungen und ersetzen keine Fachplanung.
Gilt für Deutschland.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
