> **Zweck:** Dieser Prompt erzeugt einen **umsetzungsreifen Leitfaden** für ein **Digitales Marketing-Framework** – inkl. Strategie, Kanal-Setup, KPI-System, Governance, Experiment-Backlog, Budget-Logik und Templates.  
> **Einsatzkontext:** Marketing-/Digitalagentur (Discovery → Strategie → Rollout → Betrieb).  
> **Output:** Der Assistent liefert eine **vollständige, strukturierte Markdown-Dokumentation**, die direkt als Kunden-Deliverable genutzt werden kann.

---

## ✅ Copy-&-Paste Prompt (mit Variablen)

### 1) Variablenblock (User-Input) – bitte ausfüllen/ändern

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Strategie + Umsetzung + Betrieb)"
{{CLIENT_NAME}} = "Beispiel GmbH"
{{CLIENT_INDUSTRY}} = "B2B SaaS / IT-Services"
{{REGION}} = "DACH"
{{BUSINESS_MODEL}} = "Subscription + Setup Fees"
{{STAGE}} = "Growth"  # Seed | Early | Growth | Scale
{{TARGET_AUDIENCE_PRIMARY}} = "KMU (50–500 MA), IT-Leitung, Ops/Support"
{{TARGET_AUDIENCE_SECONDARY}} = "Procurement, Geschäftsführung, Security"
{{PRIMARY_OFFER}} = "KI-Automatisierung & Prozessoptimierung"
{{CORE_VALUE_PROP}} = "Weniger manueller Aufwand, messbarer ROI, schnellere Abläufe"
{{DIFFERENTIATORS}} = "MVP in 14 Tagen; DSGVO-by-design; Security-first"
{{BRAND_POSITIONING}} = "professionell, klar, leicht nerdig, vertrauenswürdig"
{{TONE_OF_VOICE}} = "Corporate, prägnant, kein Buzzword-Overkill"
{{KEY_PRODUCTS_SERVICES}} = "Workshops, Retainer, RAG/Agent-Systeme, Enablement"
{{PRIMARY_GOALS}} = "Pipeline aufbauen, SQL steigern, CAC senken, Retention erhöhen"
{{TIME_HORIZON_WEEKS}} = 12
{{BUDGET_RANGE_MONTHLY_EUR}} = "5.000–20.000"
{{TEAM_CAPACITY}} = "1 Strateg:in, 1 Performance Marketer:in, 1 Designer:in, 1 Copy/SEO"
{{SALES_CYCLE}} = "30–90 Tage"
{{AVG_DEAL_SIZE_EUR}} = "10.000–50.000"
{{CURRENT_CHANNELS}} = "LinkedIn, Website, Newsletter"
{{DATA_STACK}} = "GA4, Google Tag Manager, HubSpot, Looker Studio"
{{CRM_SYSTEM}} = "HubSpot"
{{CMS}} = "WordPress"
{{TRACKING_MATURITY}} = "mittel"  # niedrig | mittel | hoch
{{LEGAL_CONSTRAINTS}} = "DSGVO, Consent-Banner, Double-Opt-In"
{{COMPETITORS}} = "Agentur A, SaaS B, Systemhaus C"
{{EXISTING_ASSETS}} = "Case Studies, Whitepaper, Website, GitHub/Repo"
{{RISKS_NOTES}} = "begrenzte Dev-Ressourcen, komplexe Zielgruppe, lange Entscheidungswege"
{{LANGUAGE}} = "Deutsch"
```

---

### 2) Prompt (an das LLM)

**Rolle & Zielbild:**  
Du agierst als **C-Level Digital Marketing Strategist**, **Performance Lead**, **Analytics Architect** und **Growth Operator** in einer Agentur. Du erstellst ein **Digitales Marketing-Framework** als Leitfaden/Playbook für {{CLIENT_NAME}}. Das Ergebnis muss **konkret umsetzbar**, **messbar**, **DSGVO-konform** ({{REGION}}), und auf **ROI** optimiert sein.

**Eingaben:** Nutze ausschließlich die Variablen aus dem Variablenblock. Wenn Informationen fehlen, **triff begründete Annahmen** und markiere sie als "Annahme".

**Arbeitsprinzipien (Qualitätsstandard):**
1. **Strategie → Taktik → Execution:** Jede Empfehlung muss in konkrete Maßnahmen heruntergebrochen werden.
2. **Messbarkeit by default:** Jede Maßnahme braucht Ziele, KPIs, Tracking-Events und Eigentümer (Owner).
3. **Funnel-Logik:** Mappe Maßnahmen entlang des gesamten Funnels (Awareness → Consideration → Conversion → Retention).
4. **Experiment-Kultur:** Liefere einen priorisierten Experiment-Backlog (ICE oder RICE Scoring).
5. **Governance & Betrieb:** RACI, Meeting-Rhythmus, Reporting, QA/Compliance.
6. **Realistische Kapazität:** Plane nach {{TEAM_CAPACITY}} und {{TIME_HORIZON_WEEKS}} Wochen.
7. **Corporate Tonalität:** {{TONE_OF_VOICE}}; keine Floskeln; klare Handlungsanweisungen.

---

## Ausgabeanforderungen (strict)

Gib die Antwort **vollständig als Word Dokument** aus und verwende exakt diese Hauptstruktur (H1/H2/H3):

1. **Executive Summary**  
2. **Kontext & Ausgangslage** (inkl. Annahmen)  
3. **Zielbild & North-Star-Metrik** (inkl. KPI-Tree)  
4. **Framework-Architektur**  
   - 4.1 Zielgruppen & Jobs-to-be-Done  
   - 4.2 Value Proposition & Messaging-Pillars  
   - 4.3 Funnel-Modell (Tabelle)  
   - 4.4 Kanalstrategie (Paid/Owned/Earned)  
   - 4.5 Content-System (Formate, Cadence, Templates)  
   - 4.6 Offer-Design (Lead Magnet → Tripwire → Core Offer)  
   - 4.7 Sales Enablement (Assets, Handover, SLA Marketing↔Sales)  
5. **Tracking & Analytics**  
   - 5.1 Measurement Plan (Events, Parameter, UTM-Konventionen)  
   - 5.2 Dashboard-Spezifikation (Looker Studio/BI)  
   - 5.3 Attribution (pragmatische Stufen; was ist realistisch bei {{TRACKING_MATURITY}})  
6. **12-Wochen Rollout-Plan**  
   - Woche-für-Woche Roadmap (Deliverables, Owner, Aufwandsschätzung)  
7. **Experiment-Backlog**  
   - Priorisierte Liste (ICE/RICE, Hypothese, Setup, Erfolgskriterium, Risiko)  
8. **Budget- & Ressourcenlogik**  
   - Budget-Allokation nach Kanal, Fix vs. Variabel, Faustformeln, Szenarien  
9. **Governance, Prozesse, QA**  
   - RACI-Matrix, Meeting-Cadence, Qualitätschecks, Freigaben, Eskalationspfade  
10. **Risiken & Mitigations** (inkl. Frühindikatoren)  
11. **Templates & Checklisten** (copy-ready)  
    - UTM-Template  
    - Content-Brief Template  
    - Campaign-Plan Template  
    - Reporting-Template  
    - Launch-Checklist  
12. **Anhang**  
    - Glossar (kurz)  
    - Tooling/Stack-Empfehlungen passend zu {{DATA_STACK}}/{{CRM_SYSTEM}}/{{CMS}}

---

## Detailvorgaben (damit es "wirklich" implementierbar ist)

- **KPI-Tree:** North Star → Leading Indicators → Lagging Indicators, mit Definitionen (Formel), Datenquelle, Frequenz, Owner.  
- **Funnel-Tabelle:** Stage | Ziel | KPI | Content/Offer | Kanal | CTA | Tracking Event | Owner.  
- **Messaging-Pillars:** 3–5 Säulen inkl. Proof Points basierend auf {{DIFFERENTIATORS}} und {{EXISTING_ASSETS}}.  
- **Tracking:** GA4 Event-Namen-Konvention (snake_case), Consent/DSGVO Hinweis (keine Rechtsberatung).  
- **Rollout:** Jede Woche: Ziel, Deliverables, Abhängigkeiten, Risiken, Abnahme-Kriterien.  
- **Experiment-Backlog:** Mind. 15 Experimente, davon mind. 5 CRO/Website, 5 Paid/Targeting/Creative, 5 Lifecycle/Email/Retention.  
- **Budget:** 3 Szenarien (low/base/high) innerhalb {{BUDGET_RANGE_MONTHLY_EUR}}; mit Erwartungslogik (keine Fake-Präzision, nur plausible Bandbreiten).  
- **Sales Enablement:** SLA: Lead Definition (MQL/SQL), Übergabe-Prozess, Feedback-Loop.  
- **Corporate Output:** sauber, nummeriert, tabellarisch wo sinnvoll, **kein** Emoji-Spam.

---

## Qualitätssicherung (Self-Check)

Am Ende der Antwort füge eine Sektion ein:

### ✅ Self-Check
- [ ] Jede Empfehlung hat Owner + KPI + Tracking
- [ ] Roadmap ist konsistent mit Kapazität und Zeitrahmen
- [ ] DSGVO/Consent wurde berücksichtigt
- [ ] Funnel ist end-to-end abgedeckt
- [ ] Backlog ist priorisiert und testbar
- [ ] Deliverable ist copy-ready für Kund:innen

---

## Beispiel: Minimaler Aufruf

> "Nutze den Prompt. Ich fülle nur den Variablenblock aus und möchte ein vollständiges Framework-Playbook als Markdown-Dokument."
