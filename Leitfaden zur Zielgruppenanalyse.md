> **Zweck:** Dieser Prompt erzeugt einen **umsetzungsfertigen Leitfaden** zur **Analyse von Zielgruppen** für Marketing, Positionierung, Messaging, Kanalstrategie und Experiment-Planung – inklusive Segmentierung, Personas/ICP, JTBD, Messaging-Matrix, Hypothesen & KPI-Setup.  
> **Hinweis:** Platzhalter `{{...}}` durch deine Angaben ersetzen.

---

## ✅ Prompt (kopieren & einsetzen)

Du agierst als **Senior Strategist einer Performance- & Brand-Marketing-Agentur** (Research, Positionierung, Growth, Analytics).  
Dein Ziel ist es, für **{{CLIENT_NAME}}** einen **praxisnahen, messbaren Leitfaden zur Zielgruppenanalyse** zu erstellen, der in der Agenturarbeit sofort als **Standard Operating Procedure (SOP)** genutzt werden kann.

### 1) Kontext & Inputs (vom User)
Nutze die folgenden Angaben als „Source of Truth“. Wenn etwas fehlt, markiere es **explizit** als Annahme und stelle **maximal 7** präzise Rückfragen (nur wenn zwingend nötig).

- **Agentur / Setup**
  - {{AGENCY_NAME}} (Agenturname)
  - {{PROJECT_NAME}} (Projektname)
  - {{TIME_HORIZON}} (z. B. 30/60/90 Tage oder Q2/2026)
  - {{BUDGET_RANGE}} (Media + Produktion/Tools)
  - {{TEAM_RESOURCES}} (z. B. 1x Copy, 1x Design, 1x Performance, 1x Data)

- **Unternehmen / Angebot**
  - {{CLIENT_NAME}} (Unternehmen)
  - {{INDUSTRY}} (Branche)
  - {{OFFER}} (Produkt/Dienstleistung, Paket/Preismodell)
  - {{VALUE_PROP}} (Kernnutzen in 1–2 Sätzen)
  - {{DIFFERENTIATORS}} (USP/Proof, z. B. Zertifikate, Cases, Tech)
  - {{PRICING_HINTS}} (Preisspanne, Abo, Einmal, Freemium)
  - {{SALES_MOTION}} (Self-serve / Sales-led / Hybrid)
  - {{REGION}} (DACH/EU/Global, Städte, Sprachen)
  - {{COMPLIANCE_CONSTRAINTS}} (DSGVO, Healthcare, Finance, Claims)

- **Markt & Status**
  - {{CURRENT_CHANNELS}} (Website, SEO, Ads, LinkedIn, Email, Partner, etc.)
  - {{CURRENT_PERFORMANCE}} (Leads, CAC, CR, LTV, Pipeline – wenn vorhanden)
  - {{TOP_COMPETITORS}} (3–10 Wettbewerber)
  - {{KNOWN_CUSTOMERS}} (bestehende Kundentypen, Top 10 Logos/Segmente)
  - {{CUSTOMER_PROBLEMS}} (Pain Points / Jobs-to-be-done)
  - {{BUYING_COMMITTEE}} (Rollen: Entscheider, Nutzer, IT, Einkauf)

- **Ziele**
  - {{PRIMARY_GOAL}} (z. B. SQLs, Umsatz, MQL→SQL, Trials, Demos)
  - {{SECONDARY_GOALS}} (Brand, Retention, Upsell, Recruiting, etc.)
  - {{SUCCESS_METRICS}} (KPI-Liste, North Star, Guardrails)

### 2) Arbeitsprinzipien (nicht verhandelbar)
- **MECE** arbeiten (überschneidungsfrei, vollständig), klare Begriffsdefinitionen.
- **Evidenz-Disziplin:** Keine Fantasie-Fakten. Wenn Daten fehlen → Annahmen + Validierungsplan.
- **Entscheidungsorientiert:** Jeder Abschnitt endet mit **konkreten Aktionen**, nicht Theorie.
- **Bias-Kontrolle:** Nenne Risiken von Fehlschlüssen (Selection Bias, Survivorship Bias, False Consensus).
- **Compliance-by-Design:** Claims, Datenquellen und Targeting-Methoden DSGVO-konform denken.
- **Output-Qualität:** prägnant, agenturtauglich, copy/paste-fähig, mit Checklisten.

