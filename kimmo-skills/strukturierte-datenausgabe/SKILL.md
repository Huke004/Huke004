---
name: strukturierte-datenausgabe
description: Ergebnisse maschinenlesbar ausgeben – JSON-Schemas für Objektdaten, Bewertungsergebnis, Mieterliste und Exposé. Nutzen bei API-Anbindung, CRM-Import, Datenbank, Schnittstelle, Weiterverarbeitung durch andere Systeme.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Strukturierte Datenausgabe

## Zweck

Ein Agent, dessen Ergebnisse nur als Fließtext existieren, ist eine Sackgasse.
Dieser Skill definiert stabile Datenstrukturen, damit Ergebnisse in CRM,
Datenbank, Portal-Schnittstelle oder Folgeprozesse laufen können.

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

- Der Nutzer nennt JSON, API, Schnittstelle, Import, CRM, Datenbank, Tabelle
- Der Agent ist Teil einer Pipeline und liefert an ein anderes System
- Wiederkehrende Objektaufnahmen sollen vergleichbar gespeichert werden

## Vorgehen

1. Passendes Schema aus dem Abschnitt „Schemas" unten wählen
2. Nur belegte Felder füllen; unbekannte Felder auf `null`, **nicht raten**
3. Jedes wertbestimmende Feld bekommt einen Eintrag in `quellen`
4. Ausgabe als **reines JSON ohne umgebenden Text**, wenn maschinell
   weiterverarbeitet wird; sonst JSON im Codeblock plus kurze Erläuterung
5. Gegen das Schema validieren (Pflichtfelder, Typen, Einheiten)

## Konventionen

| Thema | Regel |
|---|---|
| Zahlen | JSON-Number, Punkt als Dezimaltrenner, **kein** Tausendertrenner |
| Währung | separates Feld `waehrung` (`EUR`, `CHF`) |
| Einheiten | im Feldnamen (`wohnflaeche_qm`, `miete_netto_monat`, `zins_prozent`) |
| Datum | ISO 8601 `JJJJ-MM-TT` |
| Unbekannt | `null`, nie `0`, nie `"k.A."` |
| Annahme | in `annahmen[]`, nicht stillschweigend im Wert |
| Aufzählungen | feste Enums, klein geschrieben |

## Schemas

Vier Schemas, jeweils als Kurzform hier und vollständig im Anhang dieser Datei:

| Schema | Inhalt |
|---|---|
| **objekt** | Bewertungsobjekt: Stammdaten, Flächen, Zustand, Rechte und Lasten |
| **bewertung** | Bewertungsergebnis inklusive Rechenweg, Annahmen, Freigabestatus |
| **mieterliste** | Mietvertragsdaten, pseudonymisiert |
| **expose** | Vermarktungsdaten, an OpenImmo anschlussfähig |

### Kurzform Objekt

```json
{
  "objekt_id": "2026-0142",
  "adresse": {"strasse": "Musterweg 12", "plz": "44801", "ort": "Bochum", "land": "DE"},
  "objektart": "einfamilienhaus",
  "baujahr": 1978,
  "modernisierungen": [{"jahr": 2015, "gewerk": "heizung"}],
  "grundstuecksflaeche_qm": 520,
  "wohnflaeche_qm": 142.5,
  "flaechenbasis": "wofliv",
  "zimmer": 5,
  "energie": {"ausweisart": "verbrauch", "kennwert_kwh_qm_a": 148, "klasse": "E"},
  "rechte_lasten": [{"abteilung": "II", "art": "wegerecht", "beschreibung": "..."}],
  "quellen": [
    {"feld": "wohnflaeche_qm", "quelle": "Aufmaß Bauplan 1978", "stand": "2026-08-14"}
  ],
  "annahmen": []
}
```

### Kurzform Bewertungsergebnis

