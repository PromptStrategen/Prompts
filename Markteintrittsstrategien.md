## Variablen (User-Input Platzhalter)
> **Hinweis:** Alles in `{{...}}` sind Platzhalter. Der User ersetzt sie vor Ausführung.

- `{{AGENTUR_NAME}}` = z. B. „Prompt Strategen“
- `{{KUNDE_NAME}}` = z. B. „Muster GmbH“
- `{{PRODUKT_SERVICE}}` = z. B. „B2B SaaS für automatisierte Rechnungsprüfung“
- `{{KATEGORIE}}` = z. B. „FinTech / Accounting Automation“
- `{{ZIELMARKT_REGION}}` = z. B. „DACH“, „Deutschland“, „EU“, „USA“
- `{{START_DATUM}}` = z. B. „2026-03-01“
- `{{ZEITHORIZONT}}` = z. B. „90 Tage“, „6 Monate“, „12 Monate“
- `{{BUDGET_GESAMT}}` = z. B. „150.000 €“
- `{{TEAM_SETUP}}` = z. B. „1 Growth Lead, 1 Performance Marketer, 1 Content, 1 Sales (SDR), 0.5 Designer“
- `{{ZIELE}}` = z. B. „10 Pilotkunden, 2 Enterprise-Deals, CAC < 1.200 €, Payback < 4 Monate“
- `{{ICP}}` = z. B. „KMU 50–500 MA, Finance/Operations, DACH, digital affin“
- `{{BUYER_PERSONAS}}` = z. B. „CFO, Head of Finance, Ops Lead, IT-Leiter“
- `{{PROBLEM_STATEMENTS}}` = z. B. „Manuelle Prüfprozesse, hohe Fehlerquote, Medienbrüche, Audit-Risiken“
- `{{WETTBEWERBER_LISTE}}` = z. B. „Competitor A, Competitor B, Inhouse/Excel“
- `{{DIFFERENZIERUNG}}` = z. B. „Audit-Ready, DSGVO-by-design, 14 Tage Time-to-Value“
- `{{PREISMODELL}}` = z. B. „Abo pro Standort + Setup Fee“
- `{{REGULATORIK_COMPLIANCE}}` = z. B. „DSGVO, GoBD, ISO27001 (Ziel), SOC2 (später)“
- `{{VERTRIEBSKANAELE_BESTEHEND}}` = z. B. „LinkedIn Outbound, Partner, Inbound SEO“
- `{{BESTEHENDE_ASSETS}}` = z. B. „Website, 3 Case Studies, 1 Whitepaper, 0 Webinare“
- `{{EINZIGARTIGE_EVIDENZ}}` = z. B. „ROI Case: -35% Bearbeitungszeit, -60% Fehlerquote“
- `{{RISIKO_TOLERANZ}}` = z. B. „konservativ“, „balanced“, „aggressiv“
- `{{SPRACHE_TONALITAET}}` = z. B. „Deutsch, B2B, präzise, seriös“

---

## System / Rolle
Du agierst als **Senior Growth Strategist einer Marketingagentur** plus **Business Analyst** und **Go-to-Market Lead**.  
Ziel: Eine **umsetzbare Markteintrittsstrategie** mit klaren Entscheidungen, Prioritäten, Budgets, Risiken, Messsystem und 90-Tage-Plan.

---

## Hauptprompt (kopieren & verwenden)

**Aufgabe:** Erstelle eine Markteintrittsstrategie für `{{KUNDE_NAME}}` mit dem Angebot `{{PRODUKT_SERVICE}}` in `{{ZIELMARKT_REGION}}` ab `{{START_DATUM}}` für `{{ZEITHORIZONT}}`. Nutze Best Practices moderner GTM-Strategie (Segmentierung, Positionierung, ICP, Channel-Mix, Experimente, KPIs, Unit Economics, Risiko-Management).

### Kontext (Input)
- Agentur: `{{AGENTUR_NAME}}`
- Kunde/Produkt: `{{KUNDE_NAME}}` – `{{PRODUKT_SERVICE}}` (Kategorie: `{{KATEGORIE}}`)
- Ziele: `{{ZIELE}}`
- Budget & Team: `{{BUDGET_GESAMT}}` | `{{TEAM_SETUP}}`
- ICP: `{{ICP}}`
- Buyer Personas: `{{BUYER_PERSONAS}}`
- Probleme/Jobs-to-be-done: `{{PROBLEM_STATEMENTS}}`
- Wettbewerb: `{{WETTWERBER_LISTE}}`
- Differenzierung: `{{DIFFERENZIERUNG}}`
- Preis & Packaging: `{{PREISMODELL}}`
- Compliance/Regulatorik: `{{REGULATORIK_COMPLIANCE}}`
- Bestehende Kanäle/Assets: `{{VERTRIEBSKANAELE_BESTEHEND}}` | `{{BESTEHENDE_ASSETS}}`
- Evidenz/Proof: `{{EINZIGARTIGE_EVIDENZ}}`
- Risiko-Toleranz: `{{RISIKO_TOLERANZ}}`
- Sprache/Tonalität: `{{SPRACHE_TONALITAET}}`

---

## Arbeitsanweisung (Qualitätsstandard)
1. **Erst denken, dann liefern:** Triff Annahmen nur, wenn nötig, und markiere sie als *Annahme*.
2. **Keine generischen Tipps:** Alles muss auf `{{KUNDE_NAME}}` und `{{ZIELMARKT_REGION}}` zugeschnitten sein.
3. **Entscheidungsorientiert:** Liefere klare Empfehlungen + Alternativen + Trade-offs.
4. **Messbar & operativ:** Jede Initiative bekommt KPIs, Owner, Aufwand, Kostenrahmen, erwarteten Impact.
5. **90-Tage Execution:** Liefere einen sprintfähigen Plan (Wochen 1–2, 3–4, 5–8, 9–12).
6. **Konsistenzcheck:** Positionierung ↔ ICP ↔ Channels ↔ Angebot ↔ Pricing ↔ KPI-Model.

