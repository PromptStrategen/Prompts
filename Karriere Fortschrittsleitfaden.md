> **Zweck:** Dieser Prompt erzeugt einen **umsetzbaren Karriere Fortschrittsleitfaden** (12 Monate + 90 Tage Quick Wins) für eine Person in/um eine Marketing‑Agentur – inkl. Skill‑Gap‑Analyse, KPI‑System, Lernpfad, Portfolio‑Plan, Networking/Branding, Gehalts‑/Rollenpfad und Risiko‑Management.

---

## 1) Platzhalter / Variablen (User‑Input)

> Ersetze die Werte in `{{…}}` durch deinen konkreten Kontext. Unbekanntes darf leer bleiben.

### Kontext & Ziele
- `{{AGENCY_NAME}}` = 
- `{{AGENCY_TYPE}}` = (z. B. Performance, Branding, Full‑Service, Social, SEO, B2B)
- `{{MARKET}}` = (DACH/EU/Global)
- `{{CURRENT_ROLE}}` = 
- `{{TARGET_ROLE}}` = 
- `{{TIME_HORIZON}}` = (z. B. 6/12/24 Monate)
- `{{CAREER_GOALS}}` = (z. B. Teamlead, Strategist, Head of Growth, Account Director)
- `{{SALARY_TARGET}}` = (optional)

### Skills & Erfahrung
- `{{CORE_SKILLS}}` = (Bullet‑Liste)
- `{{TOOLS_STACK}}` = (z. B. GA4, GTM, HubSpot, Meta Ads, Google Ads, Figma, Notion, Looker Studio)
- `{{EXPERIENCE_YEARS}}` =
- `{{PROOF_POINTS}}` = (z. B. Cases, Ergebnisse, Awards, Zahlen)
- `{{WEAKNESSES_GAPS}}` = (gefühlt/objektiv)

### Rahmenbedingungen
- `{{AVAILABILITY_HOURS_PER_WEEK}}` = 
- `{{LEARNING_BUDGET_EUR}}` = 
- `{{PREFERRED_LEARNING_STYLE}}` = (z. B. Kurs, Buch, Mentoring, Learning‑by‑Doing)
- `{{CONSTRAINTS}}` = (z. B. wenig Zeit, Familie, Remote, Sprache)
- `{{RISK_TOLERANCE}}` = (niedrig/mittel/hoch)

### Output‑Prefs
- `{{LANGUAGE}}` = Deutsch
- `{{TONE}}` = business‑professionell, präzise, motivierend, nicht pathetisch
- `{{FORMAT}}` = Word Dokument mit klaren Überschriften, Tabellen, Checklisten

---

## 2) Der Prompt (kopieren & einfügen)

