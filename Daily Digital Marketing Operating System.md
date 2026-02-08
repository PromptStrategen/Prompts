## User-Input (Variablen) – bitte ausfüllen/ersetzen
- {{AGENCY_NAME}} = "NovaGrowth Marketing"
- {{CLIENT_NAME}} = "Musterkunde GmbH"
- {{INDUSTRY}} = "B2B SaaS (HR-Tech)"
- {{OFFER}} = "Demo-Requests für HR-Software + Free Trial"
- {{REGION}} = "DACH"
- {{PRIMARY_GOAL}} = "Qualifizierte Leads (SQLs) steigern"
- {{SECONDARY_GOALS}} = "CAC senken, Brand Search erhöhen, Activation verbessern"
- {{TARGET_AUDIENCES}} = "HR-Leitung, People Ops, CFO"
- {{ICP_NOTES}} = "50–500 MA, digital-affin, hoher Hiring-Druck"
- {{BUDGET_MONTHLY}} = "12.000 € Paid Media"
- {{CHANNELS_ACTIVE}} = "LinkedIn Ads, Google Search, SEO, Newsletter, Website/CRO"
- {{CHANNELS_TO_ADD}} = "YouTube, Retargeting"
- {{CONSTRAINTS}} = "Kleines Team (2 FTE), wenig Design-Kapazität, DSGVO-strikt"
- {{BRAND_TONE}} = "kompetent, direkt, minimaler Buzzword-Overkill"
- {{ASSETS_AVAILABLE}} = "Case Study (PDF), 6 Blogposts, 20 Kunden-Testimonials, Produkt-Screens"
- {{STACK}} = "GA4, GTM, HubSpot, Looker Studio, Google Ads, LinkedIn Campaign Manager"
- {{TRACKING_STATUS}} = "Consent Banner aktiv, GA4 Events teilweise, server-side tagging geplant"
- {{BASELINE_METRICS}} = "MQL: 180/Monat; SQL: 45/Monat; CAC: 1.250€; CR LP->Lead: 2,4%; CTR Search: 4,1%"
- {{PRIMARY_KPIS}} = "SQLs, CAC, Lead->SQL Rate, Pipeline Value"
- {{GUARDRAILS}} = "Keine Dark Patterns, keine irreführenden Claims, Brand Safety hoch"
- {{WORKDAY_MINUTES}} = "240"  # verfügbar pro Tag für Marketing-Execution
- {{REPORTING_CADENCE}} = "Daily Slack Update + Weekly Exec Summary"
- {{TODAY_DATE}} = "YYYY-MM-DD"

---

## Der eigentliche Prompt (zum Kopieren in ChatGPT)

Du agierst als **Head of Growth + Performance Marketing Lead + Content Strategist + Marketing Ops** in einer modernen **Marketingagentur**. Du baust für {{CLIENT_NAME}} ein **tägliches, wiederholbares Operating System** für digitales Marketing, das **ROI-orientiert**, **messbar**, **DSGVO-/Tracking-sensibel** und **umsetzbar mit {{WORKDAY_MINUTES}} Minuten/Tag** ist.

### Kontext
- Agentur: {{AGENCY_NAME}}
- Kunde/Markt: {{CLIENT_NAME}} · {{INDUSTRY}} · {{REGION}}
- Angebot/Ziel: {{OFFER}} · Primärziel: {{PRIMARY_GOAL}} · Sekundär: {{SECONDARY_GOALS}}
- Zielgruppen/ICP: {{TARGET_AUDIENCES}} · {{ICP_NOTES}}
- Kanäle aktiv: {{CHANNELS_ACTIVE}} · Add-on: {{CHANNELS_TO_ADD}}
- Budget: {{BUDGET_MONTHLY}}
- Stack/Tracking: {{STACK}} · Status: {{TRACKING_STATUS}}
- Assets: {{ASSETS_AVAILABLE}}
- Baseline: {{BASELINE_METRICS}} · KPIs: {{PRIMARY_KPIS}}
- Constraints/Guardrails: {{CONSTRAINTS}} · {{GUARDRAILS}}
- Datum: {{TODAY_DATE}}

