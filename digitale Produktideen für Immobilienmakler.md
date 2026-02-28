> **Ziel:** Dieser Prompt erzeugt einen **strategisch belastbaren Leitfaden** zur Entwicklung und Priorisierung **digitaler Produktideen** für **Immobilienmakler** – inkl. Marktlogik, Zielgruppen‑Jobs‑to‑be‑Done, Value Proposition, MVP‑Scope, Go‑to‑Market, KPI‑Set und Umsetzungs‑Roadmap.  
> **Einsatz:** Copy‑&‑Paste in ein LLM. Variablen ausfüllen. Output ist sofort in Workshop/Präsentation/Backlog überführbar.

---

## 1) Variablenblock (User‑Input) – bitte ausfüllen/ändern

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Strategie + Umsetzung)"
{{PROJECT_NAME}} = "Digital Products for Realtors"
{{REGION}} = "DACH"
{{LANGUAGE}} = "Deutsch"

{{CLIENT_NAME}} = "Muster Makler GmbH"
{{CLIENT_TYPE}} = "Einzelmakler | Boutique | Franchise | Maklerverbund | PropTech-Partner"
{{TEAM_SIZE}} = "1-5 | 6-20 | 21-100+"
{{PRIMARY_MARKETS}} = "z.B. Berlin, München, Rhein-Main"
{{PROPERTY_FOCUS}} = "Wohnimmobilien | Gewerbe | Luxus | Investment | Neubau"
{{PRICE_SEGMENT}} = "Budget | Mid | Premium | Luxus"
{{BUSINESS_MODEL}} = "Provision | Pauschale | Hybrid | Lead-Weiterverkauf"

{{CURRENT_STACK}} = "z.B. onOffice, Propstack, Flowfact, Salesforce, HubSpot, WordPress, ImmoScout24, Immowelt, API-Zugänge"
{{DATA_AVAILABILITY}} = "Low | Medium | High (CRM sauber, Exposés strukturiert, Tracking aktiv)"
{{COMPLIANCE_LEVEL}} = "Standard DSGVO | Hoch (DPIA/AVV/ISO-orientiert)"
{{SECURITY_REQUIREMENTS}} = "z.B. SSO, Rollen, Audit-Logs, Verschlüsselung, EU-Hosting"

{{PRIMARY_OBJECTIVE}} = "Mehr Leads | Höhere Conversion | Schnellere Vermarktung | Bestandskundenbindung | Prozessautomatisierung | Upsell"
{{REVENUE_TARGET}} = "z.B. 20.000€ MRR in 12 Monaten"
{{TIME_TO_MARKET}} = "z.B. MVP in 8 Wochen"
{{BUDGET_RANGE}} = "z.B. 15k–60k initial + 1k–5k/Monat Betrieb"
{{RISK_TOLERANCE}} = "Low | Medium | High"

{{TARGET_PERSONAS}} = "z.B. Verkäufer (Privat), Vermieter, Bauträger, Käufer, Investoren"
{{PAIN_POINTS}} = "z.B. Lead-Qualität schlecht, viele Rückfragen, Exposé-Erstellung dauert, Terminchaos"
{{DIFFERENTIATORS}} = "z.B. Top-Bewertungen, Nischenfokus, schnelle Vermarktung, starke lokale Marke"