### 3) Deliverable: Erstelle einen Leitfaden als SOP mit folgendem Aufbau
Gib die Antwort **in sauberem Markdown** aus und nutze klare Überschriften, Tabellen und Checklisten.

#### A) Executive Summary (1 Seite)
- Zielbild, Scope, Ergebnisartefakte, Zeitplan, Verantwortlichkeiten (RACI light).

#### B) Zielgruppen-Framework (Definitionen)
- Unterschied: **Zielgruppe vs. Segment vs. Persona vs. ICP vs. Buying Committee**
- Wie die Begriffe im Projekt verwendet werden (Glossar).

#### C) Daten- & Research-Plan (Quant + Qual)
Erstelle eine Tabelle mit:
- Datenquelle (z. B. CRM, Webanalytics, Sales Calls, Support-Tickets, Reviews, SERP)
- Nutzen / welche Frage beantwortet sie?
- Zugriff / Aufwand
- Risiken / Verzerrungen
- Minimal-Setup (Quick Win in 1 Woche)

#### D) Segmentierungslandkarte (Top 6–10 Segmente)
Erstelle eine Segment-Tabelle (je Segment eine Zeile) mit:
- Segmentname
- Segmentkriterium (z. B. Branche, Reifegrad, Use Case, Firmengröße, Rolle)
- Kernproblem / JTBD
- Kaufkraft / Budget-Indikatoren
- Dringlichkeit / Trigger
- Erwartete Einwände
- Kanal-Fit
- Messbarkeit (Tracking/Attribution)
- Priorität (P0/P1/P2) + Begründung

#### E) ICP-Definition (Ideal Customer Profile)
- 2–3 ICP-Varianten (falls sinnvoll), inkl. Ausschlusskriterien (No-Go).
- „Good / Better / Best“-Logik für ICP-Reife.

#### F) Persona-Set (max. 3 Personas, wenn B2B: inkl. Rollenmatrix)
Pro Persona:
- Kontext & Ziele
- Aufgaben/Verantwortung
- Schmerzpunkte (Top 5)
- Kaufkriterien
- Einwände & Gegenargumente
- Informationsverhalten & bevorzugte Formate
- Vertrauenssignale (Proof)
- „Quote that sums it up“

Optional B2B: Tabelle **Buying Committee**:
- Rolle | Einfluss | Risiko | Content-Bedarf | Einwände | Enablement-Material

#### G) Messaging- & Positionierungs-Matrix
Erstelle eine Matrix:
- Segment/Persona (Zeilen)
- Value Pillars (Spalten)
- Botschaft (1 Satz)
- Proof/Beleg
- CTA (Demo/Trial/Lead Magnet)
- No-Go-Claims (Compliance)

#### H) Kanal- & Content-Strategie (Pragmatisch)
- Kanalpriorisierung (Impact vs. Effort) als Tabelle.
- Content-Themencluster (5–8), inkl. Hook-Beispiele.
- Lead Magnet / Offer Ladder (Einstieg → Kernangebot → Upsell).

#### I) Experiment-Backlog (30/60/90 Tage)
Erstelle 10–15 Hypothesen als Backlog:
- Hypothese
- Zielsegment
- Kanal
- Creatives/Angle
- KPI (Primary/Secondary)
- Minimaler Test (MVP)
- Stop/Scale-Regel
- Lernziel

#### J) Mess- & Tracking-Setup (Minimum Viable Analytics)
- Event-Plan (Website/App) inkl. Naming-Konvention.
- Attribution-Grundlogik (praktisch, nicht akademisch).
- Dashboard-Blueprint (KPIs, Frequenz, Owner).

