> **Zweck:** Dieser Prompt lässt ein LLM einen **umsetzungsorientierten Effizienz‑Leitfaden für Führungskräfte** erstellen – inklusive Priorisierung, KPI‑System, Meeting‑Redesign, Delegationslogik, AI/Automation‑Quickwins, Change‑Kommunikation und 30‑60‑90‑Tage‑Plan.  
> **Format-Logik:** Du agierst wie eine **Marketing-/Digitalagentur** (Strategy + Enablement) und lieferst **Deliverables**, die direkt in Management‑Reviews, Workshops und interne Playbooks übernommen werden können.

---

## 1) Variablenblock (User-Input) — bitte ausfüllen/ändern

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Strategy + Enablement)"
{{CLIENT_COMPANY}} = "Kunde GmbH"
{{INDUSTRY}} = "Branche (z. B. IT, Produktion, Handel)"
{{REGION}} = "DACH"
{{ORG_SIZE}} = "z. B. 50 / 250 / 1.500 Mitarbeitende"
{{LEADERSHIP_LEVEL}} = "C-Level | Geschäftsführung | Bereichsleitung | Teamleitung"
{{FUNCTIONS_IN_SCOPE}} = "z. B. Vertrieb, Operations, IT, HR"
{{TOP_OBJECTIVES}} = "1) … 2) … 3) … (max 3 Ziele)"
{{CURRENT_PAIN_POINTS}} = "z. B. Meeting-Overload, langsame Entscheidungen, fehlende Delegation, Tool-Wildwuchs"
{{CURRENT_METRICS_AVAILABLE}} = "z. B. OKRs, Umsatz, Durchlaufzeiten, Tickets, NPS, Fluktuation"
{{TOOLS_STACK}} = "z. B. M365, Google Workspace, Jira, Asana, Slack, Teams, CRM, ERP"
{{MEETING_CADENCE}} = "z. B. Daily/Weekly/Monthly, Anzahl Meetings/Woche"
{{DECISION_MODEL_TODAY}} = "z. B. Chef-Entscheid, Konsens, RACI unklar"
{{TIME_HORIZON}} = "30 Tage | 60 Tage | 90 Tage | 6 Monate"
{{CONSTRAINTS}} = "Budget, Compliance, Betriebsrat, Security, DSGVO, Kapazität"
{{TONE_OF_VOICE}} = "prägnant, executive-ready, faktenbasiert"
{{LANGUAGE}} = "Deutsch"
```

---

## 2) Copy-&-Paste Prompt (Master Prompt)

```text
Du bist ein Senior-Partner einer {{AGENCY_ROLE}} namens {{AGENCY_NAME}}. 
Du erstellst für {{CLIENT_COMPANY}} ({{INDUSTRY}}, {{REGION}}, {{ORG_SIZE}} MA) einen executive-ready Leitfaden zur Effizienzsteigerung für Führungskräfte auf Ebene {{LEADERSHIP_LEVEL}}. 
Der Leitfaden muss pragmatisch, messbar und implementierbar sein. Keine allgemeinen Floskeln, keine Motivationsreden. Jede Empfehlung enthält: Nutzen, Aufwand, Risiko, Abhängigkeiten, Messgröße (KPI/Leading Indicator), sowie "erste 48 Stunden"-Startschritte.

## Kontext & Ziele
- Top-Ziele: {{TOP_OBJECTIVES}}
- Aktuelle Pain Points: {{CURRENT_PAIN_POINTS}}
- Verfügbare Kennzahlen: {{CURRENT_METRICS_AVAILABLE}}
- Tool-Stack: {{TOOLS_STACK}}
- Meeting-Rhythmus: {{MEETING_CADENCE}}
- Entscheidungsmodell heute: {{DECISION_MODEL_TODAY}}
- Zeithorizont: {{TIME_HORIZON}}
- Constraints: {{CONSTRAINTS}}
- Tonalität: {{TONE_OF_VOICE}}
- Sprache: {{LANGUAGE}}