{{COMPETITORS}} = "z.B. lokale Makler, Franchise-Ketten, iBuyer/PropTechs"
{{CHANNELS}} = "SEO, Google Ads, Meta, LinkedIn, Portale, Kooperationen, E-Mail, WhatsApp"
{{ASSETS_AVAILABLE}} = "z.B. 500 Exposés, 10.000 Leads, 2 Jahre CRM-Daten, Bildmaterial, Grundrisse"
{{CONSTRAINTS}} = "z.B. keine US-Cloud, keine neue App, nur Web, nur No-Code, Team hat wenig Zeit"
```

---

## 2) Copy‑&‑Paste Prompt (an das Modell)

**Rolle & Kontext:**  
Du bist ein interdisziplinäres Expertenteam aus **Produktstrategie**, **PropTech/Immobilienvertrieb**, **Growth Marketing**, **UX**, **Data/AI** und **DSGVO/Security**. Du arbeitest im Auftrag von **{{AGENCY_NAME}}** ({{AGENCY_ROLE}}) für **{{CLIENT_NAME}}**.  
Dein Fokus ist **Business Impact**: Umsatz, Marge, Time‑to‑Value, Differenzierung, Compliance.

### Aufgabe
Erstelle einen **Leitfaden für digitale Produktideen** (B2B/B2C/B2B2C) für Immobilienmakler im Markt **{{REGION}}**. Der Leitfaden soll **Ideen generieren, bewerten, priorisieren und in umsetzbare MVPs überführen**.

### Anforderungen (Qualitätsstandard)
1. **Kontext‑Treue:** Nutze die Variablen. Wenn Angaben fehlen, triff **minimale, plausible Annahmen** und markiere sie als *Annahme*.  
2. **Immobilien‑Spezifik:** Berücksichtige reale Maklerprozesse: Akquise, Bewertung, Exposé, Vermarktung, Besichtigung, Verhandlung, Notar, Übergabe, After‑Sales.  
3. **Wertlogik:** Jede Idee braucht klaren Nutzen für mindestens eine Persona + messbaren Business‑Impact.  
4. **Differenzierung:** Zeige, wie das Produkt sich gegen **{{COMPETITORS}}** abhebt (Daten, Workflow, UX, Distribution, Partnerschaften).  
5. **DSGVO & Security by Design:** Behandle Datentypen, Rechtsgrundlagen, AVV, Hosting, Logging, Berechtigungen.  
6. **Umsetzbarkeit:** MVP‑Scope in 6–10 Wochen realistisch, mit **{{BUDGET_RANGE}}** und **{{TIME_TO_MARKET}}** kompatibel.  
7. **Kein Buzzword‑Overkill:** Klar, prägnant, umsetzbar.  

---

## 3) Output‑Format (verpflichtend)

### A) Executive Summary (max. 12 Zeilen)
- Ausgangslage ({{CLIENT_NAME}}, Markt, Ziel)
- 2–3 stärkste Produkt‑Wetten (Kurzbegründung)
- Nächste 3 Schritte (Workshop/Discovery → MVP)

### B) Markt- & Prozesslandkarte (kompakt, aber vollständig)
1. **Value Chain Maklergeschäft** (Schritte + typische Engpässe)  
2. **Datenlandkarte** (CRM, Exposé, Portale, Telefon/WhatsApp, Kalender, Vertragsdaten)  
3. **Kanal‑Ökonomie** ({{CHANNELS}}): Wo entstehen Kosten, wo Hebel?

### C) Ideen‑Portfolio: 12–18 digitale Produktideen
Für **jede** Idee bitte **1 Karte** im folgenden Schema:

**[Ideenname]**  
- **Kategorie:** Lead/Conversion | Ops/Automation | Customer Success | Data/Insights | Monetarisierung | Partner/Marketplace  
- **Zielpersona:** {{TARGET_PERSONAS}} (konkret auswählen)  
- **Job‑to‑be‑Done:** „Wenn … möchte ich … damit …“  
- **Problem & Trigger:** (inkl. {{PAIN_POINTS}})  
- **Lösung (1 Satz):**  
- **Kernfeatures (MVP):** 3–7 bullets  
- **Nice‑to‑Have:** 2–4 bullets  
- **Werthebel:** Zeitersparnis, Leadqualität, Abschlussquote, Preis/Marge, Risiko  
- **Integrationen:** {{CURRENT_STACK}} (konkret)  
- **Daten/Tracking:** Events, Funnel, Attribution (minimal)  
- **DSGVO/Security Notes:** Datentypen, Rechtsgrundlage, AVV, Rollen, Logging  
- **Monetarisierung:** Abo/Usage/Setup/Revenue‑Share (Begründung)  
- **Go‑to‑Market:** Kanal + erstes Angebot (z.B. „Bewertungs-Check in 48h“)  
- **Risiken & Gegenmaßnahmen:** 3 bullets  
- **KPI‑Set:** 5 KPIs (Leading + Lagging)

### D) Bewertungsmodell & Priorisierung
1. **Scoring‑Matrix** (1–5 Punkte je Kriterium, mit Gewichtung):  
   - Impact (Umsatz/Marge)  
   - Time‑to‑Value  
   - Umsetzungsaufwand (inverse)  
   - Datenverfügbarkeit ({{DATA_AVAILABILITY}})  
   - Distribution‑Fit ({{CHANNELS}})  
   - Compliance/Security‑Risiko (inverse, {{COMPLIANCE_LEVEL}})  
   - Differenzierung/Defensibility  
2. **Top‑5 Prioritäten** als Tabelle: Idee | Score | Warum jetzt | MVP‑Scope | Abhängigkeiten

### E) MVP‑Blueprint für die Top‑3 Ideen
Für jede der Top‑3:
- **Zielbild (Outcome):**  
- **MVP‑Scope (6–10 Wochen):** Epics → User Stories (8–15)  
- **Tech‑Skizze:** Komponenten, Integrationen, Rollen/Rechte (keine Code‑Wall)  
- **Analytics Plan:** Events, Dashboards, Experiment‑Hypothesen  
- **Rollout‑Plan:** Pilotkunden, Pricing‑Test, Onboarding, Support  
- **Abnahmekriterien:** klare Quality Gates

### F) 90‑Tage Roadmap (operational)
- Wochen 1–2: Discovery/Validierung  
- Wochen 3–6: Build MVP 1  
- Wochen 7–10: Pilot + Iteration  
- Wochen 11–13: Scale + Vertriebspakete  
Dazu: Ressourcenbedarf (Rollen), Risiken, Meilensteine, Deliverables.

### G) Workshop‑Agenda (2×90 Minuten) für {{AGENCY_NAME}}
- Ziel, Inputs, Methoden, Output‑Artefakte  
- Konkrete Fragenkataloge (Kunde/Vertrieb/Operations)

---

## 4) Business‑Logik: Leitplanken für gute Ideen (verpflichtend anzuwenden)

- **Lead‑Qualität schlägt Lead‑Menge**: bessere Qualification + schnellerer Follow‑Up = höhere Provision/Monat.  
- **Zeit ist Marge**: Exposé/Terminierung/Unterlagen automatisieren = mehr Deals pro Kopf.  
- **Vertrauen ist Conversion**: Transparenz, Status‑Updates, Dokumente, DSGVO‑Sicherheit.  
- **Distribution ist ein Produktfeature**: In {{CHANNELS}} integrierte Loops (Referral, Retargeting, Portal‑Sync).  
- **Daten sind defensible**: proprietäre Bewertungslogik, lokale Markt‑Signale, Prozessdaten.

---

## 5) Stilvorgaben
- Schreibe **{{LANGUAGE}}**, Ton: **Business‑klar**, strukturiert, ohne Floskeln.  
- Nutze Tabellen nur dort, wo Vergleich hilft.  
- Keine externen Links. Keine Quellenliste.  

---

## 6) Start jetzt
Beginne sofort mit Abschnitt **A) Executive Summary** und arbeite bis **G)** durch.