```json
{
  "objekt_id": "2026-0142",
  "stichtag": "2026-09-01",
  "wertbegriff": "verkehrswert",
  "zweck": "kaufpreisfindung",
  "waehrung": "EUR",
  "verfahren": [
    {
      "art": "sachwert",
      "ergebnis": 468000,
      "eingangsgroessen": {
        "bodenwert": 218400,
        "nhk_qm": 1150,
        "bruttogrundflaeche_qm": 240,
        "alterswertminderung_prozent": 38,
        "sachwertfaktor": 1.05
      }
    },
    {"art": "vergleichswert", "ergebnis": 495000, "anzahl_vergleichsfaelle": 6}
  ],
  "ergebnis": {
    "wert": 480000,
    "spanne_von": 455000,
    "spanne_bis": 505000,
    "rundung": "auf volle 5.000 EUR",
    "begruendung_gewichtung": "Vergleichswert führend, Sachwert stützend"
  },
  "kennzahlen": {"eur_pro_qm_wohnflaeche": 3368, "bodenwertanteil_prozent": 45.5},
  "annahmen": ["Restnutzungsdauer 45 Jahre angenommen, da Modernisierungsumfang nicht belegt"],
  "freigabe_erforderlich": true
}
```

## Portalstandard OpenImmo

Für die Übergabe an Immobilienportale im deutschsprachigen Raum ist **OpenImmo**
(XML) der verbreitete Austauschstandard. Der Agent liefert die Inhalte in der
`expose.schema.json`-Struktur; die Abbildung auf OpenImmo-XML übernimmt der
anschließende Export.

## Regeln

- **Nie ein Feld erfinden, um das Schema zu füllen.** Unbekannt bleibt `null`.
- Rechenwege gehören mit ins Ergebnisobjekt (`eingangsgroessen`), damit das
  Ergebnis nachvollziehbar und reproduzierbar bleibt.
- Schemaänderungen versionieren (`schema_version`), nie Feldbedeutungen still
  umdefinieren.
- Personenbezogene Felder nur, wenn zwingend (siehe Grundregeln, Personendaten).
  Mieterlisten standardmäßig pseudonymisiert (`mieter_ref: "M-03"`).

## Qualitätskontrolle

- [ ] JSON syntaktisch gültig und gegen das Schema validiert
- [ ] Pflichtfelder gefüllt, Unbekanntes auf `null`
- [ ] Einheiten in Feldnamen, Zahlen ohne Tausendertrenner
- [ ] Quellen und Annahmen befüllt
- [ ] Keine unnötigen Personendaten

## Grenzen

Definiert Struktur, nicht Fachinhalt. Wie die Werte zustande kommen, steht in
den Bewertungs-Skills.


## Anhang: vollständige JSON-Schemas

Die vier Schemas im Volltext. Sie sind Teil dieser Datei; es muss nichts
nachgeladen werden. Beim Anpassen `schema_version` erhöhen.