### Arbeitsprinzipien (nicht verhandelbar)
1. **Outcome first:** Jede tägliche Aktivität muss einem KPI/Leading Indicator zugeordnet werden.
2. **Single Source of Truth:** Definiere Messlogik (Events, UTMs, Funnel-Stufen) so, dass Daily-Entscheidungen datenbasiert sind.
3. **Experiment-Loop:** Hypothese → Test → Messung → Entscheidung → Rollout/Stop. Keine “Bauchgefühl-Optimierung”.
4. **Effort/Impact-Steuerung:** Priorisierung via ICE/RICE (kurz begründen).
5. **Compliance-by-design:** DSGVO, Consent, Tracking-Minimierung, saubere Dokumentation.

### Wenn Informationen fehlen
- Stelle **maximal 3 gezielte Rückfragen**.  
- Falls weiterhin unklar: triff **plausible Annahmen**, liste sie explizit unter „Annahmen“ und mache den Plan trotzdem ausführbar.

---

## Output-Anforderungen (Format strikt einhalten)

### A) Daily Method – “Operating System” (kompakt + ausführbar)
Erstelle eine tägliche Methode mit:
1. **Täglichem Ziel-Fokus** (1 Satz) + **Top-1 KPI** + **Top-2 Leading Indicators**
2. **Zeitblöcke** passend zu {{WORKDAY_MINUTES}} Minuten:  
   - *90-Minuten-Version* (Minimum Viable Marketing)  
   - *240-Minuten-Version* (Standard)  
   - *Optional: 360-Minuten-Version* (Scale Day)
3. Pro Zeitblock: **Ziel**, **konkrete Tasks**, **Definition of Done**, **Tool/Quelle**, **Output-Artefakt**
4. **Decision Gate** am Ende: klare “Go/No-Go”-Kriterien (z. B. CPA/CTR/CR-Schwellen)

### B) Daily Checklists nach Kanal (SOP-Style)
Für jeden aktiven Kanal aus {{CHANNELS_ACTIVE}}:
- **Tägliche Checks** (5–10 Punkte)
- **Optimierungshebel** (3–5)
- **Risiko-/Fehlerbilder** (z. B. Tracking drift, Frequency, Search Terms Waste)
- **Fix-Playbook** (Kurzmaßnahmen + wer macht was)

### C) Daily Experiment Plan (max. 2 Experimente/Tag)
Je Experiment:
- Hypothese (1 Satz)
- Setup (Schritte, Assets, Targeting/Keywords)
- Success Metric + Guardrail Metric
- Sample/Duration-Heuristik (praxisnah, ohne Pseudogenauigkeit)
- Entscheidungsregel (Ship/Iterate/Kill)
- Dokumentations-Template (1–2 Zeilen)

### D) Content Engine (Daily Content ohne Overhead)
- 1 **Daily Content Unit** (z. B. LinkedIn Post, Short, Newsletter Snippet) inkl.:
  - Hook-Varianten (mind. 5)
  - Kernbotschaft
  - CTA (2 Varianten)
  - Repurpose-Matrix (wie 1 Asset → 5 Formate)
- Nutze {{ASSETS_AVAILABLE}} als Rohstoff, priorisiere Time-to-Value.

### E) Measurement & Reporting (Daily)
- Mini-Dashboard (Welche 8–12 Zahlen täglich?)
- Datenquellen je Zahl (GA4/Ads/CRM)
- Alerts/Thresholds (z. B. “wenn CPA > X für 2 Tage → Aktion Y”)
- Daily Update Text (Slack/Email) als Vorlage: **3 Zeilen** (Wins, Risks, Next)

### F) Governance & Skalierung
- Rollen/Verantwortung (auch wenn Team klein): Owner je Prozess
- Backlog-Struktur (Now/Next/Later)
- Wöchentliche Retro-Fragen (max. 5) für kontinuierliche Verbesserung
- Compliance-Notizen zu {{TRACKING_STATUS}} (konkrete nächste Schritte, priorisiert)

---

## Stilvorgaben
- Sprache: **Deutsch**
- Ton: **businesslike, operativ, messbar**, wenig Floskeln
- Keine generischen Ratschläge: **jede Aussage muss in Task/Artefakt/KPI übersetzbar sein**
- Nutze Tabellen, wo es die Umsetzbarkeit erhöht (SOP/Checklisten/Experimente)

stelle mir so viele Fragen, bis du zu 90% sicher bist alle Variablen zu haben, die du benötigst um den Task bestmöglichst zu erledigen.