# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## Zweck

Dieses Repo enthält automatisiert erstellte Marktbeobachtungs-Reports für die ÖPNV-IT-Branche. Ein Scheduled Claude Code Trigger recherchiert relevante Nachrichten und speichert strukturierte Markdown-Reports.

## Zielunternehmen

**INIT SE** – weltweit führender Anbieter von IT-Lösungen für den öffentlichen Nahverkehr.
Produkte: ITCS/Betriebsleitsysteme, Ticketing & Fahrgeldmanagement, Fahrgastinformation, E-Mobilität, Mobilitätsplattformen.
Produktnamen: COPILOTpc, EVENDpc, MOBILEstatistics, MOBILEcharge, RESPONSEassist, regiomove.

## Nutzerin

Projektmanagerin bei INIT SE – verantwortlich für die Implementierung von INIT-Lösungen bei Verkehrsbetrieben in Deutschland.

---

## Beobachtungsfelder

### 1. ÖPNV-Branche
- Politische Entscheidungen (Finanzierung, Regionalisierungsgesetz, Deutschlandticket)
- Ausschreibungen für IT-Systeme bei Verkehrsbetrieben
- Fusionen, Übernahmen, Kooperationen
- Branchenverbände (VDV, UITP)

### 2. Wettbewerber
**DACH:**
- IVU Traffic Technologies (Berlin) – ITCS, Planungssysteme
- Trapeze Group (Schweiz) – ITCS, Fahrgastinformation
- Scheidt & Bachmann (Mönchengladbach) – Ticketing, Parking

**International:**
- Cubic Transportation Systems (USA) – Fare Collection, Open Payment
- Conduent Transportation (USA) – Fare Collection, Transit
- Masabi (UK) – Mobile Ticketing, Fare Payments as a Service
- Vix Technology (Australien) – Fare Collection, Smart Cards
- Littlepay (UK) – Open Payment, cEMV Transit

### 3. Technologie & Innovation
- Account-Based Ticketing (ABT), Open Payment, cEMV
- KI/ML im ÖPNV (Echtzeitprognosen, Disposition, Nachfragesteuerung)
- V2X-Kommunikation, Buspriorisierung
- Mobility as a Service (MaaS), Multimodalität
- E-Bus-Integration, Lademanagement
- Open Data, GTFS/GTFS-RT, NeTEx/SIRI

### 4. Verkehrsbetriebe (Deutschland)
BVG Berlin, MVG München, SSB Stuttgart, KVB Köln, VGF Frankfurt, üstra Hannover, DVB Dresden, BSAG Bremen, Hamburger Hochbahn, Rheinbahn Düsseldorf, ESWE Wiesbaden, VAG Nürnberg, SWB Bonn.
Weitere VBs nach Ergänzung durch die Nutzerin.

---

## Report-Format

### Regulärer Report (`reports/regular/YYYY-MM-DD.md`)

```markdown
# Marktbeobachtung ÖPNV – YYYY-MM-DD

## Highlights
- Bullet Points mit **Firmennamen**, [Quellen](url), Sprach-Tags [EN]

## Wettbewerber
- Aktivitäten der Konkurrenz

## Technologie & Innovation
- Neue Technologien, Pilotprojekte, Forschung

## Regulierung & Politik
- Gesetze, Förderungen, Finanzierungsentscheidungen

## Verkehrsbetriebe
- Nachrichten über konkrete VBs, Ausschreibungen, Projekte

## Einordnung
| Bereich | Handlungsempfehlung |
|---|---|
| Projektmanagement | ... |
| Vertrieb | ... |
| Technik | ... |
```

### Wochen-Digest (`reports/weekly/YYYY-WXX.md`)

Am Donnerstag statt regulärem Report, wenn es eine volle Woche zu bewerten gibt:

```markdown
# Wochen-Digest KW XX/YYYY

## Top 3 der Woche
1. ...

## Wettbewerber-Aktivität
| Unternehmen | Aktivität | Quelle |
|---|---|---|

## Trend-Bewertung
- ↑ Aufwärts: ...
- → Stabil: ...
- ↓ Abwärts: ...

## Empfehlungen
- ...
```

---

## Recherche-Regeln

- **Max 6–8 Web-Searches pro Lauf**
- **Sprachen:** Deutsch (primär), Englisch für internationale Quellen
- **Sprach-Tags:** `[EN]` an englischsprachige Einträge
- **Quellen:** Immer als Markdown-Link `[Quelle](url)` angeben
- **Firmennamen** fett markieren: `**IVU Traffic Technologies**`
- **Keine Duplikate** zu den letzten 2–3 Reports prüfen (git log lesen)
- **Kompakte Bullet Points** – keine ausschweifenden Absätze
- **Einordnung:** Konkrete Handlungsempfehlungen für Projektmanagement, Vertrieb, Technik
- Fokus auf **Relevanz für INIT SE** – nicht jede ÖPNV-Nachricht ist relevant

## Commit-Konvention

- Regulär: `report: Marktbeobachtung YYYY-MM-DD`
- Weekly: `report: Wochen-Digest KW XX`

---

## Befehle

```bash
git log --oneline -10    # Letzte Reports prüfen (Duplikat-Check)
ls reports/regular/      # Vorhandene reguläre Reports
ls reports/weekly/       # Vorhandene Wochen-Digests
```
