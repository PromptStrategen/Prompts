> **Zweck:** Dieser Prompt erzeugt einen **maximal detaillierten, didaktisch sauberen Leitfaden** für einen **Meisterkurs** zum Thema **Generationsunterschiede** (z. B. Baby Boomer, Gen X, Millennials, Gen Z, Gen Alpha) – **aus Sicht einer Marketing-/Brand-/Kommunikationsagentur**, inklusive Curriculum, Übungen, Fallstudien, Materialien, Evaluations- und Transferplan.  
> **Hinweis:** Platzhalter **{{…}}** sind für den User-Input gedacht.

---

## 1) User-Input: Variablenblock (ausfüllen)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_TYPE}} = "Marketing- & Digitalagentur"
{{CLIENT_BRAND}} = "Beispiel GmbH"
{{INDUSTRY}} = "B2B SaaS / IT-Services"                  # z.B. Retail, Healthcare, Legal, Manufacturing
{{REGION}} = "DACH"
{{TARGET_AUDIENCE_PRIMARY}} = "Führungskräfte & Teamleads"
{{TARGET_AUDIENCE_SECONDARY}} = "HR, Marketing, Vertrieb, Produkt"
{{AUDIENCE_SIZE}} = 25                                    # Teilnehmende
{{DELIVERY_MODE}} = "Live-Workshop"                       # Live-Workshop | Hybrid | Self-paced | Inhouse
{{COURSE_LEVEL}} = "Meisterkurs"                          # Grundlagen | Fortgeschritten | Meisterkurs
{{COURSE_DURATION_HOURS}} = 12                             # Gesamtstunden
{{MODULE_COUNT}} = 6                                      # Anzahl Module
{{SESSION_LENGTH_MIN}} = 90                               # je Session
{{TIMEBOX_QA_MIN}} = 15                                   # je Session
{{LANGUAGE}} = "Deutsch"
{{TONE}} = "Corporate, prägnant, wissenschaftlich sauber"
{{BRAND_VOICE}} = "klar, modern, kein Buzzword-Overkill"
{{LEARNING_GOALS_TOP3}} = [
  "Generationsstereotype von evidenzbasierten Mustern unterscheiden",
  "Kommunikations- und Kollaborationsstrategien generationenübergreifend etablieren",
  "Marketing-/Employer-Branding-Maßnahmen pro Zielsegment wirksam aussteuern"
]
{{CONTEXT_CONSTRAINTS}} = [
  "DSGVO/Datenschutz berücksichtigen (z.B. bei internen Umfragen)",
  "Keine pauschalen Abwertungen oder Stereotype; differenziert und respektvoll",
  "Praxisfokus: umsetzbare Tools, Vorlagen, Checklisten"
]
{{ORG_CONTEXT}} = "Wachsende Organisation (200 MA) mit gemischten Teams, Remote/Hybrid"
{{CURRENT_PAIN_POINTS}} = [
  "Missverständnisse in Kommunikation (Chat vs. Meetings)",
  "Unterschiedliche Feedback-Erwartungen",
  "Konflikte bei Change- & Tool-Einführung"
]
{{EXISTING_ASSETS}} = [
  "Brand-Guidelines",
  "Kommunikationsleitfaden",
  "Onboarding-Unterlagen"
]
{{SUCCESS_METRICS}} = [
  "Teilnehmerzufriedenheit (NPS) ≥ 45",
  "Wissenszuwachs (Pre/Post-Test) ≥ 25%",
  "Transfer: 3 konkrete Maßnahmen pro Team innerhalb 30 Tage"
]
{{RISK_SENSITIVITIES}} = [
  "Altersdiskriminierung vermeiden",
  "Kulturelle Diversität mitdenken",
  "Keine Diagnosen/psychologischen Ferndiagnosen"
]
{{DELIVERABLE_FORMAT}} = "Leitfaden + Slides-Outline + Übungen + Handouts + Evaluationsplan"
{{OUTPUT_LENGTH}} = "sehr ausführlich"
```

---

## 2) Master-Prompt (Copy & Paste)

```text
Du bist ein interdisziplinäres Expertenteam in einer Rolle:
(1) Organisationspsychologie & Arbeitssoziologie (evidenzbasiert, bias-sensibel),
(2) Didaktik/Instructional Design (Meisterkurs-Architektur),
(3) Marketingstrategie & Kommunikation (Agenturperspektive, Zielgruppenlogik),
(4) HR/People & Change Management (Transfer in Organisation),
(5) Daten-/Messkonzept (KPI, Evaluation, Experimentdesign light).

