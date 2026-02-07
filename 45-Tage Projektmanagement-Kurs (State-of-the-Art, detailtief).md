## Variablen (User-Input) – bitte ausfüllen
- {{ZIELGRUPPE}} = z. B. „Quereinsteiger“, „Junior PMs“, „Team Leads“
- {{VORKENNTNISSE}} = z. B. „keine“, „Scrum Basics“, „PMO-Erfahrung“
- {{BRANCHE}} = z. B. „IT/Software“, „Logistik“, „Bau“, „Behörde“
- {{KURSZIEL}} = z. B. „Job-ready PM“, „IPMA/PMI-Grundlagen“, „Hybrid-PM im Unternehmen“
- {{ZEIT_PRO_TAG_MIN}} = z. B. 45–90
- {{LERNFORMAT}} = z. B. „Self-Study“, „Live-Training“, „Blended“
- {{SPRACHE}} = „Deutsch“
- {{TOOLSTACK}} = z. B. „Jira + Confluence“, „MS Project“, „Trello“, „Excel/Sheets“
- {{ZERTIFIKATSFOKUS}} = z. B. „keiner“, „CAPM-orientiert“, „PRINCE2-Basics“, „IPMA-Basics“
- {{KURSINTENSITÄT}} = z. B. „normal“, „intensiv“
- {{WOCHENENDEN}} = z. B. „frei“, „leichtes Wiederholen“, „voll integriert“
- {{CAPSTONE_PROJEKT_DOMÄNE}} = z. B. „App-Launch“, „Prozessdigitalisierung“, „Rollout“, „Infrastruktur“
- {{ARTEFAKT_TIEFE}} = z. B. „kompakt“, „business-ready“, „enterprise-level“
- {{BEWERTUNG}} = z. B. „Quiz + Abgabe“, „nur Selbstcheck“, „Rubric + Feedback“

---

## Prompt (an das LLM)
Du agierst als **Lead Instructional Designer, Senior Project Manager (Hybrid: PMBOK/PRINCE2 + Agile/Scrum/Kanban), PMO-Architekt und Didaktiker**.  
Deine Aufgabe: Entwickle einen **45-Tage Projektmanagement-Kurs** nach **aktuellen Best Practices** (kompetenzbasiert, outcome-orientiert, praxisnah, messbar). Output ist **sofort einsatzfähig** im Unternehmenskontext.

### Kontext & Zielbild
- Zielgruppe: {{ZIELGRUPPE}}
- Vorkenntnisse: {{VORKENNTNISSE}}
- Branche/Use-Cases: {{BRANCHE}}
- Kursziel: {{KURSZIEL}}
- Lernzeit pro Tag: {{ZEIT_PRO_TAG_MIN}} Minuten
- Lernformat: {{LERNFORMAT}}
- Sprache: {{SPRACHE}}
- Toolstack: {{TOOLSTACK}}
- Zertifikatsfokus: {{ZERTIFIKATSFOKUS}}
- Kursintensität: {{KURSINTENSITÄT}}
- Wochenenden: {{WOCHENENDEN}}
- Capstone-Domäne: {{CAPSTONE_PROJEKT_DOMÄNE}}
- Artefakt-Tiefe: {{ARTEFAKT_TIEFE}}
- Bewertung/Prüfung: {{BEWERTUNG}}

### Arbeitsanweisung (ohne Rückfragen starten)
1. **Wenn Angaben fehlen**, triff **vernünftige Annahmen** und liste sie transparent unter "Annahmen".  
2. Kurs muss **Hybrid-PM** abdecken: Initiierung → Planung → Ausführung/Steuerung → Abschluss; plus Agile-Delivery & Change-Handling.  
3. Jede Lerneinheit ist **deliverable-getrieben**: Am Ende von Tag X existiert ein konkretes Artefakt oder Skill-Nachweis.  
4. Nutze **Microlearning + Praxis**: pro Tag (a) Input, (b) Übung, (c) Output, (d) Selbstcheck.  
5. Kurs baut auf einem **durchgängigen Capstone-Projekt** auf ({{CAPSTONE_PROJEKT_DOMÄNE}}), das alle Artefakte 
"real" benötigt.  
6. Formatiere klar, unternehmensfähig, ohne Marketing-Floskeln.  
7. Kein unnötiges Blabla: **maximale Dichte**, aber lesbar.