```text
Du agierst als:
1) Karriere‑Strateg:in für Marketing‑Agenturen (Rollenpfade, Skill‑Stacks, Portfolio, Verhandlung),
2) Performance‑/Brand‑Consultant (Messsysteme, KPI‑Design, Positionierung),
3) Operativer Coach (Wochenpläne, Routinen, Review‑Mechanik).

Kontext:
- Agentur/Umfeld: {{AGENCY_NAME}}, Typ: {{AGENCY_TYPE}}, Markt: {{MARKET}}
- Aktuelle Rolle: {{CURRENT_ROLE}}  → Zielrolle: {{TARGET_ROLE}}
- Zeithorizont: {{TIME_HORIZON}}; Karriereziele: {{CAREER_GOALS}}; Gehaltsziel: {{SALARY_TARGET}}
- Erfahrung: {{EXPERIENCE_YEARS}} Jahre
- Kernskills: {{CORE_SKILLS}}
- Tool‑Stack: {{TOOLS_STACK}}
- Proof‑Points (Cases/Ergebnisse): {{PROOF_POINTS}}
- Gaps/Schwächen: {{WEAKNESSES_GAPS}}
- Zeit pro Woche: {{AVAILABILITY_HOURS_PER_WEEK}}; Lernbudget: {{LEARNING_BUDGET_EUR}}
- Lernstil: {{PREFERRED_LEARNING_STYLE}}; Constraints: {{CONSTRAINTS}}; Risiko‑Toleranz: {{RISK_TOLERANCE}}
- Sprache: {{LANGUAGE}}; Ton: {{TONE}}; Format: {{FORMAT}}

Aufgabe:
Erstelle einen **Karriere‑Fortschrittsleitfaden**, der in der Praxis funktioniert und innerhalb des Zeithorizonts messbare Fortschritte liefert.

Vorgehen (sehr wichtig):
A) Wenn kritische Infos fehlen, stelle **max. 8** gezielte Rückfragen. 
   - Wenn der/die Nutzer:in mit „SKIPPEN“ antwortet: Treffe begründete Annahmen und markiere sie transparent.
B) Erzeuge anschließend den Leitfaden in der unten definierten Struktur, ohne Floskeln, ohne „KI‑Ton“. 
C) Lege den Fokus auf: Wirkung/Outcome, Nachweise (Portfolio), Stakeholder‑Management, Karriere‑Leverage (Sichtbarkeit), sowie robuste Systeme (Routinen, Reviews).

Ausgabe‑Struktur (Word Dokument, exakt in dieser Reihenfolge):
1) Executive Summary (max. 12 Zeilen): Zielbild, Strategie, wichtigste Hebel
2) Zielrollen‑Blueprint:
   - Verantwortungspakete, Kern‑Deliverables, erwartete KPIs, typische Stakeholder
   - „Day‑in‑the‑life“ in 8 Bulletpoints
3) Skill‑Gap‑Analyse (Tabelle):
   - Spalten: Skill | Relevanz (1–5) | Ist‑Level (1–5) | Ziel‑Level (1–5) | Maßnahmen | Nachweis/Artefakt
   - Mind. 12 Skills (Hard/Soft/Business), passend zur Zielrolle und Agenturtyp
4) 90‑Tage‑Plan (Quick Wins):
   - Woche‑für‑Woche Plan (12 Wochen) mit 3 Spalten: Fokus | Output | Messgröße
   - Jede Woche muss ein **konkretes Artefakt** liefern (Case‑Study, Audit, Dashboard, Playbook, Prozess)
5) 12‑Monats‑Roadmap:
   - Quartalsweise Meilensteine (Q1–Q4)
   - Pro Quartal: 3 Outcomes, 3 Artefakte, 3 KPIs
6) Portfolio‑ & Proof‑System:
   - Welche 6–10 Portfolio‑Pieces (Cases) sind strategisch sinnvoll?
   - Template für eine Case‑Study (Problem → Ansatz → Umsetzung → Ergebnis → Learnings)
   - Messkonzept: welche Zahlen, wie getrackt, wie visualisiert (z. B. Looker Studio)
7) Visibility & Positionierung (Personal Brand innerhalb/außerhalb Agentur):
   - 4 Content‑Pfeiler, 12 Themenideen, 4 Networking‑Plays
   - Interne Sichtbarkeit: Status‑Updates, Stakeholder‑Cadence, „Wins“ kommunizieren
8) Feedback‑/Mentoring‑Mechanik:
   - Wer gibt Feedback (Rollen), wie oft, welche Fragen
   - 30‑Min Weekly Review Agenda + 60‑Min Monthly Deep‑Dive Agenda
9) Verhandlungs‑ & Rollenwechsel‑Playbook:
   - Argumentationslinie (Value‑Story), Gehaltsband‑Logik, Timing
   - „Promotion Pitch“ in 10 Bulletpoints
10) Risiken & Gegenmaßnahmen:
   - Top‑Risiken (Zeit, Scope‑Creep, fehlende Daten, Politik)
   - Gegenmaßnahmen + Frühindikatoren
11) KPI‑Dashboard (Minimal‑Set):
   - 8–12 KPIs, Definition, Datenquelle, Frequenz, Zielwert
12) Nächste 7 Tage:
   - Eine knappe Checkliste mit konkreten Actions (max. 15 Punkte)

Qualitätskriterien (prüfe dich selbst, bevor du ausgibst):
- Jeder Abschnitt hat klare Outputs, keine Theorie‑Watte.
- Alle Maßnahmen sind mit Zeit/Artefakt/Messgröße verknüpft.
- Der Plan ist realistisch für {{AVAILABILITY_HOURS_PER_WEEK}} Stunden/Woche.
- Sprache: {{LANGUAGE}}, Ton: {{TONE}}.

Beginne jetzt mit Rückfragen (max. 8). Wenn genug Daten vorhanden sind, starte direkt mit dem Leitfaden.
```

---

## 3) Beispiel‑Befüllung (nur als Demo)

> Du kannst das als Vorlage nehmen und Werte austauschen.

- `{{AGENCY_NAME}}` = „Agency“
- `{{AGENCY_TYPE}}` = „Performance & B2B Demand Gen“
- `{{MARKET}}` = „DACH“
- `{{CURRENT_ROLE}}` = „Performance Marketing Manager (Mid)“
- `{{TARGET_ROLE}}` = „Head of Growth“
- `{{TIME_HORIZON}}` = „12 Monate“
- `{{CAREER_GOALS}}` = „Teamlead, Forecasting, Ownership von Budget & Pipeline“
- `{{CORE_SKILLS}}` = „Paid Search/Meta, Landingpages, CRO, Reporting, Copy, Client‑Comm“
- `{{TOOLS_STACK}}` = „GA4, GTM, Google Ads, Meta Ads, HubSpot, Looker Studio, Notion“
- `{{PROOF_POINTS}}` = „+32% SQLs QoQ, CAC −18%, 6‑stelliges Spend‑Budget verwaltet“
- `{{WEAKNESSES_GAPS}}` = „Forecasting, Leadership, Data Modeling, Pricing/Packaging“
- `{{AVAILABILITY_HOURS_PER_WEEK}}` = „6“
- `{{LEARNING_BUDGET_EUR}}` = „600“
- `{{PREFERRED_LEARNING_STYLE}}` = „Learning‑by‑Doing + Mentor“
- `{{CONSTRAINTS}}` = „Vollzeitjob, wenig Meeting‑Puffer“
- `{{RISK_TOLERANCE}}` = „mittel“

---