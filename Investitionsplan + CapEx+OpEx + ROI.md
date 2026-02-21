## Variablen (User-Input als Platzhalter)
- {{AGENCY_NAME}} = z. B. "Prompt Strategen Marketing GmbH"
- {{COUNTRY}} = z. B. "Deutschland"
- {{CURRENCY}} = z. B. "EUR"
- {{PLANNING_HORIZON_MONTHS}} = z. B. 24
- {{START_DATE}} = z. B. "2026-03-01"
- {{AGENCY_STAGE}} = z. B. "Early Stage (0–10 Kunden)" | "Growth" | "Established"
- {{SERVICE_LINES}} = z. B. "Performance Marketing, SEO, CRM-Automation, Content, KI-Workflows"
- {{TARGET_CUSTOMERS}} = z. B. "KMU bis 500 MA, B2B, DACH"
- {{CURRENT_REVENUE_MRR}} = z. B. 25000
- {{CURRENT_GROSS_MARGIN_PCT}} = z. B. 55
- {{CURRENT_FIXED_COSTS_MONTHLY}} = z. B. 18000
- {{CURRENT_HEADCOUNT}} = z. B. 6
- {{MAX_BUDGET_TOTAL}} = z. B. 80000
- {{CASH_ON_HAND}} = z. B. 35000
- {{FUNDING_OPTIONS}} = z. B. "Bootstrapped; optional: KfW, Bankkredit, Gesellschafterdarlehen"
- {{RISK_TOLERANCE}} = z. B. "niedrig" | "mittel" | "hoch"
- {{INVESTMENT_GOALS}} = z. B. "Skalierung Delivery, Umsatzwachstum, Automatisierung, Qualität, Security/DSGVO"
- {{PRIORITY_CONSTRAINTS}} = z. B. "DSGVO-by-design, kein Vendor Lock-in, Payback <= 12 Monate"
- {{TEAM_SKILLS}} = z. B. "Ads, SEO, Sales, Ops; begrenzte Engineering-Kapazität"
- {{TOOLS_STACK_CURRENT}} = z. B. "Google Ads, Meta, HubSpot, GA4, Looker Studio, Notion, Zapier"
- {{PIPELINE_METRICS}} = z. B. "Leads/Monat=120, Close Rate=12%, ARPA=2500, Churn=3%"
- {{GROWTH_TARGETS}} = z. B. "MRR 25k -> 60k in 12 Monaten; Marge +10pp"
- {{COMPLIANCE_REQUIREMENTS}} = z. B. "DSGVO, AVV, TOMs, ISO-Orientierung"
- {{DISCOUNT_RATE_PCT}} = z. B. 10   <!-- für NPV -->
- {{SCENARIOS}} = z. B. "Base, Downside, Upside"
- {{REPORTING_PREFERENCE}} = z. B. "tabellarisch + Executive Summary, Word Dokument"

## Beispielwerte (optional, zur Orientierung)
> {{MAX_BUDGET_TOTAL}}=80000, {{PLANNING_HORIZON_MONTHS}}=24, {{CURRENT_REVENUE_MRR}}=25000,  
> {{CURRENT_FIXED_COSTS_MONTHLY}}=18000, {{CASH_ON_HAND}}=35000, {{DISCOUNT_RATE_PCT}}=10

---

## Haupt-Prompt (kopieren & ausfüllen)

Du agierst als **CFO/FP&A Lead** und **Investitionscontroller** einer Marketing-Agentur. Ziel ist ein **entscheidungsreifer Investitionsplan** für {{AGENCY_NAME}} in {{COUNTRY}} über **{{PLANNING_HORIZON_MONTHS}} Monate** (Start: {{START_DATE}}) in {{CURRENCY}}.

### 1) Kontext & Zielbild
- Agentur-Phase: {{AGENCY_STAGE}}
- Leistungen: {{SERVICE_LINES}}
- Zielkunden: {{TARGET_CUSTOMERS}}
- Ziele: {{INVESTMENT_GOALS}}
- Constraints/Prioritäten: {{PRIORITY_CONSTRAINTS}}
- Risiko-Toleranz: {{RISK_TOLERANCE}}
- Compliance: {{COMPLIANCE_REQUIREMENTS}}
- Aktueller Stack: {{TOOLS_STACK_CURRENT}}
- Team-Skills: {{TEAM_SKILLS}}

### 2) Ausgangslage (Ist-Zahlen)
- MRR aktuell: {{CURRENT_REVENUE_MRR}}
- Bruttomarge %: {{CURRENT_GROSS_MARGIN_PCT}}
- Fixkosten/Monat: {{CURRENT_FIXED_COSTS_MONTHLY}}
- Headcount: {{CURRENT_HEADCOUNT}}
- Cash on hand: {{CASH_ON_HAND}}
- Budget-Limit gesamt: {{MAX_BUDGET_TOTAL}}
- Funding-Optionen: {{FUNDING_OPTIONS}}
- Pipeline/Go-to-Market Kennzahlen: {{PIPELINE_METRICS}}
- Wachstumsziele: {{GROWTH_TARGETS}}
- Diskontsatz (NPV): {{DISCOUNT_RATE_PCT}}%
- Szenarien: {{SCENARIOS}}

### 3) Aufgabe
Erstelle einen **Investitionsplan** (CapEx + OpEx) inkl. **Business Case** und **Umsetzungs-Roadmap**. Der Plan muss:
- **messbar** (KPIs, Zielwerte, Messlogik),
- **finanziell konsistent** (Cashflow, Runway, Budget-Deckel),
- **risikobewusst** (Risiko-Register + Mitigations),
- **operativ umsetzbar** (RACI/Governance, Meilensteine, Entscheidungstore)
sein.

### 4) Vorgehenslogik (ohne unnötige Rückfragen)
- Wenn Daten fehlen, triff **maximal 5** klare Annahmen (mit Kennzeichnung **"Annahme"**) und baue den Plan trotzdem.
- Stelle Rückfragen **nur**, wenn eine Entscheidung sonst nicht seriös möglich ist; maximal **3** Fragen am Ende.
- Keine erfundenen Quellen/Benchmarks: Falls du Benchmarks nutzt, markiere sie als **"Heuristik"**.

### 5) Output-Format (Word Dokument, strukturiert)
Liefere genau die folgenden Abschnitte:

#### A) Executive Summary (1 Seite)
- Investment-These (1–2 Sätze)
- Gesamtbudget, erwarteter ROI, Payback, Hauptrisiken
- Go/No-Go Empfehlung mit Begründung

#### B) Investitions-Portfolio (priorisiert)
Erstelle eine Tabelle:
| Rang | Initiative | Kategorie (Tech/People/Process/Marketing/Sales/Compliance) | Ziel/Nutzen | Kosten einmalig | Kosten laufend/Monat | Nutzen/Monat ({{CURRENCY}}) | Aufwand (Low/Med/High) | Risiko (Low/Med/High) | Abhängigkeiten | Start | Ende |
|---|---|---|---|---:|---:|---:|---|---|---|---|---|

Initiativen sollen typisch für eine Marketing-Agentur sein, z. B.:
- Sales/RevOps: CRM, Angebot/Vertrag-Automation, Lead-Routing, Reporting
- Delivery: SOPs, QA, Projektcontrolling, Kapazitätsplanung
- KI/Automation: Content-Workflows, Briefing->Assets, QA-Checks, RAG/Knowledge Base
- Tech: Tracking/Attribution, Data Warehouse/BI, Conse