---

## Output-Format (verbindlich)

### 0) Executive Summary (1 Seite)
- Nutzenversprechen (Business-Mehrwert)
- Zielkompetenzen (max. 10 Bulletpoints)
- End-Deliverables (Artefaktliste)

### 1) Kursarchitektur
- Kompetenzmodell (z. B. Scope/Time/Cost/Risk/Stakeholder/Quality/Agile/Leadership)
- Lernpfad-Logik (Warum diese Reihenfolge?)
- Didaktik: Input-/Übungs-/Feedback-Mechanik

### 2) 45-Tage Plan (Tabelle)
Erstelle eine Tabelle mit exakt 45 Zeilen (Tag 1–45) und Spalten:
- **Tag**
- **Thema**
- **Lernziel (messbar)**
- **Micro-Input (Kernaussagen)**
- **Praxisübung (konkret, Schrittfolge)**
- **Artefakt/Abgabe (Dateiname/Template)**
- **Tool-Schritt (bezogen auf {{TOOLSTACK}})**
- **Zeitbudget (Minuten, passend zu {{ZEIT_PRO_TAG_MIN}})**
- **Selbstcheck (3–5 Fragen/Criteria)**

### 3) Capstone-Projekt (durchgängig)
- Projekt-Kurzbeschreibung (Scope, Ziele, Nicht-Ziele)
- Meilensteine (mit Tag-Zuordnung)
- Abnahmekriterien / Definition of Done (DoD)
- Risiko-/Änderungslogik (wie im Kurs verwendet)

### 4) Templates & Artefakte (Business-ready)
Liefer **ausfüllfertige** Vorlagen (kurz aber vollständig), mindestens:
- Project Charter
- Stakeholder-Matrix + Power/Interest
- RACI
- WBS (Work Breakdown Structure) + Beispielstruktur
- Terminplan (Gantt-Logik oder Sprint-Plan, je nach Kontext)
- Kosten-/Budget-Baseline (vereinfachtes Modell)
- RAID-Log (Risks, Assumptions, Issues, Dependencies)
- Risiko-Register (Eintritt, Impact, Maßnahmen, Owner)
- Kommunikationsplan
- Change Request (CR) + Entscheidungsworkflow
- Lessons Learned + Abschlussbericht
- Agile Artefakte (Product Goal, Backlog, Sprint Goal, Review/Retro-Format)

**Hinweis:** Artefakte sollen zur {{ARTEFAKT_TIEFE}} passen (kompakt/business-ready/enterprise-level).

### 5) Assessments & Qualitätssicherung
- Wöchentliche Quiz-Struktur (Fragetypen + Beispielitems)
- Bewertungsrubric für Capstone (Kriterien, Punkte, Mindestscore)
- Häufige Fehler (Top 10) + Gegenmaßnahmen

### 6) Manager-Readout (für Stakeholder/HR)
- Was kann ein Teilnehmer nach Tag 45 konkret liefern?
- Einsatzszenarien im Unternehmen
- Empfehlung zur Weiterentwicklung (30-60-90 Tage)

---

## Qualitäts-Gates (vor Abgabe prüfen)
- Konsistenz: Tagesplan referenziert Capstone & Artefakte ohne Lücken
- Realismus: Zeitbudget passt zu {{ZEIT_PRO_TAG_MIN}}
- Progression: Schwierigkeit steigt nachvollziehbar
- Hybrid-Balance: klassisches PM + Agile + Soft Skills
- "Enterprise-tauglich": klare Begriffe, klare Deliverables, klare Kriterien
