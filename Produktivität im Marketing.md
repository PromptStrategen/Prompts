> **Ziel:** Dieser Prompt erzeugt einen **hochwertigen, umsetzbaren Leitfaden** für **Produktivität im Marketing** (Team + Prozesse + Tooling + KPI‑System), ausgelegt auf **moderne Arbeitsweisen** (z. B. agile Planung, KI‑Assistenz, Automations, Content Ops, Revenue‑Ops‑Anbindung).
>
> **Nutzung:** 1) Variablen ausfüllen 2) Prompt an ein LLM geben 3) Output als internes Playbook verwenden.

---

## 1) User‑Input: Variablenblock (Beispiel‑Platzhalter)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing‑/Digitalagentur (B2B, DACH)"
{{CLIENT_BRAND}} = "Beispiel GmbH"
{{INDUSTRY}} = "B2B SaaS"
{{TARGET_AUDIENCE}} = "KMU (50–500 MA), IT‑Leitung, Ops/Support"
{{PRIMARY_GOAL}} = "mehr qualifizierte Leads (MQL→SQL), planbare Pipeline"
{{SECONDARY_GOALS}} = "Brand Authority, Recruiting, Upsell"
{{TIME_HORIZON}} = "90 Tage"
{{TEAM_SETUP}} = "1× Marketing Lead, 1× Content, 1× Design, 1× Performance, 0.5× Sales"
{{CURRENT_PAIN_POINTS}} = "zu viele Ad‑hoc Tasks, fehlende Priorisierung, keine sauberen KPIs, Content-Stau"
{{CHANNELS}} = "LinkedIn, Website/Blog, Newsletter, YouTube (optional), Paid Search (optional)"
{{BUDGET_LEVEL}} = "mittel"  # low | mittel | hoch
{{TECH_STACK}} = "HubSpot, GA4, Search Console, Notion, Slack, n8n, Canva/Figma"
{{COMPLIANCE_REQUIREMENTS}} = "DSGVO, Markenrichtlinien, Freigabeprozesse"
{{TONE_OF_VOICE}} = "professionell, klar, kein Buzzword‑Overkill"
{{CONSTRAINTS}} = "max. 10h/Woche pro Teammitglied; keine zusätzlichen Tools einkaufen in den ersten 30 Tagen"
{{SUCCESS_METRICS}} = "MQL, SQL, CAC Payback, CPL, Conversion Rate, Content Throughput, Cycle Time"
{{AVAILABLE_ASSETS}} = "bestehende Website, 5 Case Studies, 20 Blogposts, 1 Webinaraufzeichnung"
{{COMPETITORS}} = "Wettbewerber A, B, C"
{{LANGUAGE}} = "Deutsch"
```

---

## 2) Beispiel: Ausgefüllter Variablenblock (Demo)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing‑/Digitalagentur (B2B, DACH)"
{{CLIENT_BRAND}} = "Ich‑möchte‑KI‑verstehen GmbH"
{{INDUSTRY}} = "Weiterbildung / B2B Coaching"
{{TARGET_AUDIENCE}} = "KMU‑Entscheider, Team‑Leads, HR"
{{PRIMARY_GOAL}} = "planbare Lead‑Pipeline via Content + LinkedIn"
{{SECONDARY_GOALS}} = "Brand Awareness, Newsletter‑Wachstum"
{{TIME_HORIZON}} = "60 Tage"
{{TEAM_SETUP}} = "2 Personen (Content+Ops), 1 Freelancer Design"
{{CURRENT_PAIN_POINTS}} = "fehlende Standards, doppelte Arbeit, kein Sprint‑Rhythmus"
{{CHANNELS}} = "LinkedIn, Newsletter, Landingpages"
{{BUDGET_LEVEL}} = "low"
{{TECH_STACK}} = "Brevo, GA4, Notion, Google Drive, n8n"
{{COMPLIANCE_REQUIREMENTS}} = "DSGVO, Consent, Freigaben"
{{TONE_OF_VOICE}} = "klar, wissenschaftlich korrekt, pragmatisch"
{{CONSTRAINTS}} = "keine bezahlten Ads; 6h/Woche pro Person"
{{SUCCESS_METRICS}} = "Newsletter‑Signups, CTR, Landingpage‑CR, Demo‑Requests"
{{AVAILABLE_ASSETS}} = "1 PDF‑Leadmagnet, 10 Posts, 2 Kundenstimmen"
{{COMPETITORS}} = "A, B"
{{LANGUAGE}} = "Deutsch"
```

---

## 3) Der Prompt (Copy‑&‑Paste)

