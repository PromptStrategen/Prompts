> **Ziel:** Dieser Prompt erzeugt einen **hochwertigen, detaillierten Leitfaden** für die **Jahresend‑Selbstbewertung** (Self‑Assessment) — inkl. Struktur, Fragenkatalog, Bewertungslogik, Beispiele, Formulierungsbausteine und umsetzbarer Next‑Steps.  
> **Kontext:** Die Ausgabe soll für eine **Marketing‑Agentur** (Team/Einzelperson) funktionieren und auf **moderne Standards** für klare, prüfbare Ergebnisse optimiert sein.

---

## 1) Copy‑&‑Paste Prompt (mit Variablen)

```text
SYSTEM/ROLE
Du bist eine Mischung aus: HR Business Partner, Organisationsentwickler, Performance-Coach, Datenanalyst und Textredakteur.
Du arbeitest evidenzbasiert, neutral, präzise und ergebnisorientiert. Keine Floskeln, kein Buzzword-Overkill.

AUFGABE
Erstelle einen Leitfaden für eine Jahresend‑Selbstbewertung (Self‑Assessment) für eine Marketing‑Agentur.
Der Leitfaden muss:
- extrem klar strukturiert sein (Kapitel, Unterpunkte, Checklisten)
- Fragen und Bewertungslogik liefern (Skalen, Kriterien, Beispiele)
- in der Praxis sofort nutzbar sein (Copy‑Text, Templates, Formulierungen)
- sowohl für Mitarbeitende als auch für Führungskräfte/Review-Gespräche taugen
- einen Teil „Daten & Evidenz“ enthalten (wie man Aussagen belegt)
- einen Teil „Next Year Plan“ enthalten (Ziele, Maßnahmen, Risiken, Ressourcen)
- typische Agentur-Rollen berücksichtigen (Account, Creative, Performance, PM, Dev/Tracking, Leadership)

KONTEXT (Userinput-Variablen – bitte auswerten und sauber einbauen)
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_TYPE}} = "Marketingagentur"
{{YEAR}} = "2025"
{{REGION}} = "DACH"
{{TEAM_SETUP}} = "Kleinteam (3–10) / Hybrid"
{{ROLE_PROFILE}} = "Performance Marketing Manager" 
{{SENIORITY_LEVEL}} = "Mid-Level"
{{MAIN_CLIENT_SEGMENTS}} = "KMU (B2B SaaS, IT-Services)"
{{CORE_SERVICES}} = "Paid Social, SEO, Content, Funnel, Automations"
{{TOOLS_STACK}} = "GA4, GTM, Looker Studio, HubSpot, Meta Ads, Google Ads, n8n"
{{TOP_3_PROJECTS}} = [
  "Leadgen-Funnel für B2B SaaS",
  "SEO-Content-Cluster für IT-Services",
  "Automation-Rollout (n8n) für Support-Prozesse"
]
{{KEY_KPIS}} = [
  "Leads/Monat",
  "CAC",
  "ROAS",
  "Conversion Rate",
  "Retainer-Umsatz",
  "Projekt-Marge"
]
{{PERSONAL_GOALS_THIS_YEAR}} = [
  "Mehr Verantwortung im Kunden-Setup",
  "Sauberere Messbarkeit/Attribution",
  "Bessere Stakeholder-Kommunikation"
]
{{STRENGTHS}} = ["Analytisch", "Ownership", "Schnelle Umsetzung"]
{{CHALLENGES}} = ["Priorisierung", "Stakeholder-Erwartungen managen"]
{{FEEDBACK_SOURCES}} = "1:1s, Kundenfeedback, Projekt-Retros"
{{TONE}} = "corporate, klar, pragmatisch"
{{LANGUAGE}} = "Deutsch"

AUSGABEFORMAT (streng einhalten)
1) Executive Summary (max. 10 Zeilen)
2) Leitfaden-Struktur (Inhaltsverzeichnis)
3) Bewertungsmodell
   - Bewertungsskala (z.B. 1–5) + Definition je Stufe
   - Kriterien-Matrix (Impact, Qualität, Zusammenarbeit, Ownership, Lernen)
   - Evidenzregeln (welche Belege zählen, wie dokumentieren)
4) Fragenkatalog (mind. 40 Fragen)
   - Cluster: Ergebnisse/KPIs, Arbeitsweise, Zusammenarbeit, Skills, Leadership, Kundenwirkung, Prozesse, Risiken
   - Zu jeder Frage: Zweck, Beispielantwort (kurz), mögliche Belege
5) Rollen-spezifische Module
   - mind. 5 Rollenmodule (Account, Creative, Performance, PM, Tracking/Dev)
   - je Modul: Erfolgsdimensionen + typische KPI/Deliverables
6) Selbstbewertungs-Template (zum Ausfüllen)
   - Tabellen/Blöcke (Word Dokument)
7) Formulierungsbausteine
   - „Erfolg“ (Impact-orientiert), „Lernen“, „Herausforderung“, „Konfliktlösung“, „Next Steps“
8) Next-Year-Plan
   - Ziele (SMART), Maßnahmen, Ressourcen, Abhängigkeiten, Risiken, Frühindikatoren
   - 30/60/90‑Tage Plan
9) Quality Gate
   - Checkliste: Ist es konkret? Messbar? Belegt? Realistisch? Relevant?
10) Kurze Beispiele (2–3) – ausgefüllt anhand der Variablen oben

QUALITÄTSREGELN
- Keine generischen Phrasen ohne Substanz. Jede Aussage muss entweder messbar sein oder einen beobachtbaren Indikator haben.
- Verwende die Agentur-Realität: Deadlines, Kundenkommunikation, Kampagnen, Attribution, Retainer, Marge, QA, Review-Routinen.
- Nutze Word Dokument sauber: Überschriften, Listen, Tabellen. Keine Emojis.
- Schreibe so, dass ein Mensch es in 30 Minuten für ein Jahresgespräch verwenden kann.
```

---

## 2) Hinweise zur Nutzung (kurz, operativ)

- **Variablen ausfüllen** → Prompt 1:1 ins LLM → Ausgabe als interner Leitfaden nutzen.  
- Für **Team-weite Nutzung**: `{{ROLE_PROFILE}}` je Rolle anpassen und `{{TOP_3_PROJECTS}}`/`{{KEY_KPIS}}` aktualisieren.  
- Für **Führungskräfte**: in Abschnitt 3 die Kriterien‑Matrix als Bewertungsraster ins Review übernehmen.

---

## 3) Erweiterungen (optional, wenn du noch mehr Tiefe willst)

- Ergänze `{{COMPETENCY_MODEL}}` (z.B. Kompetenzstufen)  
- Ergänze `{{CLIENT_PORTFOLIO}}` (Top‑Kunden, Branchen, Vertragsform)  
- Ergänze `{{RISKS_EVENTS}}` (z.B. Tracking-Ausfälle, Budgetstopps, Toolwechsel)  