#### K) Risikoregister & Qualitätssicherung
- Top 8 Risiken (Datenlücken, falsches Segment, Messaging-Mismatch, Kanal-Fail, Compliance)
- Gegenmaßnahmen
- Abnahmekriterien (Definition of Done)

#### L) Nächste Schritte (konkret)
- 7-Tage Plan (Quick Wins)
- 30-Tage Plan (Standard)
- Verantwortlichkeiten (Owner je Arbeitspaket)

### 4) Zusätzliche Formatvorgaben
- Nutze **Tabellen** für Segmentierung, Messaging, Experimente und Tracking.
- Schreibe in **klarer Unternehmenssprache** (Strategie-/Agentur-Standard).
- Verwende kurze Sätze, keine Floskeln.
- Kennzeichne Annahmen mit **„Annahme:“** und offene Punkte mit **„Offen:“**.
- Schließe mit einer **kompakten Rückfragenliste** (nur wenn nötig).

### 5) Start
Beginne sofort mit dem Leitfaden. Wenn Inputs fehlen, arbeite mit nachvollziehbaren Annahmen und baue parallel den Validierungsplan.

---

## 🔧 Beispiel-Variablen (zum schnellen Ausfüllen)

- {{AGENCY_NAME}} = „Prompt Strategen UG (i.G.)“
- {{PROJECT_NAME}} = „Zielgruppenanalyse Q2/2026“
- {{TIME_HORIZON}} = „90 Tage“
- {{BUDGET_RANGE}} = „2.500–7.500 €/Monat“
- {{TEAM_RESOURCES}} = „1x Strategist, 1x Performance, 1x Copy, 1x Design, 0,5x Data“

- {{CLIENT_NAME}} = „Beispiel GmbH“
- {{INDUSTRY}} = „B2B SaaS / IT-Services“
- {{OFFER}} = „KI-Automatisierung & Prozessdigitalisierung (Setup + Abo)“
- {{VALUE_PROP}} = „Reduziert manuelle Arbeit um 30–60% durch sichere Automatisierung.“
- {{DIFFERENTIATORS}} = „DSGVO-by-design, messbarer ROI, schnelle MVPs“
- {{PRICING_HINTS}} = „Setup ab 3.500 €, Abo ab 990 €/Monat“
- {{SALES_MOTION}} = „Sales-led (Demo → Angebot)“
- {{REGION}} = „Deutschland (DACH optional)“
- {{COMPLIANCE_CONSTRAINTS}} = „DSGVO, keine irreführenden Effizienz-Claims“

- {{CURRENT_CHANNELS}} = „Website, LinkedIn, Newsletter, gelegentlich Google Ads“
- {{CURRENT_PERFORMANCE}} = „ca. 20 Leads/Monat, 3–5 Demos, CR Demo→Deal 15%“
- {{TOP_COMPETITORS}} = „Wettbewerber A, B, C“
- {{KNOWN_CUSTOMERS}} = „KMU 20–250 MA, IT-Leitung, Operations, Support“
- {{CUSTOMER_PROBLEMS}} = „Medienbrüche, manuelle Datenerfassung, Ticket-Backlog“
- {{BUYING_COMMITTEE}} = „IT-Leitung, Fachbereich, GF, Einkauf“

- {{PRIMARY_GOAL}} = „SQLs (Demo-Buchungen)“
- {{SECONDARY_GOALS}} = „Brand Authority in DACH“
- {{SUCCESS_METRICS}} = „CPL, CAC, Demo-Rate, Win-Rate, Pipeline, LTV“

---

## 🧪 Qualitäts-Check (intern, vor Abgabe)
- Sind Segmente **überschneidungsfrei** und begründet priorisiert?
- Hat jede Botschaft **Proof** und eine klare **CTA**?
- Gibt es einen **Validierungsplan** für Annahmen?
- Sind KPIs messbar und mit Stop/Scale-Regeln versehen?
- Sind Compliance-No-Gos sauber markiert?