DEIN ZIEL:
Erstelle einen hochqualitativen, detailtiefen Leitfaden für einen Meisterkurs zum Thema "Generationsunterschiede" für {{CLIENT_BRAND}} im Kontext {{INDUSTRY}} in {{REGION}} – entwickelt von {{AGENCY_NAME}} ({{AGENCY_TYPE}}).
Der Leitfaden muss fachlich korrekt, respektvoll (anti-stereotyp), praxisnah und umsetzungsorientiert sein.

WICHTIGE LEITPLANKEN:
- Nutze aktuelle, allgemein anerkannte Erkenntnisse (ohne Quellenhalluzinationen). Wenn du unsicher bist, formuliere als Annahme und markiere es.
- Vermeide platte Generationen-Klischees. Stelle klar: Generationenmodelle sind Heuristiken, keine Diagnosen.
- Berücksichtige Diversitätsdimensionen (Kultur, Bildung, Branche, Persönlichkeit, Lebensphase) als Moderatoren.
- Fokus: Konkrete Handlungsfähigkeit für Führung, Teams und Marketing/HR.
- Datenschutz/Compliance: Vorschläge für interne Daten/Umfragen immer DSGVO-konform formulieren.
- Sprache: {{LANGUAGE}}. Ton: {{TONE}}. Brand Voice: {{BRAND_VOICE}}.

KONTEXT:
- Zielgruppen: Primär {{TARGET_AUDIENCE_PRIMARY}}, sekundär {{TARGET_AUDIENCE_SECONDARY}}
- Teilnehmende: {{AUDIENCE_SIZE}}
- Durchführung: {{DELIVERY_MODE}}
- Kurslevel: {{COURSE_LEVEL}}
- Gesamtdauer: {{COURSE_DURATION_HOURS}} Stunden
- Module: {{MODULE_COUNT}} (je Session {{SESSION_LENGTH_MIN}} Minuten, Q&A {{TIMEBOX_QA_MIN}} Minuten)
- Organisationaler Kontext: {{ORG_CONTEXT}}
- Schmerzpunkte: {{CURRENT_PAIN_POINTS}}
- Vorhandene Assets: {{EXISTING_ASSETS}}
- Erfolgsmetriken: {{SUCCESS_METRICS}}
- Sensitivitäten/Risiken: {{RISK_SENSITIVITIES}}
- Constraints: {{CONTEXT_CONSTRAINTS}}

AUSGABEFORMAT (bitte exakt einhalten):
1) Executive Summary (max. 200 Wörter): Nutzenversprechen, Zielbild, erwartete Effekte
2) Kurs-Blueprint (Übersichtstabelle): Module, Lernziele, Inhalte, Methoden, Materialien, Zeitplan, Output je Modul
3) Detaillierter Leitfaden pro Modul:
   - Modulziel (SMART)
   - Kernkonzepte (präzise, verständlich)
   - "Myth vs. Reality": typische Fehlschlüsse + korrigierende Perspektiven
   - Praxis-Transfer: konkrete Handlungsprinzipien (Do/Don’t)
   - Interaktive Übung(en): Ablauf, Dauer, Rollen, Material, Moderationsskript, Debrief-Fragen
   - Mini-Case aus {{INDUSTRY}}: Ausgangslage, Konflikt, Analyse, Lösungspfad, Lessons Learned
   - Artefakte: Checklisten, Templates, Gesprächsleitfäden, One-Pager (ausformuliert)
   - Messpunkt: wie wir Lernfortschritt/Transfer messen (Pre/Post, Beobachtung, Mini-Assessment)
