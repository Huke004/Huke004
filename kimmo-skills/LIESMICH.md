# 25 eigenständige Skills für einen Immobilien-KI-Agenten (DACH)

**Diese Datei ist reine Orientierung. Für den Betrieb wird sie nicht gebraucht.**
Jeder Ordner enthält genau eine `SKILL.md`, und jede dieser Dateien funktioniert
für sich allein – ohne Manifest, ohne Router, ohne Beilagen, ohne Verweise auf
andere Skills.

```
kimmo-skills/
├── LIESMICH.md                  ← optional
├── agent-grundregeln/SKILL.md
├── qualitaetssicherung/SKILL.md
└── …  (25 Ordner, je eine SKILL.md)
```

## Verwendung

Einen Ordner nehmen und dorthin legen, wo die jeweilige Umgebung Skills sucht –
oder den Inhalt der `SKILL.md` direkt als System-Prompt bzw. Tool-Instruktion
verwenden. Mehrere Skills lassen sich kombinieren; nötig ist es nicht.

| Umgebung | Vorgehen |
|---|---|
| Claude Skills / Claude Code | Ordner in das Skills-Verzeichnis kopieren; `name` und `description` werden gelesen |
| LangChain / LlamaIndex | Dateiinhalt als Tool-Instruktion, `description` als Auswahlkriterium |
| n8n, Make, Flowise | Dateiinhalt in den System-Prompt der jeweiligen Node |
| Eigene RAG-Pipeline | `description` einbetten, Dateiinhalt als Kontext ausliefern |
| OpenAI Assistants / Agents SDK | Dateiinhalt als `instructions` eines Sub-Agents |

## Aufbau jeder Datei

```
---
name · description · version · stand · geltungsbereich
---
# Titel
## Zweck
## Grundregeln (gelten immer)     ← Guardrails, in jeder Datei enthalten
## Wann anwenden
## …fachlicher Teil…
## Vorgehen
## Regeln
## Ausgabeformat
## Qualitätskontrolle
## Grenzen
## Anhang (nur wo nötig)
```

Der Block **Grundregeln** ist in allen Fachskills identisch und enthält die
Leitplanken, die früher in eigenen Dateien standen: Auftragsklärung,
Quellenpflicht für Marktdaten und Rechtsstände, Verbot erfundener Fakten,
Kennzeichnung von Annahmen, offener Rechenweg mit Selbstprüfung,
Datensparsamkeit und die Fälle, in denen eine menschliche Freigabe nötig ist.

Vier Skills tragen diesen Block nicht, weil sie seine Langfassung *sind*:
`agent-grundregeln`, `qualitaetssicherung`, `quellen-und-recherche`,
`datenschutz-ki-compliance`.

## Die 25 Skills

### Fundament
| Skill | Inhalt |
|---|---|
| agent-grundregeln | Verhalten, Umgang mit Unsicherheit, Annahmen, Eskalation |
| qualitaetssicherung | Fünf Prüfdurchgänge vor jeder Auslieferung |
| quellen-und-recherche | Quellenlandkarte DE/AT/CH, Zitierweise, Belegpflicht |
| datenschutz-ki-compliance | DSGVO, EU AI Act, Kennzeichnung, Protokollierung |
| strukturierte-datenausgabe | JSON-Konventionen und vier vollständige Schemas im Anhang |
| dokumenten-extraktion | Grundbuch, Teilungserklärung, Energieausweis, Mietvertrag auswerten |
| human-in-the-loop | Freigabestufen 0–3, Übergabeformat, Protokollierung |

### Word
| Skill | Inhalt |
|---|---|
| word-lesen-analysieren | .docx-Aufbau, Text in Dokumentreihenfolge, Kommentare, Änderungsverfolgung |
| word-erstellen-formatieren | Formatvorlagen, Tabellen, Seitenzahlen, Inhaltsverzeichnis, Querformat |
| word-vorlagen-serienbrief | docxtpl/Jinja2, Schleifen, Serienerstellung, Prüfskript |
| word-review-kommentare | Versionsvergleich, Review-Raster für Verträge und Gutachten |