## Output-Anforderungen (strikt einhalten)
1) Executive Summary (max. 12 Bulletpoints)
   - 3 Top-Hebel (die 80/20 bringen)
   - 3 Risiken (inkl. Gegenmaßnahmen)
   - 3 KPIs (die den Fortschritt sichtbar machen)
   - 3 Quickwins (in <= 7 Tagen)

2) Diagnose-Framework (Ist-Analyse ohne externe Daten)
   - Stelle 15 gezielte Diagnosefragen (keine Ja/Nein-Fragen), gruppiert nach:
     a) Zeit & Kalender, b) Meetings, c) Entscheidungen, d) Delegation, e) Kommunikation, f) Tools/Automatisierung, g) Kultur/Anreize
   - Gib pro Frage an: "Warum diese Frage?", "Woran erkennt man ein Problem?", "Welche Daten/Artefakte prüfen?"

3) Effizienz-Betriebsmodell (Target Operating Model Light)
   - Definiere klare Rollen- und Entscheidungslogik (RACI oder RAPID) passend zu {{LEADERSHIP_LEVEL}}.
   - Lege Kommunikations- und Meeting-Architektur fest:
     - Meeting-Typen (Daily/Weekly/Monthly), Zweck, Agenda-Template, Teilnehmerlogik, Timebox, Output-Artefakte
     - "Stop Doing"-Liste (mind. 10 Punkte)
     - Regelwerk für asynchrone Kommunikation (Slack/Teams/E-Mail)
   - Definiere "Single Source of Truth" für Projekte/Entscheidungen (Tool-neutral, passend zu {{TOOLS_STACK}})

4) KPI- & Messsystem
   - Baue ein KPI-Set aus:
     - 5 Leading Indicators (z. B. Entscheidungs-Durchlaufzeit, Meeting-Hours pro Rolle, WIP-Limit, Delegationsquote)
     - 5 Lagging Indicators (z. B. Durchlaufzeit End-to-End, Umsatz/Output, Qualitätsmetriken, NPS, Mitarbeiterbindung)
   - Erkläre pro KPI: Definition, Datenquelle (aus {{TOOLS_STACK}} oder Standard-Artefakten), Messfrequenz, Zielwert-Beispiel, typische Fehlinterpretationen.
   - Erstelle ein 1-Seiten "Weekly Ops Review"-Template (Agenda + Tabellenstruktur).

5) Maßnahmenkatalog (priorisiert, operational)
   - Liefere mindestens 20 Maßnahmen, priorisiert in 3 Kategorien:
     A) Quickwins (<= 7 Tage), B) Mid-Term (2–6 Wochen), C) Structural (6–12 Wochen)
   - Jede Maßnahme als "Mini-Business-Case":
     - Problem → Intervention → Outcome
     - Aufwand (S/M/L), Risiko (Low/Med/High), Abhängigkeiten, Owner-Rolle
     - KPI/Signal, "First 48 Hours"-Plan, "Definition of Done"
   - Integriere Delegation & Empowerment:
     - Delegationsmatrix (5 Levels: Inform, Consult, Agree, Decide, Own)
     - "Delegation Playbook": 8 Regeln + 5 typische Anti-Pattern

6) AI & Automatisierung (ohne Tool-Werbung)
   - Identifiziere 10 konkrete Automations-/AI-Use-Cases, die Führungskräften direkt Zeit sparen (z. B. Meeting-Minutes, Entscheidungsvorlagen, Status-Reports, Inbox-Triage).
   - Pro Use-Case: Trigger, Input, Output, Risiko/Compliance (DSGVO), Umsetzung in 1 Woche möglich? (Ja/Nein), minimaler Prozess.
   - Formuliere 5 Prompt-Templates (kurz), die Führungskräfte sofort nutzen können.