### Objekt — `objekt.schema.json`

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "urn:kimmo:schema:objekt",
  "title": "Bewertungsobjekt",
  "description": "Stammdaten eines Immobilienobjekts fuer Bewertung und Vermarktung im DACH-Raum.",
  "type": "object",
  "required": ["objekt_id", "adresse", "objektart", "schema_version"],
  "properties": {
    "schema_version": { "type": "string", "const": "1.0.0" },
    "objekt_id": { "type": "string", "description": "Interne Akten-/Vorgangsnummer" },
    "erfasst_am": { "type": "string", "format": "date" },
    "adresse": {
      "type": "object",
      "required": ["ort", "land"],
      "properties": {
        "strasse": { "type": ["string", "null"] },
        "plz": { "type": ["string", "null"] },
        "ort": { "type": "string" },
        "ortsteil": { "type": ["string", "null"] },
        "land": { "type": "string", "enum": ["DE", "AT", "CH"] },
        "bundesland_kanton": { "type": ["string", "null"] }
      }
    },
    "grundbuch": {
      "type": ["object", "null"],
      "properties": {
        "amtsgericht": { "type": ["string", "null"] },
        "gemarkung": { "type": ["string", "null"] },
        "blatt": { "type": ["string", "null"] },
        "flur": { "type": ["string", "null"] },
        "flurstueck": { "type": ["string", "null"] },
        "auszug_stand": { "type": ["string", "null"], "format": "date" }
      }
    },
    "objektart": {
      "type": "string",
      "enum": [
        "einfamilienhaus", "doppelhaushaelfte", "reihenhaus", "zweifamilienhaus",
        "mehrfamilienhaus", "eigentumswohnung", "wohn_und_geschaeftshaus",
        "buero", "einzelhandel", "logistik", "hotel", "spezialimmobilie",
        "unbebautes_grundstueck", "erbbaurecht"
      ]
    },
    "baujahr": { "type": ["integer", "null"], "minimum": 1000, "maximum": 2100 },
    "modernisierungen": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["gewerk"],
        "properties": {
          "jahr": { "type": ["integer", "null"] },
          "gewerk": {
            "type": "string",
            "enum": ["dach", "fassade_daemmung", "fenster", "heizung", "leitungen",
                     "baeder", "innenausbau", "grundriss", "elektro", "sonstiges"]
          },
          "beleg": { "type": ["string", "null"] }
        }
      }
    },
    "grundstuecksflaeche_qm": { "type": ["number", "null"], "minimum": 0 },
    "wohnflaeche_qm": { "type": ["number", "null"], "minimum": 0 },
    "nutzflaeche_qm": { "type": ["number", "null"], "minimum": 0 },
    "bruttogrundflaeche_qm": { "type": ["number", "null"], "minimum": 0 },
    "flaechenbasis": {
      "type": ["string", "null"],
      "enum": ["wofliv", "din277", "oenorm_b1800", "sia416", "geschaetzt", null],
      "description": "Rechtsgrundlage der Flaechenermittlung. WoFlV = Wohnflaechenverordnung (DE)."
    },
    "zimmer": { "type": ["number", "null"] },
    "geschosse": { "type": ["integer", "null"] },
    "keller": { "type": ["string", "null"], "enum": ["voll", "teil", "kein", null] },
    "stellplaetze": {
      "type": ["object", "null"],
      "properties": {
        "garage": { "type": ["integer", "null"] },
        "carport": { "type": ["integer", "null"] },
        "aussen": { "type": ["integer", "null"] },
        "tiefgarage": { "type": ["integer", "null"] }
      }
    },
    "zustand": {
      "type": ["string", "null"],
      "enum": ["neuwertig", "gepflegt", "normal", "renovierungsbeduerftig",
               "sanierungsbeduerftig", "abbruchreif", null]
    },
    "restnutzungsdauer_jahre": { "type": ["number", "null"] },
    "gesamtnutzungsdauer_jahre": { "type": ["number", "null"] },
    "baurecht": {
      "type": ["object", "null"],
      "properties": {
        "grundlage": { "type": ["string", "null"], "enum": ["bplan", "par34_baugb", "par35_baugb", "zonenplan", "flaechenwidmung", null] },
        "grz": { "type": ["number", "null"] },
        "gfz": { "type": ["number", "null"] },
        "zulaessige_nutzung": { "type": ["string", "null"] }
      }
    },
    "energie": {
      "type": ["object", "null"],
      "properties": {
        "ausweisart": { "type": ["string", "null"], "enum": ["bedarf", "verbrauch", "keiner", null] },
        "kennwert_kwh_qm_a": { "type": ["number", "null"] },
        "klasse": { "type": ["string", "null"] },
        "energietraeger": { "type": ["string", "null"] },
        "baujahr_heizung": { "type": ["integer", "null"] },
        "gueltig_bis": { "type": ["string", "null"], "format": "date" }
      }
    },
    "rechte_lasten": {
      "type": "array",
      "description": "Grundbuchliche Rechte und Lasten sowie Baulasten.",
      "items": {
        "type": "object",
        "required": ["art"],
        "properties": {
          "abteilung": { "type": ["string", "null"], "enum": ["II", "III", "baulastenverzeichnis", null] },
          "art": { "type": "string" },
          "beschreibung": { "type": ["string", "null"] },
          "wertrelevanz": { "type": ["string", "null"], "enum": ["wertmindernd", "werterhoehend", "neutral", "unklar", null] },
          "betrag_eur": { "type": ["number", "null"] }
        }
      }
    },
    "vermietung": {
      "type": ["object", "null"],
      "properties": {
        "status": { "type": ["string", "null"], "enum": ["eigennutzung", "vermietet", "teilvermietet", "leerstand", null] },
        "jahresnettokaltmiete_ist_eur": { "type": ["number", "null"] },
        "jahresnettokaltmiete_soll_eur": { "type": ["number", "null"] },
        "leerstandsquote_prozent": { "type": ["number", "null"] }
      }
    },
    "besonderheiten": {
      "type": "array",
      "items": { "type": "string" },
      "description": "Denkmalschutz, Altlastenverdacht, Erbbaurecht, Wohnrecht, Bauschaeden, Hochwasserzone usw."
    },
    "quellen": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["feld", "quelle"],
        "properties": {
          "feld": { "type": "string" },
          "quelle": { "type": "string" },
          "stand": { "type": ["string", "null"], "format": "date" }
        }
      }
    },
    "annahmen": { "type": "array", "items": { "type": "string" } }
  },
  "additionalProperties": false
}
```

### Bewertungsergebnis — `bewertung.schema.json`

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "urn:kimmo:schema:bewertung",
  "title": "Bewertungsergebnis",
  "description": "Ergebnis einer Wertermittlung inklusive Rechenweg, Annahmen und Freigabestatus.",
  "type": "object",
  "required": ["schema_version", "objekt_id", "stichtag", "wertbegriff", "zweck", "waehrung", "verfahren", "ergebnis"],
  "properties": {
    "schema_version": { "type": "string", "const": "1.0.0" },
    "objekt_id": { "type": "string" },
    "stichtag": { "type": "string", "format": "date", "description": "Wertermittlungsstichtag" },
    "qualitaetsstichtag": { "type": ["string", "null"], "format": "date" },
    "wertbegriff": {
      "type": "string",
      "enum": ["verkehrswert", "marktwert", "beleihungswert", "kaufpreisindikation",
               "versicherungswert", "steuerwert", "investitionswert"]
    },
    "zweck": {
      "type": "string",
      "enum": ["kaufpreisfindung", "finanzierung", "erbauseinandersetzung", "scheidung",
               "steuerlich", "bilanzierung", "gericht", "zwangsversteigerung", "intern"]
    },
    "waehrung": { "type": "string", "enum": ["EUR", "CHF"] },
    "ortsbesichtigung": {
      "type": ["object", "null"],
      "properties": {
        "durchgefuehrt": { "type": "boolean" },
        "datum": { "type": ["string", "null"], "format": "date" },
        "umfang": { "type": ["string", "null"], "enum": ["innen_und_aussen", "nur_aussen", "unterlagen", null] }
      }
    },
    "verfahren": {
      "type": "array",
      "minItems": 1,
      "items": {
        "type": "object",
        "required": ["art", "ergebnis"],
        "properties": {
          "art": { "type": "string", "enum": ["vergleichswert", "ertragswert", "sachwert", "dcf", "residualwert", "liquidationswert"] },
          "ergebnis": { "type": "number" },
          "gewichtung_prozent": { "type": ["number", "null"], "minimum": 0, "maximum": 100 },
          "rolle": { "type": ["string", "null"], "enum": ["fuehrend", "stuetzend", "kontrolle", null] },
          "eingangsgroessen": {
            "type": "object",
            "description": "Alle Rechengroessen mit sprechenden Feldnamen inkl. Einheit im Namen.",
            "additionalProperties": { "type": ["number", "string", "null"] }
          },
          "rechenweg": { "type": ["string", "null"], "description": "Formel und Zwischenschritte im Klartext" },
          "anzahl_vergleichsfaelle": { "type": ["integer", "null"] }
        }
      }
    },
    "besondere_objektspezifische_grundstuecksmerkmale": {
      "type": "array",
      "description": "boG nach ImmoWertV: Zu- und Abschlaege, die nicht bereits im Verfahren erfasst sind.",
      "items": {
        "type": "object",
        "required": ["bezeichnung", "betrag_eur"],
        "properties": {
          "bezeichnung": { "type": "string" },
          "betrag_eur": { "type": "number" },
          "herleitung": { "type": ["string", "null"] }
        }
      }
    },
    "ergebnis": {
      "type": "object",
      "required": ["wert"],
      "properties": {
        "wert": { "type": "number" },
        "spanne_von": { "type": ["number", "null"] },
        "spanne_bis": { "type": ["number", "null"] },
        "rundung": { "type": ["string", "null"] },
        "begruendung_gewichtung": { "type": ["string", "null"] }
      }
    },
    "kennzahlen": {
      "type": ["object", "null"],
      "properties": {
        "eur_pro_qm_wohnflaeche": { "type": ["number", "null"] },
        "bodenwertanteil_prozent": { "type": ["number", "null"] },
        "faktor_kaufpreis_jahresnettokaltmiete": { "type": ["number", "null"] },
        "bruttoanfangsrendite_prozent": { "type": ["number", "null"] }
      }
    },
    "sensitivitaet": {
      "type": "array",
      "description": "Wirkung der Variation kritischer Eingangsgroessen auf das Ergebnis.",
      "items": {
        "type": "object",
        "properties": {
          "groesse": { "type": "string" },
          "von": { "type": "number" },
          "bis": { "type": "number" },
          "wert_von": { "type": "number" },
          "wert_bis": { "type": "number" }
        }
      }
    },
    "quellen": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["groesse", "quelle"],
        "properties": {
          "groesse": { "type": "string" },
          "quelle": { "type": "string" },
          "stand": { "type": ["string", "null"], "format": "date" }
        }
      }
    },
    "annahmen": { "type": "array", "items": { "type": "string" } },
    "fehlende_unterlagen": { "type": "array", "items": { "type": "string" } },
    "freigabe_erforderlich": { "type": "boolean", "default": true },
    "freigabe": {
      "type": ["object", "null"],
      "properties": {
        "durch": { "type": ["string", "null"] },
        "am": { "type": ["string", "null"], "format": "date" },
        "rolle": { "type": ["string", "null"] }
      }
    },
    "erstellt_durch": {
      "type": ["object", "null"],
      "description": "Nachvollziehbarkeit der KI-Erzeugung (AI-Act-Transparenz).",
      "properties": {
        "system": { "type": ["string", "null"] },
        "modell": { "type": ["string", "null"] },
        "skills": { "type": "array", "items": { "type": "string" } },
        "zeitpunkt": { "type": ["string", "null"], "format": "date-time" }
      }
    }
  },
  "additionalProperties": false
}
```