### Bewertung
| Skill | Inhalt |
|---|---|
| objektdaten-erfassung | Pflichtangaben, Unterlagenliste, Flächenbegriffe, GND/RND; Aufnahmebogen im Anhang |
| vergleichswertverfahren | ImmoWertV §§ 24–26, Bodenwert, Anpassungen, Rechenbeispiel |
| ertragswertverfahren | §§ 27–34, drei Varianten, Barwertfaktor, DCF, Rechenbeispiel |
| sachwertverfahren | §§ 35–39, BGF, NHK 2010, Alterswertminderung, Sachwertfaktor |
| verkehrswertgutachten | § 194 BauGB, Gliederung, Wertableitung, Formulierungsregeln |
| marktanalyse-lage | Makro-/Mikrolage, Fünf-Stufen-Raster, Marktdaten |
| bewertung-oesterreich-schweiz | LBG, ÖNORM, SVKG, SIA – Unterschiede zum deutschen Recht |

### Praxis
| Skill | Inhalt |
|---|---|
| expose-und-vermarktung | Exposé-Aufbau, GEG-Pflichtangaben, Provision, Bildrechte; Gerüst im Anhang |
| rendite-und-finanzierung | Kaufnebenkosten, BAR/NAR, Cashflow, Annuität, Restschuld, Sensitivität |
| energieausweis-geg | Ausweisarten, GEG, EPBD, Effizienzklassen und Preiswirkung |
| grundbuch-und-kaufvertrag | Drei Abteilungen, Rechte und Lasten, Erbbaurecht, Kaufvertragsraster |
| mietrecht-und-mietvertrag | Vertragsraster, Mieterhöhung, Betriebskosten, Beendigung |
| weg-verwaltung | Teilungserklärung, Beschlusssammlung, Rücklage, bauliche Veränderungen |
| steuern-und-afa | AfA-Sätze, Kaufpreisaufteilung, Werbungskosten, Fristen, Erbschaftsteuer |

## Rechtsstand

Alle Inhalte haben den Stand **September 2026** und sind Arbeitsgrundlage,
keine Rechts-, Steuer- oder Bewertungsberatung.

| Thema | Fundstelle | Bemerkung |
|---|---|---|
| Verkehrswert | § 194 BauGB | stabil |
| Wertermittlung | ImmoWertV 2021, in Kraft seit 01.01.2022 | Vergleichswert §§ 24–26, Ertragswert §§ 27–34, Sachwert §§ 35–39, Bodenwert §§ 40–45, Rechte §§ 46–52 |
| Anlagen der ImmoWertV | 1 GND · 2 RND-Modernisierungsmodell · 3 Bewirtschaftungskosten · 4 NHK 2010 · 5 Bodenrichtwertgrundstück | NHK-Preisstand 2010, mit Baupreisindex fortzuschreiben |
| Anwendungshinweise | ImmoWertA, veröffentlicht 20.09.2023 | Auslegungshilfe, keine Rechtsnorm |
| **GEG / EPBD** | GEG; EPBD-Neufassung | **in Änderung** – EU-Frist 29.05.2026 abgelaufen, deutsche Novelle zu diesem Zeitpunkt nicht in Kraft |
| **EU AI Act** | VO (EU) 2024/1689 | Transparenzpflichten Art. 50 seit 02.08.2026; Hochrisiko Anhang III verschoben auf 12/2027, Anhang I auf 08/2028 |
| Provision Kauf | §§ 656a–656d BGB | Teilungsgebot bei EFH/ETW an Verbraucher |
| Provision Vermietung | WoVermRG | Bestellerprinzip, max. 2 Nettokaltmieten zzgl. USt |
| Mietrecht | §§ 535 ff. BGB, BetrKV, HeizkostenV, CO2KostAufG | Kappungsgrenzen und Mietpreisbremse landesrechtlich |
| Wohnungseigentum | WEG i. d. F. der Reform 2020 | |
| AfA | § 7 EStG | linear 2,5 / 2,0 / 3,0 % nach Fertigstellungsjahr; degressiv 5 % bei Baubeginn 01.10.2023–30.09.2029 |
| Weitere Steuer | §§ 6, 7b, 7h, 7i, 23 EStG; GrEStG; GrStG; ErbStG/BewG | Grunderwerbsteuer 3,5–6,5 % je Bundesland |
| Österreich | LBG, ÖNORM B 1802 ff., B 1800, MRG | |
| Schweiz | SVKG/SEK-SVIT-Standard, SIA 416, OR/ZGB, kantonales Steuerrecht | |

**Vor produktivem Einsatz prüfen und danach halbjährlich wiederholen.** Geänderte
Inhalte in der betroffenen `SKILL.md` anpassen und dort `version` sowie `stand`
hochsetzen. Marktdaten (Bodenrichtwerte, Liegenschaftszinssätze, NHK-Indexierung,
Mietspiegel) gehören nicht in die Skills, sondern in die Recherche zum Einzelfall –
so steht es auch in den Grundregeln jeder Datei.
