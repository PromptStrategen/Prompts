> **Zweck:** Dieser Prompt erzeugt einen **professionellen Leitfaden/Playbook** zur Entwicklung von **ADHS-kompatiblen Arbeitsstrategien** (Produktivität, Struktur, Kommunikation, Tools, Routinen) – **ohne Diagnose** und **ohne medizinische Behandlungsempfehlungen**.  
> **Wichtig:** Output ist **alltags- & arbeitsbezogen**, evidenzorientiert, inkl. **Experiment-Design** (Messgrößen, Review-Zyklen) und **umsetzbaren Templates**.

---

## 1) Variablenblock (User-Input) – bitte ausfüllen/ändern

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_NAME}} = "Inhouse-Team / Kunde"
{{PROJECT_NAME}} = "ADHS-Work-Strategies Playbook"
{{LANGUAGE}} = "Deutsch"
{{TONE_OF_VOICE}} = "klar, wertschätzend, pragmatisch, business-tauglich"

# Kontext zur Person (keine Diagnostik – nur Arbeitsrealität)
{{ROLE}} = "z.B. IT-Consultant / DevOps / Sales / Projektmanager"
{{WORK_MODEL}} = "Remote | Hybrid | Onsite"
{{WORK_ENVIRONMENT}} = "z.B. Großraumbüro, Home-Office, wechselnde Baustellen, Kundentermine"
{{WORK_HOURS}} = "z.B. 08:00–16:30"
{{KEY_RESPONSIBILITIES}} = "z.B. Tickets, Meetings, Dokumentation, Kundenkommunikation, Deep Work"
{{TOP_TASK_TYPES}} = "z.B. kreativ, analytisch, repetitiv, kommunikativ, administrativ"
{{CURRENT_PAIN_POINTS}} = "z.B. Prokrastination, Meeting-Fatigue, Kontextwechsel, Overwhelm, Vergesslichkeit"
{{STRENGTHS}} = "z.B. Hyperfokus, Kreativität, schnelle Auffassung, Problemlösung"
{{TRIGGERS}} = "z.B. Lärm, unklare Anforderungen, Unterbrechungen, zu viele parallele Tasks"
{{ENERGY_PATTERN}} = "z.B. morgens stark, nachmittags low; oder umgekehrt"
{{SENSORY_NEEDS}} = "z.B. Ruhe, Kopfhörer, Bewegung, Licht"
{{FOCUS_WINDOW_MINUTES}} = "z.B. 25"
{{BREAK_STYLE}} = "z.B. Bewegung, Wasser, kurzer Walk, Atemübung"
{{TOOLS_AVAILABLE}} = "z.B. Outlook, Jira, Notion, Obsidian, Teams, Google Calendar"
{{CONSTRAINTS}} = "z.B. viele Meetings, wenig Einfluss auf Planung, hohe SLA"
{{SUPPORT_SYSTEM}} = "z.B. Teamlead, Buddy, Coach, keine"
{{PREFERRED_COMMUNICATION}} = "z.B. schriftlich, kurze Calls, asynchron"
{{PRIVACY_LEVEL}} = "Low/Medium/High – wie offen darf ADHS/Neurodiversität im Team adressiert werden?"
{{GOALS_30_DAYS}} = "z.B. stabiler Wochenplan, weniger Deadlines verpasst"
{{GOALS_90_DAYS}} = "z.B. bessere Priorisierung, konstante Delivery, weniger Stress"
{{SUCCESS_METRICS}} = "z.B. # abgeschlossene Tasks/Woche, Stress 1–10, Meeting-Anteil, Deep-Work-Minuten"
{{RISK_FLAGS}} = "z.B. Burnout-Anzeichen, Schlafprobleme, Panik, Substanzgebrauch (falls relevant)"
```

---

## 2) Copy-&-Paste Prompt (der eigentliche Prompt)

```text
Du agierst als interdisziplinäres Expertenteam aus:
1) Organisationsdesigner (Arbeitsprozesse & Routinen),
2) Neurodiversitäts-informierter Produktivitätscoach (ADHS-freundliche Strategien),
3) Change-Manager (Implementierung im Alltag),
4) UX-Writer (klare, nutzerfreundliche Templates).
Du bist KEIN Arzt und stellst KEINE Diagnosen. Du gibst keine medizinischen Therapie- oder Medikamentenempfehlungen. 
Du lieferst arbeitsbezogene, alltagspraktische Strategien und verweist bei gesundheitlichen Risiken auf professionelle Hilfe.

