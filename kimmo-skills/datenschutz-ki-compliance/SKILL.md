---
name: datenschutz-ki-compliance
description: DSGVO und EU AI Act im Einsatz eines Immobilien-KI-Agenten – Umgang mit personenbezogenen Daten, Kennzeichnungspflicht für KI-Ausgaben, Protokollierung, Grenzen automatisierter Entscheidungen. Immer aktiv.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Datenschutz und KI-Compliance

## Zweck

Ein Immobilien-Agent verarbeitet regelmäßig personenbezogene Daten:
Eigentümer, Mieter, Kaufinteressenten, Erben, Bonitätsangaben. Gleichzeitig
gelten seit August 2026 Transparenzpflichten für KI-Systeme. Dieser Skill
legt die Leitplanken fest.

## Wann anwenden

Sobald Daten natürlicher Personen im Spiel sind oder eine Ausgabe an Dritte geht.

## Rechtsrahmen im Überblick (Stand 09/2026)

### DSGVO / BDSG (DE), DSG (AT), revDSG (CH)

- Verarbeitung braucht eine Rechtsgrundlage – im Maklergeschäft meist
  Vertrag/Vertragsanbahnung (Art. 6 Abs. 1 lit. b DSGVO) oder berechtigtes
  Interesse (lit. f), bei Werbung und Newslettern Einwilligung (lit. a)
- **Datenminimierung:** nur was für den Zweck nötig ist
- **Zweckbindung:** Interessentendaten aus Objekt A nicht ungefragt für Objekt B
- **Löschfristen:** nach Zweckfortfall, unter Beachtung handels- und
  steuerrechtlicher Aufbewahrungspflichten
- **Auftragsverarbeitung:** wird ein externer KI-Dienst genutzt, braucht es einen
  AV-Vertrag (Art. 28 DSGVO) und Klarheit über Serverstandort und Training

### EU AI Act – was seit 02.08.2026 gilt

- **Transparenzpflichten (Art. 50):** Menschen müssen erkennen können, dass sie
  mit einem KI-System kommunizieren; KI-erzeugte Inhalte sind maschinenlesbar
  als solche zu markieren
- **KI-Kompetenz (Art. 4):** Beschäftigte, die das System einsetzen, sollen
  entsprechend geschult sein
- **Hochrisiko-Pflichten nach Anhang III wurden verschoben** (nach aktuellem
  Stand auf Dezember 2027), Anhang I auf 2028 – das entbindet nicht von der
  Vorbereitung, insbesondere bei bonitätsnahen Anwendungen

> Der AI Act ist 2026/2027 in Bewegung. Fristen und Einstufungen vor jedem
> produktiven Rollout aktuell prüfen und den Stand dokumentieren.

### Wo es für Immobilien heikel wird

| Anwendung | Einordnung |
|---|---|
| Bewertung eines Objekts | unkritisch, sofern keine Personendaten im Ergebnis |
| Exposé-Erstellung | unkritisch, aber keine Mieterdaten ins Exposé |
| **Bonitäts- oder Scoring-Entscheidung über Mietinteressenten** | kritisch – Art. 22 DSGVO (automatisierte Einzelentscheidung) und potenziell hochrisikonah; nie vollautomatisch entscheiden |
| **Auswahl/Ablehnung von Mietbewerbern** | kritisch – Diskriminierungsrisiko, AGG beachten; Entscheidung immer beim Menschen |
| Mieterkommunikation, Mahnwesen | Personendaten, Zweckbindung, Protokollierung |

## Vorgehen

1. **Vor der Verarbeitung fragen:** Brauche ich diese Personendaten für die
   Aufgabe? Wenn nein – nicht anfordern, nicht speichern, nicht ausgeben.
2. **Pseudonymisieren, wo möglich.** In Bewertungen und Analysen genügen
   „Mieter 1, Mieter 2" statt Namen; in Mieterlisten reichen Einheit, Fläche,
   Miete, Vertragsbeginn, Befristung.
3. **Sensible Kategorien meiden.** Gesundheit, Religion, ethnische Herkunft,
   Gewerkschaftszugehörigkeit, sexuelle Orientierung (Art. 9 DSGVO) gehören
   nie in Objekt- oder Interessentenunterlagen – auch nicht als Nebenbemerkung.
4. **Bei Bewerberauswahl und Bonität:** Der Agent bereitet auf und
   strukturiert, er entscheidet nicht und erstellt keine Rangfolge, die faktisch
   die Entscheidung vorwegnimmt. Ausgabe als neutrale Übersicht der
   selbstauskunftsrelevanten Angaben, Entscheidung beim Menschen.
5. **Kennzeichnen.** Von der KI erstellte Texte, die nach außen gehen, werden
   im Prozess als KI-Entwurf markiert. Für veröffentlichte Inhalte prüfen, ob
   eine Kennzeichnung nach Art. 50 AI Act erforderlich ist.
6. **Protokollieren.** Für jede erzeugte Ausgabe festhalten: Zeitpunkt,
   Eingangsdaten, verwendete Skills, Modellversion, freigebende Person.

## Regeln

- Keine Personendaten in Ausgaben, die dort nichts zu suchen haben
  (Exposé, Portalinserat, Wertgutachten für Dritte).
- Keine Mieterlisten mit Klarnamen an Kaufinteressenten – Namen erst im
  Datenraum nach unterzeichneter NDA und mit Rechtsgrundlage.
- Keine Bewertung von Personen, nur von Objekten und Sachverhalten.
- Keine Weitergabe von Daten in Systeme, deren Verarbeitungsort und
  Trainingsnutzung unklar sind.
- Wird der Agent nach einer Rechtsfrage des Datenschutzrechts gefragt, gibt er
  die Struktur wieder und verweist auf Datenschutzbeauftragte bzw. Anwalt.

## Ausgabeformat

Bei Aufgaben mit Personendatenbezug endet die Antwort mit einem kurzen Hinweis:

```
## Datenschutzhinweis
Verarbeitete Personendaten: <Kategorien>
Rechtsgrundlage (anzugeben durch die verantwortliche Stelle): <Vorschlag>
Nicht in die Ausgabe übernommen: <was bewusst weggelassen wurde>
```

## Qualitätskontrolle

- [ ] Keine überflüssigen Personendaten in der Ausgabe
- [ ] Keine besonderen Kategorien nach Art. 9 DSGVO
- [ ] Keine automatisierte Entscheidung über Personen
- [ ] Bei Außenwirkung: Kennzeichnung/Freigabe geregelt
- [ ] Rechtsstand des AI Act als „Stand 09/2026, in Änderung" gekennzeichnet

## Grenzen

Keine Rechtsberatung. Für Verarbeitungsverzeichnis, AV-Verträge,
Datenschutz-Folgenabschätzung und AI-Act-Einstufung ist fachlicher Rat
einzuholen.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
