---
name: quellen-und-recherche
description: Woher Immobiliendaten und Rechtsstände kommen und wie sie belegt werden – Gutachterausschüsse, BORIS, Mietspiegel, Grundbuch, amtliche Quellen in DE/AT/CH. Immer aktiv, Pflicht bei jeder Zahl und jedem Paragraphen.
version: 2.0.0
stand: 2026-09
geltungsbereich: [DE, AT, CH]
---

# Quellen und Recherche

## Zweck

Immobilienbewertung ist Datenarbeit. Der Wert eines Ergebnisses hängt an der
Qualität der Eingangsdaten. Dieser Skill legt fest, welche Quelle für welche
Größe zuständig ist, wie sie zitiert wird und was passiert, wenn sie fehlt.

## Wann anwenden

Sobald eine Zahl, eine Frist, ein Prozentsatz oder eine Rechtsnorm in der
Antwort auftaucht.

## Grundregel

> **Marktdaten und Rechtsstände kommen niemals aus dem Modellwissen.**

Modellwissen ist zu einem Stichtag eingefroren, Bodenrichtwerte ändern sich
jährlich, Liegenschaftszinssätze und Mietspiegel ebenso, Gesetze laufend.
Zulässige Herkunft: Nutzerangabe, hochgeladenes Dokument, Live-Recherche,
angebundene Datenquelle. Alles andere ist eine Annahme.

## Quellenlandkarte Deutschland

| Größe | Zuständige Quelle |
|---|---|
| Bodenrichtwert | Gutachterausschuss der Gemeinde / Landes-BORIS; bundesweiter Einstieg über BORIS-D |
| Liegenschaftszinssatz | Gutachterausschuss, Grundstücksmarktbericht |
| Sachwert-/Vergleichsfaktoren, Umrechnungskoeffizienten | Gutachterausschuss |
| Kaufpreise, Umsatzzahlen, Marktentwicklung | Kaufpreissammlung / Grundstücksmarktbericht des Gutachterausschusses |
| Normalherstellungskosten | NHK 2010 i. V. m. ImmoWertV 2021 Anlage; Baupreisindex des Statistischen Bundesamtes zur Anpassung |
| Baupreisindex, Verbraucherpreisindex | Statistisches Bundesamt (Destatis) |
| Ortsübliche Vergleichsmiete | qualifizierter oder einfacher Mietspiegel der Gemeinde, Mietdatenbank, Sachverständigengutachten, drei Vergleichswohnungen |
| Eigentumsverhältnisse, Lasten, Rechte | Grundbuch (Abt. I–III), Einsicht über Grundbuchamt |
| Baurecht, zulässige Nutzung, GRZ/GFZ | Bebauungsplan / § 34, § 35 BauGB, Auskunft der Bauaufsicht |
| Altlasten | Altlastenkataster des Kreises/der Stadt |
| Baulasten | Baulastenverzeichnis (nicht in Bayern/Brandenburg – dort Dienstbarkeiten) |
| Denkmalschutz | Denkmalliste der unteren Denkmalschutzbehörde |
| Erschließung, Beiträge | Gemeinde / Tiefbauamt |
| Energiekennwerte | Energieausweis, Ausstellerdatenbank (DIBt) |
| Gesetzestexte | gesetze-im-internet.de (Bund), Landesrecht-Portale |

## Quellenlandkarte Österreich

| Größe | Quelle |
|---|---|
| Bewertungsrecht | Liegenschaftsbewertungsgesetz (LBG), ÖNORM B 1802-1 ff. |
| Kaufpreise | Grundbuch / Kaufpreissammlung, Immobilienpreisspiegel der WKO |
| Grundbuch, Kataster | Grundbuch und Grundstücksdatenbank (BEV) |
| Flächenwidmung | Flächenwidmungs- und Bebauungsplan der Gemeinde |
| Mietrecht | MRG, Richtwertgesetz (Richtwerte je Bundesland) |

## Quellenlandkarte Schweiz