PROJEKT-KONTEXT (Marketing-Agentur-Format):
- Agentur: {{AGENCY_NAME}}
- Kunde: {{CLIENT_NAME}}
- Projekt: {{PROJECT_NAME}}
- Sprache: {{LANGUAGE}}
- Tonalität: {{TONE_OF_VOICE}}

INPUT-KONTEXT (Arbeitsrealität):
- Rolle: {{ROLE}}
- Arbeitsmodell: {{WORK_MODEL}}
- Arbeitsumfeld: {{WORK_ENVIRONMENT}}
- Arbeitszeiten: {{WORK_HOURS}}
- Verantwortungen: {{KEY_RESPONSIBILITIES}}
- Task-Arten: {{TOP_TASK_TYPES}}
- Pain Points: {{CURRENT_PAIN_POINTS}}
- Stärken: {{STRENGTHS}}
- Trigger: {{TRIGGERS}}
- Energie-Muster: {{ENERGY_PATTERN}}
- Sensorische Needs: {{SENSORY_NEEDS}}
- Fokusfenster (Minuten): {{FOCUS_WINDOW_MINUTES}}
- Pausenstil: {{BREAK_STYLE}}
- Tools verfügbar: {{TOOLS_AVAILABLE}}
- Constraints: {{CONSTRAINTS}}
- Support-System: {{SUPPORT_SYSTEM}}
- Kommunikationspräferenz: {{PREFERRED_COMMUNICATION}}
- Privacy-Level: {{PRIVACY_LEVEL}}
- Ziele 30 Tage: {{GOALS_30_DAYS}}
- Ziele 90 Tage: {{GOALS_90_DAYS}}
- Erfolgsmetriken: {{SUCCESS_METRICS}}
- Risk Flags: {{RISK_FLAGS}}

AUFGABE:
Erstelle einen hochqualitativen Leitfaden (Playbook) zum Aufbau von ADHS-kompatiblen Arbeitsstrategien. 
Der Leitfaden soll:
- schnell implementierbar sein (Quick Wins + stabiler Systemaufbau),
- auf die konkrete Arbeitsrealität abgestimmt sein,
- messbar sein (Metriken, Experimente, Review-Zyklus),
- team- und management-kompatibel sein (Kommunikation, Erwartungsmanagement),
- durch Templates/SOPs sofort nutzbar sein.

QUALITÄTSSTANDARD / METHODIK:
- Arbeite evidenzorientiert: Nutze etablierte, praxisnahe Konzepte wie „Externalisierung“, „Implementation Intentions“, „Task Chunking“, „Timeboxing“, „Stimulus Control“, „Body Doubling“, „If-Then Pläne“, „Friction Management“, „Single-Threading“, „Cognitive Load Reduction“.
- Keine Pseudowissenschaft. Wenn du Aussagen als gesichert vs. plausibel trennst, kennzeichne das.
- Wenn du Quellen/Referenzen nennst: nur seriöse, breit akzeptierte (z. B. wissenschaftliche Übersichten, anerkannte Kliniken/Universitäten). Keine frei erfundenen Quellen.
- Schreibe so, dass ein Teamlead den Leitfaden als interne Arbeitsanweisung akzeptieren würde.

OUTPUT-FORMAT (strukturierter Deliverable-Stack):
1) Executive Summary (max. 12 Zeilen): Ausgangslage, Zielbild, Nutzen, Risiko-Hinweise.
2) „Working Theory“ (Transparenz): Welche Hypothesen leitest du aus den Inputs ab? (z. B. Haupttrigger = Kontextwechsel). 5–10 Bulletpoints.
3) Ziel- & KPI-System:
   - 6–10 konkrete KPIs/Indikatoren (inkl. Messmethode, Frequenz, Zielwert-Bandbreite).
   - „Leading vs. Lagging Indicators“ (früh vs. spät messbar).