4) Slide-Outline (pro Modul 8–12 Slides): Titel + 3–6 Bulletpoints + Sprecher-Notizen
5) Handouts/Materialien (druckfertig in Textform):
   - "Generationenübergreifende Kommunikation" (1–2 Seiten)
   - "Feedback & Konflikt" (1–2 Seiten)
   - "Change/Tool-Einführung" (1–2 Seiten)
   - "Marketing/Employer Branding Segmentierung" (1–2 Seiten)
6) Evaluations- & ROI-Plan:
   - Messlogik zu {{SUCCESS_METRICS}} (Definition, Messmethode, Zeitpunkt, Owner)
   - Kurzfragebogen (10–12 Items; Likert + 2 offene Fragen)
   - Pre/Post-Test (10 Fragen; gemischt: MC + kurze Antworten)
   - Transfer-Plan 30/60/90 Tage: Maßnahmen, Verantwortliche, Follow-up-Rituale
7) Risiken & Ethik:
   - Risiken (z.B. Altersdiskriminierung, Stereotype, "Generation-Bashing")
   - Gegenmaßnahmen (Moderationsregeln, Sprache, Beispiele, Safe-Checks)
8) "Agency Package" (für {{AGENCY_NAME}}):
   - Projektplan (2–4 Wochen) zur Vorbereitung + Durchführung + Follow-up
   - Rollen/RACI (Agentur vs. Kunde)
   - Optionales Upsell: interne Kommunikationskampagne, HR-Toolkit, Führungskräfte-Coaching

QUALITÄTSGATES (selbst prüfen, dann final ausgeben):
- Keine diskriminierenden Formulierungen, keine Pauschalurteile.
- Jede Empfehlung ist operationalisierbar (wer macht was bis wann womit).
- Jedes Modul enthält: Übung + Artefakt + Mini-Case + Messpunkt.
- Konsistenter roter Faden von Problem → Konzept → Praxis → Messung.

WICHTIG:
Wenn dir Informationen fehlen, triff plausible Annahmen und markiere sie als "Annahme:" – stelle KEINE Rückfragen, sondern liefere trotzdem das vollständige Ergebnis.
```

---

## 3) Optional: Beispiel-Variablen (Kurzvariante)

> Falls du schnell testen willst, kopiere den Block und passe nur Branche/Brand an.

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_BRAND}} = "Ich-möchte-KI-verstehen GmbH"
{{INDUSTRY}} = "B2B SaaS / IT-Services"
{{REGION}} = "DACH"
{{TARGET_AUDIENCE_PRIMARY}} = "Teamleads & Bereichsleitung"
{{DELIVERY_MODE}} = "Inhouse"
{{COURSE_DURATION_HOURS}} = 8
{{MODULE_COUNT}} = 4
{{LANGUAGE}} = "Deutsch"
{{TONE}} = "Corporate, prägnant, evidenzbasiert"
{{CURRENT_PAIN_POINTS}} = ["Kommunikation", "Feedback", "Change-Resistenz"]
{{SUCCESS_METRICS}} = ["NPS ≥ 45", "Transfer: 2 Maßnahmen/Team in 30 Tagen"]
```

---

## 4) Mini-Tuning-Hinweise (für maximale Output-Qualität)

- Wenn du **mehr Praxis** willst: erhöhe `{{MODULE_COUNT}}` oder setze `{{SESSION_LENGTH_MIN}}` auf 120.
- Wenn du **mehr Marketing** willst: füge in `{{LEARNING_GOALS_TOP3}}` explizit "Segmentierung & Messaging" hinzu.
- Wenn du **mehr HR/Change** willst: ergänze `{{CURRENT_PAIN_POINTS}}` um Recruiting, Retention, Onboarding.
