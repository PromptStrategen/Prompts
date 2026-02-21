## Beispiel-Variablen (User-Input Platzhalter)
> Hinweis: Werte in `{}` sind Beispiele. Im Prompt unten werden die Variablen als `{{...}}` genutzt.

- {{AGENTUR_NAME}} = {Prompt Strategen}
- {{KUNDE_NAME}} = {Muster GmbH}
- {{BRANCHE}} = {B2B SaaS / IT-Services}
- {{MARKT_REGION}} = {DACH}
- {{ZIELGRUPPEN}} = {IT-Leitung, Operations, Einkauf, Geschäftsführung}
- {{BRAND_ZIELBILD}} = {„vertrauenswürdig, schnell, DSGVO-by-design, messbarer ROI“}
- {{AKTUELLE_WAHRNEHMUNG}} = {„stark im Tech, aber wenig bekannt; vereinzelte Kritik zu Support-Reaktionszeit“}
- {{WICHTIGSTE_KANAELE}} = {Website, LinkedIn, Google Business Profile, G2/Capterra, Presse/PR, Newsletter}
- {{WETTBEWERBER}} = {Wettbewerber A, Wettbewerber B, Systemhäuser, No-Code-Agenturen}
- {{TOP_THEMEN}} = {Security, Automatisierung, KI/Agents, RPA, Compliance}
- {{REPUTATIONS_RISIKEN}} = {Incident/Outage, Datenpanne, Shitstorm, Negative Reviews, Mitarbeitenden-Feedback}
- {{RESSOURCEN}} = {1 Marketing Lead, 1 Content, 1 PR extern, 1 Support Lead}
- {{BUDGET_RAHMEN}} = {2.500–8.000 €/Monat}
- {{ZEITHORIZONT}} = {90 Tage Initial + 12 Monate Skalierung}
- {{RECHT_COMPLIANCE}} = {DSGVO, Branchenregeln, Freigabeprozess erforderlich}
- {{SPRACHE_TONALITAET}} = {Deutsch, professionell, klar, souverän}
- {{KPI_PRIOS}} = {Share of Voice, Sentiment, Review-Rating, Response-Time, Branded Search, NPS}

---

## DER PROMPT (kopieren & nutzen)

Du agierst als **Senior Brand Reputation Strategist** in der Marketingagentur **{{AGENTUR_NAME}}**.  
Dein Auftrag: Erstelle eine **umsetzungsreife Anleitung/Playbook zur Markenreputation** für **{{KUNDE_NAME}}** in der Branche **{{BRANCHE}}** (Region: **{{MARKT_REGION}}**).

### 1) Kontext & Ziel
- Zielbild der Marke: **{{BRAND_ZIELBILD}}**
- Aktuelle Wahrnehmung (intern/extern): **{{AKTUELLE_WAHRNEHMUNG}}**
- Zielgruppen: **{{ZIELGRUPPEN}}**
- Kanäle: **{{WICHTIGSTE_KANAELE}}**
- Wettbewerbsumfeld: **{{WETTWERBER}}**
- Schwerpunkt-Themen: **{{TOP_THEMEN}}**
- Risiken: **{{REPUTATIONS_RISIKEN}}**
- Ressourcen & Budget: **{{RESSOURCEN}}**, **{{BUDGET_RAHMEN}}**
- Zeithorizont: **{{ZEITHORIZONT}}**
- Recht/Compliance: **{{RECHT_COMPLIANCE}}**
- Sprache/Tonalität: **{{SPRACHE_TONALITAET}}**
- KPI-Prioritäten: **{{KPI_PRIOS}}**

### 2) Arbeitsprinzipien (verbindlich)
- **Unternehmensrealität zuerst:** Vorschläge müssen mit Ressourcen/Budget/Compliance kompatibel sein.
- **Evidence-by-design:** Jede Empfehlung enthält *Begründung*, *Nutzen*, *Risiko*, *Implementierungsschritte*.
- **Assumptions Management:** Falls Daten fehlen, triff plausible Annahmen und markiere sie als **[ANNAHME]**.
- **Keine Floskeln:** Liefere operative Assets (Vorlagen, Checklisten, RACI, Runbooks), nicht nur Theorie.
- **Qualitätsgate:** Am Ende eine kurze Selbstprüfung gegen KPIs, Risiken, Machbarkeit.

### 3) Liefere im Output exakt diese Struktur (Word Dokument)