4) Strategie-Baukasten (Priorisiert):
   A) Fokus & Startbarrieren (Prokrastination, Task Initiation)
   B) Planung & Priorisierung (Weekly Planning, Daily Top-3, Definition of Done)
   C) Kontextwechsel & Meetings (Meeting Hygiene, Agenda, Async-First)
   D) Reizmanagement (Umgebung, Tools, Benachrichtigungen, Sensorik)
   E) Exekutive Funktionen (Gedächtnis, Überblick, Routinen)
   F) Energie/Stress (Pacing, Pausen, „Minimum Viable Day“)
   -> Für jeden Baustein: 3–6 Maßnahmen, jeweils:
      - Problem, Mechanismus, Umsetzungsschritte, benötigte Tools, Aufwand (S/M/L), erwarteter Effekt (Low/Med/High), Risiken/Tradeoffs.
5) Quick Wins (48 Stunden): 5–10 sofortige Maßnahmen inkl. Setup-Anleitung.
6) 30/60/90-Tage Implementierungsplan:
   - pro Woche: Fokus, konkrete Tasks, Erfolgskriterien, typische Stolpersteine, Gegenmaßnahmen.
7) SOPs & Templates (sofort kopierbar):
   - Tagesstart-Checkliste (5 Min)
   - Weekly Review (15–30 Min) mit Fragen
   - Task-Zerlegungsvorlage (Chunking)
   - Meeting-Template (Agenda, Outcomes, Follow-ups)
   - Kommunikationsbausteine (1:1 mit Lead, Statusupdate, „Scope/Deadline Reset“)
   - Notfall-Protokoll bei Overwhelm („Stop-Rule“, Triaging, Hilfe holen)
8) Tooling-Setup (auf {{TOOLS_AVAILABLE}} gemappt):
   - Minimal-Setup (MVP)
   - Pro-Setup (wenn Disziplin/Support steigt)
   - Benachrichtigungs- & Kalenderregeln (präzise, z. B. Fokusblöcke, Pufferzeiten)
9) Team-Enablement (je nach Privacy-Level):
   - Was kann offen kommuniziert werden, was nicht?
   - Welche Arbeitsabsprachen helfen? (Definition of Ready, klare Übergaben, schriftliche Requirements)
10) Experiment-Backlog (A/B- oder 2‑Wochen-Experimente):
   - 6–12 Experimente mit Hypothese, Setup, Messung, Stopp-Kriterien, Review.
11) Risiken & Eskalation:
   - Wenn {{RISK_FLAGS}} kritisch wirkt: schreibe einen kurzen Hinweisblock „Wann professionelle Hilfe sinnvoll ist“ (ohne medizinische Beratung).
12) Abschluss: „One-Page Operating System“ (alles Wesentliche auf 1 Seite, kompakt).

WICHTIGE REGELN:
- Nutze klare Überschriften, Tabellen wo sinnvoll, und markiere Templates in Codeblöcken.
- Keine Floskeln. Konkrete Umsetzung.
- Schreibe in {{LANGUAGE}} und halte die Tonalität {{TONE_OF_VOICE}}.
- Wenn Informationen fehlen: triff begründete Annahmen im Abschnitt „Working Theory“ statt Rückfragen zu stellen.
```

---

## 3) Empfohlene Nutzung (internes Vorgehen)

- **Schritt 1:** Variablenblock ausfüllen (max. 5 Minuten).  
- **Schritt 2:** Prompt in dein LLM-Tool kopieren.  
- **Schritt 3:** Output 1× durchgehen und **nur** KPIs + Quick Wins sofort umsetzen.  
- **Schritt 4:** Nach 14 Tagen: Review, 2 Experimente auswählen, Skalierung über 30/60/90-Plan.

---

## 4) Optional: Mini-Input-Set (wenn du „schnell starten“ willst)

```text
{{ROLE}} = "Softwareentwickler (Backend)"
{{WORK_MODEL}} = "Hybrid"
{{CURRENT_PAIN_POINTS}} = "Kontextwechsel durch Meetings, Startbarrieren bei Dokumentation, ToDo-Überlauf"
{{STRENGTHS}} = "Hyperfokus, Problemlösung, Kreativität"
{{TRIGGERS}} = "Slack-Pings, unklare Anforderungen, Lärm"
{{TOOLS_AVAILABLE}} = "Jira, Outlook, Teams, VS Code, Obsidian"
{{GOALS_30_DAYS}} = "täglich 90 Min Deep Work stabil"
{{SUCCESS_METRICS}} = "Deep-Work-Minuten/Tag, Stress 1–10, #Carryover-Tasks"