### Mieterliste (pseudonymisiert) — `mieterliste.schema.json`

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "urn:kimmo:schema:mieterliste",
  "title": "Mieterliste (pseudonymisiert)",
  "description": "Mietvertragsdaten eines Objekts. Standardmaessig ohne Klarnamen.",
  "type": "object",
  "required": ["schema_version", "objekt_id", "stand", "einheiten"],
  "properties": {
    "schema_version": { "type": "string", "const": "1.0.0" },
    "objekt_id": { "type": "string" },
    "stand": { "type": "string", "format": "date" },
    "waehrung": { "type": "string", "enum": ["EUR", "CHF"], "default": "EUR" },
    "einheiten": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["einheit_ref", "nutzungsart"],
        "properties": {
          "einheit_ref": { "type": "string", "description": "z. B. 'WE-03' oder 'EG links'" },
          "mieter_ref": { "type": ["string", "null"], "description": "Pseudonym, z. B. 'M-03'. Klarnamen nur mit Rechtsgrundlage." },
          "nutzungsart": { "type": "string", "enum": ["wohnen", "buero", "einzelhandel", "gewerbe", "lager", "stellplatz", "sonstiges"] },
          "flaeche_qm": { "type": ["number", "null"] },
          "nettokaltmiete_monat": { "type": ["number", "null"] },
          "nebenkosten_vorauszahlung_monat": { "type": ["number", "null"] },
          "miete_pro_qm": { "type": ["number", "null"] },
          "vertragsbeginn": { "type": ["string", "null"], "format": "date" },
          "befristet_bis": { "type": ["string", "null"], "format": "date" },
          "mietart": { "type": ["string", "null"], "enum": ["unbefristet", "befristet", "staffel", "index", null] },
          "naechste_anpassung": { "type": ["string", "null"], "format": "date" },
          "kaution_vorhanden": { "type": ["boolean", "null"] },
          "leerstand": { "type": ["boolean", "null"] },
          "marktmiete_geschaetzt_qm": { "type": ["number", "null"] },
          "bemerkung": { "type": ["string", "null"] }
        }
      }
    },
    "summen": {
      "type": ["object", "null"],
      "properties": {
        "flaeche_gesamt_qm": { "type": ["number", "null"] },
        "jahresnettokaltmiete_ist": { "type": ["number", "null"] },
        "jahresnettokaltmiete_soll": { "type": ["number", "null"] },
        "leerstandsquote_prozent": { "type": ["number", "null"] },
        "mietsteigerungspotenzial_prozent": { "type": ["number", "null"] }
      }
    },
    "quellen": { "type": "array", "items": { "type": "string" } },
    "annahmen": { "type": "array", "items": { "type": "string" } }
  },
  "additionalProperties": false
}
```

### Exposé- und Vermarktungsdaten — `expose.schema.json`

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "urn:kimmo:schema:expose",
  "title": "Expose- und Vermarktungsdaten",
  "description": "Vermarktungsrelevante Daten eines Objekts. Feldnamen sind an OpenImmo anschlussfaehig gehalten.",
  "type": "object",
  "required": ["schema_version", "objekt_id", "vermarktungsart", "texte", "pflichtangaben"],
  "properties": {
    "schema_version": { "type": "string", "const": "1.0.0" },
    "objekt_id": { "type": "string" },
    "vermarktungsart": { "type": "string", "enum": ["kauf", "miete", "erbpacht"] },
    "preis": {
      "type": ["object", "null"],
      "properties": {
        "kaufpreis": { "type": ["number", "null"] },
        "nettokaltmiete_monat": { "type": ["number", "null"] },
        "nebenkosten_monat": { "type": ["number", "null"] },
        "heizkosten_enthalten": { "type": ["boolean", "null"] },
        "kaution": { "type": ["number", "null"] },
        "provision_kaeufer_prozent": { "type": ["number", "null"] },
        "provision_hinweis": { "type": ["string", "null"] },
        "waehrung": { "type": "string", "enum": ["EUR", "CHF"], "default": "EUR" }
      }
    },
    "texte": {
      "type": "object",
      "required": ["ueberschrift", "objektbeschreibung"],
      "properties": {
        "ueberschrift": { "type": "string", "maxLength": 100 },
        "objektbeschreibung": { "type": "string" },
        "ausstattung": { "type": ["string", "null"] },
        "lagebeschreibung": { "type": ["string", "null"] },
        "sonstiges": { "type": ["string", "null"] }
      }
    },
    "pflichtangaben": {
      "type": "object",
      "description": "Gesetzliche Pflichtangaben in Immobilienanzeigen (DE: GEG; AT/CH analog).",
      "required": ["energieausweis_vorhanden"],
      "properties": {
        "energieausweis_vorhanden": { "type": "boolean" },
        "ausweisart": { "type": ["string", "null"], "enum": ["bedarf", "verbrauch", null] },
        "endenergiebedarf_kwh_qm_a": { "type": ["number", "null"] },
        "energieverbrauchskennwert_kwh_qm_a": { "type": ["number", "null"] },
        "warmwasser_enthalten": { "type": ["boolean", "null"] },
        "energietraeger": { "type": ["string", "null"] },
        "baujahr_laut_ausweis": { "type": ["integer", "null"] },
        "energieeffizienzklasse": { "type": ["string", "null"] },
        "ausnahme_grund": { "type": ["string", "null"], "description": "z. B. Denkmalschutz" }
      }
    },
    "medien": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "art": { "type": "string", "enum": ["foto", "grundriss", "lageplan", "video", "rundgang", "dokument"] },
          "datei": { "type": "string" },
          "titel": { "type": ["string", "null"] },
          "reihenfolge": { "type": ["integer", "null"] },
          "urheber_geklaert": { "type": ["boolean", "null"] }
        }
      }
    },
    "verfuegbar_ab": { "type": ["string", "null"], "format": "date" },
    "kontakt": {
      "type": ["object", "null"],
      "properties": {
        "firma": { "type": ["string", "null"] },
        "ansprechpartner": { "type": ["string", "null"] },
        "telefon": { "type": ["string", "null"] },
        "email": { "type": ["string", "null"] }
      }
    },
    "hinweise": { "type": "array", "items": { "type": "string" } }
  },
  "additionalProperties": false
}
```

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