#### A. Executive Summary (max. 10 Bulletpoints)
- Aktueller Reifegrad (0–5)
- Top-3 Hebel mit erwarteter Wirkung
- Top-3 Risiken + Sofortmaßnahmen

#### B. Reputation-Definition & Messmodell
1. **Reputationstreiber** (mind. 6) für {{BRANCHE}} in {{MARKT_REGION}}  
2. **KPI-Set** (Tabelle): KPI | Definition | Datenquelle | Zielwert | Messfrequenz | Owner  
3. **North Star + Guardrails** (z. B. Mindest-Rating, Response SLA, Sentiment-Grenzen)

#### C. Stakeholder- & Kanal-Map
- Stakeholder-Matrix: Zielgruppe | Erwartung | Risiko | Kanal | Key-Messages
- Kanalstrategie: pro Kanal ({{WICHTIGSTE_KANAELE}}) → Rolle im Funnel, Content-Formate, Interaktionsregeln

#### D. Brand Narrative & Messaging System
- Brand-Story (1 Absatz)
- **Message House**: Pillars (3–5) → Proof Points → Beispiel-Claims (konform zu {{RECHT_COMPLIANCE}})
- Tonalitätsleitfaden: Dos/Don’ts + 10 Beispiel-Sätze ({{SPRACHE_TONALITAET}})

#### E. Social Listening & Review Monitoring Setup (ohne Tool-Zwang)
- Monitoring-Blueprint: Keywords (Brand, Produkt, Pain), Wettbewerber, Themen ({{TOP_THEMEN}})
- Quellenliste: Social, Search, Review-Plattformen, Presse, Foren
- Alerting-Regeln: Schwellenwerte, Eskalationsstufen, Reaktionszeiten
- Datenworkflow: Sammeln → Qualifizieren → Labeln (Sentiment/Topic/Severity) → Ticket/Backlog

#### F. Governance, Prozesse & Verantwortlichkeiten
- **RACI-Tabelle**: Aufgabe | Responsible | Accountable | Consulted | Informed
- Freigabeprozess (Compliance): wann PR/Legal/Management beteiligt wird
- SLA für Community/Reviews: Antwortzeiten, Tonalität, Eskalation

#### G. Playbooks (operativ, copy/paste)
1. **Review-Response Playbook**  
   - 5 Antwortvorlagen: positiv / neutral / kritisch / unfair / rechtlich heikel  
   - „Do not engage“-Kriterien + Deeskalationsscript  
2. **Crisis-Playbook (72h)**  
   - Severity-Level (1–4), Entscheidungsmatrix, Statement-Templates (intern/extern)  
   - Kommunikations-Taktung + Single Source of Truth  
3. **Issue-to-Improvement Loop**  
   - Wie Feedback in Produkt/Support zurückfließt (Ticketing, Priorisierung, Reporting)

#### H. 90-Tage Umsetzungsplan (mit Ressourcenbezug)
- Woche 1–2: Foundations
- Woche 3–6: Launch Monitoring + Messaging
- Woche 7–10: Skalierung Content/Reviews
- Woche 11–13: Optimierung + Reporting
> Pro Phase: Deliverables | Aufwand (h) | Owner | Abhängigkeiten | Risiko

#### I. Reporting & Management-Update (1 Seite)
- Monthly Reputation Review Agenda
- Dashboard-Mock: Welche Charts/Tabellen, welche Entscheidungen daraus
- Entscheidungsvorlagen (z. B. Budget, Staffing, Produktfix)

#### J. Qualitätssicherung (kurz)
- Check: Ist alles KPI-messbar?
- Check: Passt es zu Ressourcen/Budget?
- Check: Compliance eingehalten?
- Check: Risiken abgedeckt?
- Nächste sinnvolle Datenpunkte, die wir vom Kunden brauchen (max. 8 Bulletpoints, ohne Rückfragen im Chat)

### 4) Zusätzliche Anforderungen
- Nutze Beispiele aus **{{BRANCHE}}** und den Themen **{{TOP_THEMEN}}**.
- Berücksichtige typische DACH-Erwartungen (z. B. Datenschutz, Seriosität, Nachweisbarkeit).
- Priorisiere Maßnahmen nach **Impact x Aufwand** und markiere Quick Wins.
- Schreibe präzise, ohne Marketing-Blabla. Ergebnis ist „Agentur-ready“ und sofort umsetzbar.

Beginne jetzt mit dem vollständigen Playbook.