---

## Output-Format (muss exakt so strukturiert sein)

### 1) Executive Summary (1 Seite)
- Marktchance in `{{ZIELMARKT_REGION}}` (qualitativ)
- Strategische These (1–2 Sätze)
- Top 5 Entscheidungen (Was tun wir / was tun wir NICHT)
- Erfolgskriterien in Zahlen (KPIs + Zielwerte)
- Hauptrisiken + Gegenmaßnahmen

### 2) Markt- & Wettbewerbslogik (kompakt, aber scharf)
- Marktsegmente (3–6) inkl. Attraktivitätsrating
- Wettbewerbslandkarte: direkte/indirekte Alternativen + „Status Quo“
- Differenzierungs-Matrix: *Wertversprechen* vs. *Proof/Evidenz*
- Eintrittsbarrieren (Regulatorik, Switching Costs, Vertrauen, Procurement)

### 3) ICP & Positionierung (GTM-Kern)
- ICP-Split: **Primary ICP** + 1–2 Secondary ICPs
- Buyer-Persona-Map: Trigger, Einwände, Kaufkriterien, Dealbreaker
- Messaging House:
  - One-liner
  - 3 Value Pillars
  - Proof Points
  - Objection-handling (Top 7)
- Kategorie-Design (falls sinnvoll): „Wir sind X, nicht Y“

### 4) Angebot, Packaging & Pricing (Go-to-Market-Fit)
- Empfohlenes Angebotspaket (Starter/Growth/Enterprise) + enthaltene Deliverables
- Preislogik (Value Metric) + Begründung
- Pilot/POC-Design: Dauer, Scope, Erfolgskriterien, Exit-Kriterien
- Risk Reversal (Garantie/Onboarding/SLAs) passend zu `{{RISIKO_TOLERANZ}}`

### 5) Channel-Strategie (Priorisierung + Playbooks)
Baue einen 3-Level-Mix:
- **Tier 1 (Startkanäle, 80% Fokus):** max. 2 Kanäle
- **Tier 2 (skalierend, 20% Fokus):** 1–2 Kanäle
- **Tier 3 (später):** Liste + Trigger für Start

Für jeden Tier-1/2 Kanal:
- Ziel (Awareness / Demand / Pipeline / Revenue)
- Zielgruppe & Hook
- Kernangebot/CTA
- Taktiken (3–7) inkl. Frequenz
- Setup-Anforderungen (Tracking, Landingpages, CRM)
- KPI-Stack (Leading/ Lagging)
- Risiken (z. B. CAC-Spike) + Mitigation

### 6) Sales Motion & Funnel Design (B2B-ready)
- Funnel-Stufen (Visit → Lead → MQL → SQL → Close → Expansion)
- Definitionen (MQL/SQL Kriterien)
- Sales Motion: PLG vs. Sales-led vs. Hybrid (Empfehlung)
- Outbound-Sequenzen (kurz skizziert): 2 Varianten
- Enablement: One-Pager, Deck, Case Study, Security Sheet (Checkliste)

### 7) Operating Model (Budget, Team, Prozesse)
- Budget-Aufteilung: Acquisition/Content/Tools/Events/Partners/Contingency
- Team-Rollen & Verantwortlichkeiten (RACI light)
- Meeting-Cadence: Weekly Growth, Sales Pipeline, Monthly Review
- Tooling: CRM, Analytics, Attribution (minimalistisch)

### 8) Experimente & Roadmap (90 Tage)
- 10–15 Experimente als Backlog, priorisiert nach ICE (Impact/Confidence/Effort)
- Konkreter 90-Tage-Plan:
  - Wochen 1–2: Foundations
  - Wochen 3–4: Launch
  - Wochen 5–8: Iterate/Scale
  - Wochen 9–12: Optimize/Expand
Jede Woche: Deliverables, Owner, KPI, Entscheidungs-Checkpoint

### 9) KPI-System & Unit Economics (Management-ready)
- North Star Metric
- KPI-Tree (Input → Output → Outcome)
- Zielwerte (Benchmarks als Annahme markieren)
- CAC, Payback, LTV (Formeln + Beispielrechnung mit plausiblen Annahmen)
- Reporting-Template (Tabellenform)

### 10) Risiko-Register & Compliance (exec-sicher)
- Top 8 Risiken (Go-to-Market, Produkt, Legal, Brand)
- Wahrscheinlichkeit/Impact/Maßnahmen
- DSGVO/Compliance To-dos aus `{{REGULATORIK_COMPLIANCE}}` abgeleitet

### 11) Deliverables-Liste (Agentur-Paket)
- Was liefert `{{AGENTUR_NAME}}` konkret (Assets, Kampagnen, Setup, Reporting)
- Timeline + Abnahme-Kriterien
- Optional: Retainer-Phase nach 90 Tagen (Ziele & Scope)

---

## Zusätzliche Constraints
- Schreibe in `{{SPRACHE_TONALITAET}}`.
- Nutze klare Überschriften, Tabellen wo sinnvoll.
- Keine Füllwörter, keine Buzzword-Paraden ohne Inhalt.
- Wenn Input unvollständig ist: liefere **2 Strategiemodi**
  1) *Conservative* (low risk)
  2) *Aggressive* (fast learning)
  Und vergleiche.

---

## Abschluss
Beende mit:
- „Top 3 Next Actions (48h)“
- „Top 3 Entscheidungen, die der Kunde heute treffen muss“
- „Frühwarnindikatoren (wenn’s schief läuft)“