| Größe | Quelle |
|---|---|
| Bewertungsstandard | SVKG/SEK-SVIT Bewertungsstandard, DCF-Methodik, SIA-Normen (u. a. SIA 416 Flächen) |
| Grundbuch | kantonales Grundbuchamt |
| Amtliche Werte, Steuerwerte | kantonale Steuerverwaltung |
| Marktdaten | kantonale Statistikämter, Bundesamt für Statistik (BFS), Wüest/IAZI-Indizes |
| Zonenplan | Bau- und Zonenordnung der Gemeinde |

## Vorgehen

1. **Bedarf listen.** Vor der Recherche notieren, welche Größen fehlen.
2. **Nutzer zuerst fragen**, wenn die Daten wahrscheinlich vorliegen
   (Grundbuchauszug, Energieausweis, Mieterliste, Teilungserklärung,
   Grundstücksmarktbericht). Das ist schneller und belastbarer als Recherche.
3. **Primärquelle vor Sekundärquelle.** Gutachterausschuss vor Maklerportal,
   Gesetzestext vor Ratgeberseite, Grundbuch vor Verkäuferangabe.
4. **Datieren.** Jede Zahl bekommt Stand und Stichtag:
   `Bodenrichtwert 420 €/m², Stand 01.01.2026, BORIS NRW, Zone …`
5. **Bei Nichtverfügbarkeit:** benennen, was fehlt, wo es zu bekommen ist und
   welche Auswirkung die Lücke auf das Ergebnis hat. Ersatzweise mit
   gekennzeichneter Annahme und Sensitivitätsangabe rechnen
   („bei einem Liegenschaftszinssatz zwischen 3,5 % und 4,5 % ergibt sich eine
   Wertspanne von … bis …").

## Zitierweise

Im Fließtext:
`(Gutachterausschuss Bochum, Grundstücksmarktbericht 2026, S. 47)`

In Gutachten und Berichten am Ende ein Quellenverzeichnis:

```
## Quellen und Unterlagen
1. Grundbuchauszug von <Amtsgericht>, Blatt <Nr.>, Stand TT.MM.JJJJ
2. Bodenrichtwert <Wert> €/m², Stichtag 01.01.JJJJ, <Gutachterausschuss>
3. Liegenschaftszinssatz <Wert> %, <Quelle, Jahr>
4. Energieausweis vom TT.MM.JJJJ, Registriernummer <…>
5. Ortsbesichtigung am TT.MM.JJJJ / keine Ortsbesichtigung durchgeführt
```

## Regeln

- Immobilienportale sind **Angebotspreise**, keine Kaufpreise. Sie taugen zur
  Markteinschätzung, nie als Vergleichspreis im Sinne des Vergleichswertverfahrens.
- Preisspiegel Dritter (Portale, Maklerverbände) nur ergänzend und mit Nennung
  der Methodik.
- Keine Zahl aus einem Suchergebnis-Snippet übernehmen, ohne die Quelle zu öffnen.
- Widersprechen sich zwei Quellen: beide nennen, die belastbarere begründet
  bevorzugen, Spanne ausweisen.
- Rechtsstände immer mit Datum. Bei laufenden Gesetzgebungsverfahren (2026 z. B.
  GEG-Novelle zur EPBD-Umsetzung) den Verfahrensstand benennen, nicht die
  geplante Fassung als geltendes Recht darstellen.

## Qualitätskontrolle

- [ ] Jede Zahl hat Quelle und Stand
- [ ] Primärquellen bevorzugt
- [ ] Angebotspreise nicht als Kaufpreise verwendet
- [ ] Rechtsstand datiert
- [ ] Quellenverzeichnis vollständig

## Grenzen

Deckt die Beschaffung ab, nicht die fachliche Verwendung – dafür die jeweiligen
Bewertungs-Skills.

---

*Eigenständige Datei. Sie enthält alles, was für diese Aufgabe nötig ist, und
setzt keine weiteren Skills, Schemas oder Vorlagen voraus.*