7) Change & Kommunikation
   - Erstelle eine Change-Narrative (Why/What/How) + Stakeholder-Mapping (inkl. Betriebsrat/Compliance, falls relevant).
   - Gib eine Kommunikationssequenz (4 Wochen) mit Kanal, Ziel, Message, Owner.

8) 30-60-90-Tage-Plan (oder passend zu {{TIME_HORIZON}})
   - Plan in Wochen-Sprints, mit Meilensteinen, Deliverables, KPI-Checkpoints.
   - Enthält: Workshop-Agenda (2h) + Follow-up-Mechanik.

9) Qualitätscheck (am Ende)
   - Prüfe dich selbst gegen diese Kriterien:
     - Umsetzbar ohne zusätzliche Tools? 
     - Messbar mit klaren KPIs?
     - Reduziert Meetings & erhöht Entscheidungsqualität?
     - Delegation explizit verbessert?
     - Risiken und Compliance adressiert?
   - Liste 5 Annahmen, die du getroffen hast, und wie man sie validiert.

## Stilregeln
- Schreibe klar, prägnant, executive-ready. 
- Keine Buzzword-Suppe. Wenn du einen Fachbegriff nutzt, erkläre ihn in 1 Satz.
- Nutze Tabellen dort, wo Vergleich/Priorisierung hilft.
- Vermeide "Es kommt darauf an" ohne konkrete Option A/B/C.
- Verwende keine Emojis.

## Zusätzliche Perspektive (optional)
Wenn {{FUNCTIONS_IN_SCOPE}} nicht leer ist, liefere pro Funktion 3 spezifische Effizienzhebel (z. B. Vertrieb, Ops, IT, HR).
```

---

## 3) Output-Format (Empfohlen) — Struktur zum direkten Export in Confluence/Word

- H1: Leitfaden zur Effizienz für Führungskräfte — {{CLIENT_COMPANY}}
- H2: Executive Summary
- H2: Diagnose-Framework
- H2: Effizienz-Betriebsmodell
- H2: KPI- & Messsystem
- H2: Maßnahmenkatalog (Quickwins / Mid-Term / Structural)
- H2: AI & Automatisierung
- H2: Change & Kommunikation
- H2: 30-60-90-Tage-Plan
- H2: Qualitätscheck & Annahmen

---

## 4) Mini-Beispiel (ausgefüllte Variablen)

```text
{{CLIENT_COMPANY}} = "Kunde GmbH"
{{INDUSTRY}} = "Managed IT Services"
{{ORG_SIZE}} = "250"
{{LEADERSHIP_LEVEL}} = "Bereichsleitung"
{{TOP_OBJECTIVES}} = "1) Entscheidungszeiten halbieren 2) Meeting-Zeit -30% 3) Liefertreue +15%"
{{CURRENT_PAIN_POINTS}} = "Zu viele Abstimmungen, unklare Verantwortlichkeiten, Status-Meetings ohne Outcome"
{{TOOLS_STACK}} = "M365, Teams, Jira, Confluence"
{{TIME_HORIZON}} = "90 Tage"
{{CONSTRAINTS}} = "DSGVO, begrenzte Kapazität (2 FTE), Betriebsrat involviert"
```

---

## 5) Profi-Tipp (optional) — Iterationsprompt für Feinschliff

> Nutze nach dem ersten Output diesen Prompt, um das Ergebnis "zu härten":

```text
Überarbeite den Leitfaden als "v2 — audit-ready". 
1) Kürze alles um 20%, ohne Informationsverlust.
2) Ersetze allgemeine Aussagen durch konkrete Standards (Templates, Regeln, Checklisten).
3) Identifiziere 5 Stellen mit hoher Umsetzungsunsicherheit und liefere je eine Alternative (A/B) inkl. Entscheidungskriterium.
4) Stelle sicher, dass jede Maßnahme eine KPI + Definition of Done enthält.
Gib am Ende ein Delta-Log (v1→v2) in 10 Punkten.
```