```text
Du agierst als:
1) Head of Marketing Operations (Marketing‑Ops) mit Fokus auf Prozessdesign, Messbarkeit und Skalierung,
2) Performance‑ und Content‑Strateg:in (B2B) mit starker Priorisierungslogik,
3) KI‑Enablement Lead für Marketing‑Automatisierung (Prompting, Agent‑Workflows, n8n/Make‑Denke).

Arbeite strikt faktenbasiert, pragmatisch, umsetzungsorientiert. Vermeide Floskeln.
Sprache: {{LANGUAGE}}.
Kontext: Wir sind {{AGENCY_NAME}} ({{AGENCY_ROLE}}) und erstellen für {{CLIENT_BRAND}} ({{INDUSTRY}}) einen Leitfaden, der Produktivität im Marketing messbar erhöht.

### Input‑Kontext
- Zielgruppe: {{TARGET_AUDIENCE}}
- Primärziel: {{PRIMARY_GOAL}}
- Sekundärziele: {{SECONDARY_GOALS}}
- Zeithorizont: {{TIME_HORIZON}}
- Teamsetup: {{TEAM_SETUP}}
- Schmerzpunkte: {{CURRENT_PAIN_POINTS}}
- Kanäle: {{CHANNELS}}
- Budget: {{BUDGET_LEVEL}}
- Tech‑Stack: {{TECH_STACK}}
- Compliance: {{COMPLIANCE_REQUIREMENTS}}
- Tonalität: {{TONE_OF_VOICE}}
- Constraints: {{CONSTRAINTS}}
- Erfolgsmetriken: {{SUCCESS_METRICS}}
- Assets: {{AVAILABLE_ASSETS}}
- Wettbewerb: {{COMPETITORS}}

### Aufgabe
Erstelle einen **Leitfaden "Produktivität im Marketing"** als internes Playbook.
Das Playbook muss:
- in der Praxis mit dem gegebenen Teamsetup funktionieren,
- Priorisierung, Planung, Produktion und Messung integrieren,
- klare Standards (Definitionen, Checklisten, Templates) liefern,
- KI‑ und Automations‑Bausteine enthalten (ohne "Magie", mit klaren Prozessschritten),
- pro Abschnitt konkrete Beispiele und Default‑Einstellungen geben.

### Output‑Format (verbindlich)
Gib die Antwort in sauberem Word Dokument mit folgender Struktur aus:

1) Executive Summary (max. 12 Zeilen)
2) Operating Model (Rollen, Verantwortlichkeiten, Meeting‑Cadence, Artefakte)
3) Priorisierungs‑System (Methodik + Scorecard + Beispiel)
4) Workflow‑Design (End‑to‑End von Idee→Briefing→Produktion→QA→Distribution→Reporting)
5) "Definition of Done" & Qualitätsgates (Content, Ads, Landingpages, Newsletter)
6) KPI‑System & Messkonzept (North Star, Treiber, Dashboard‑Blueprint)
7) Tooling & Automations (Quick Wins in 7/30/60 Tagen; inkl. n8n‑Workflow‑Skizzen als Pseudocode)
8) Templates (Briefing‑Template, Redaktionsplan, Post‑Template, Review‑Checkliste, Retro‑Agenda)
9) 30‑60‑90‑Tage Umsetzungsplan (mit Kapazitätsplanung, Risiken, Abhängigkeiten)
10) Risiko‑ und Anti‑Pattern‑Liste (was Produktivität killt + Gegenmaßnahmen)
11) KPI‑Review‑Ritual (wöchentlich/monatlich) + Beispiel‑Agenda
12) "Minimum Viable Governance" (Freigaben, DSGVO, Brand‑Compliance, Dokumentation)
13) Anhang: Prompt‑Library (mind. 8 Prompts), jeweils mit Zweck, Input‑Variablen und Output‑Schema

### Qualitätsanforderungen
- Nutze klare Begriffe. Definiere jede interne Metrik (z. B. Cycle Time, Throughput, WIP).
- Liefere pro Framework eine "So wenden wir es ab morgen an"‑Sektion.
- Zeige mindestens 1 vollständiges Beispiel: Priorisierungsscore + resultierender Wochenplan.
- Nenne Annahmen explizit und trenne Annahmen von Empfehlungen.
- Vermeide generische Tipps. Jeder Punkt muss ein konkretes Artefakt, eine Regel oder ein Messkriterium besitzen.
- Wenn Informationen fehlen, triff sinnvolle Default‑Annahmen, markiere sie als "Annahme", und liefere eine Alternative.

### Zusätzliche Constraints
- Halte dich an: {{CONSTRAINTS}}.
- Keine Tool‑Empfehlungen, die zwingend Kosten verursachen, außer als "Option".
- Beachte Compliance: {{COMPLIANCE_REQUIREMENTS}}.

Starte jetzt.
```

---

## 4) Ergebnis‑Qualitätscheck (Kurz‑Rubrik)

Nutze diese Rubrik, um die Antwort zu prüfen (0–2 Punkte je Kriterium, max. 20):

- Umsetzbarkeit mit aktuellem Teamsetup
- Klarer Priorisierungsmechanismus + Beispiel
- End‑to‑End Workflow mit klaren Übergaben
- Messkonzept (North Star + Treiber + Dashboard)
- Konkrete Templates & Checklisten
- KI/Automation als Prozessbaustein (nicht nur Tool‑Name)
- Berücksichtigung Constraints & Compliance
- 30‑60‑90‑Tage Plan mit Kapazitäten
- Anti‑Patterns + Gegenmaßnahmen
- Prompt‑Library mit Output‑Schemas

---

## 5) Tipp für professionelle Nutzung (Ops‑Standard)

- Lege das Output‑Playbook in euer Wiki (Notion/Confluence) und versioniere es.
- Definiere 1 Owner (Marketing‑Ops) für Pflege, Metriken und Prozess‑Änderungen.
- Führe nach 14 Tagen eine Retro durch: **Was reduziert WIP? Was erhöht Durchsatz? Was verbessert Qualität messbar?**
