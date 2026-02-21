## Zielbild
Dieser Prompt erzeugt einen **hochwertigen, detailtiefen Leitfaden** zur **Unterstützung bei Forschungsanträgen** (z. B. DFG, BMBF, EU Horizon, Stiftungen). Output ist so strukturiert, dass Teams schnell von **Idee → Antragslogik → Workpackages → Budgetlogik → Risiken/Compliance → Einreichungsready Assets** kommen.

---

## 1) Copy-&-Paste Master-Prompt (neueste Prompt-Standards, mit Variablen)

> **Hinweis:** Ersetze die Platzhalter im Variablenblock. Danach den gesamten Prompt an dein LLM geben.

### 1.1 Variablenblock (User-Input / Marketing-Agentur-Form)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Research Enablement + Content/Storytelling + Strukturierung)"
{{CLIENT_ORG_NAME}} = "Beispiel Universität / Institut / KMU"
{{CLIENT_ORG_TYPE}} = "Universität|Forschungseinrichtung|KMU|Klinik|NGO"
{{COUNTRY_REGION}} = "Deutschland / EU"
{{FUNDING_PROGRAM}} = "DFG Sachbeihilfe (Beispiel)"
{{CALL_TITLE}} = "Titel/Call-Bezeichnung (falls vorhanden)"
{{DEADLINE_DATE}} = "YYYY-MM-DD"
{{PROJECT_ACRONYM}} = "ACRONYM"
{{PROJECT_TITLE}} = "Arbeitstitel des Projekts"
{{PROJECT_DURATION_MONTHS}} = 36
{{PROJECT_BUDGET_RANGE_EUR}} = "z. B. 300.000–800.000 EUR"
{{DISCIPLINE_DOMAIN}} = "z. B. KI-Sicherheit, MedTech, Materialwissenschaft, Energie"
{{PROBLEM_STATEMENT_1L}} = "1 Zeile: Welches Problem lösen wir?"
{{INNOVATION_1L}} = "1 Zeile: Was ist neu/anders?"
{{IMPACT_1L}} = "1 Zeile: Warum lohnt es sich (Wissenschaft/Industrie/Gesellschaft)?"
{{TARGET_USERS_STAKEHOLDERS}} = "z. B. Kliniken, DevOps-Teams, Behörden, Patient:innen"
{{STATE_OF_THE_ART_SUMMARY}} = "Kurz: Was ist Stand der Forschung/Markt?"
{{KEY_HYPOTHESES}} = "z. B. H1, H2, H3"
{{RESEARCH_QUESTIONS}} = "z. B. RQ1, RQ2"
{{METHODS_TOOLING}} = "z. B. Experimente, Simulation, RCT, qualitative Studien, ML, RAG"
{{DATA_SOURCES}} = "z. B. Datensätze, Sensorik, klinische Daten, Umfragen"
{{ETHICS_PRIVACY_SECURITY}} = "z. B. DSGVO, Ethikvotum, ISO 27001, DPIA"
{{CONSORTIUM_PARTNERS}} = "Partnerliste + Rollen (wenn vorhanden)"
{{TEAM_CAPABILITIES}} = "Kernkompetenzen, Vorarbeiten, Publikationen, IP"
{{TRLS_CURRENT_TARGET}} = "z. B. TRL 3 → TRL 6 (optional)"
{{DELIVERABLE_PREFERENCES}} = "z. B. Leitfaden + Checklisten + Templates + Beispieltexte"
{{TONE}} = "professionell, prägnant, wissenschaftlich sauber, ohne Buzzword-Overkill"
{{LANGUAGE}} = "Deutsch"
{{ASSUMPTIONS_ALLOWED}} = "Ja, aber klar markieren (Annahmen vs. Fakten)"
{{KNOWN_CONSTRAINTS}} = "z. B. max. 15 Seiten, bestimmte Gliederung, Budgetkategorien"
```

### 1.2 Master-Prompt (an das Modell)

```text
Du agierst als:
1) Grant-Writing Lead (DFG/EU/öffentlich geförderte Projekte),
2) Research Methodologist (saubere Forschungslogik, Hypothesen, Methoden),
3) Compliance & Risk Advisor (Ethik/DSGVO/IT-Security),
4) Programm-Manager (Workpackages, Meilensteine, Ressourcen, Gantt),
5) Kommunikationsstratege aus {{AGENCY_NAME}} ({{AGENCY_ROLE}}), der Komplexität in eine überzeugende, klare Storyline übersetzt.

AUFGABE
Erstelle einen Leitfaden zur Unterstützung bei Forschungsanträgen für {{CLIENT_ORG_NAME}} ({{CLIENT_ORG_TYPE}}) im Kontext:
- Förderprogramm: {{FUNDING_PROGRAM}}
- Call/Deadline: {{CALL_TITLE}} | {{DEADLINE_DATE}}
- Projekt: {{PROJECT_ACRONYM}} – {{PROJECT_TITLE}}
- Laufzeit/Budget: {{PROJECT_DURATION_MONTHS}} Monate | {{PROJECT_BUDGET_RANGE_EUR}}
- Domäne: {{DISCIPLINE_DOMAIN}}

INPUT-ZUSAMMENFASSUNG (vom User bereitgestellt)
- Problem: {{PROBLEM_STATEMENT_1L}}
- Innovation: {{INNOVATION_1L}}
- Impact: {{IMPACT_1L}}
- Zielgruppen: {{TARGET_USERS_STAKEHOLDERS}}
- Stand der Forschung: {{STATE_OF_THE_ART_SUMMARY}}
- Hypothesen: {{KEY_HYPOTHESES}}
- Forschungsfragen: {{RESEARCH_QUESTIONS}}
- Methoden/Tooling: {{METHODS_TOOLING}}
- Datenquellen: {{DATA_SOURCES}}
- Ethik/Datenschutz/Security: {{ETHICS_PRIVACY_SECURITY}}
- Konsortium/Partner: {{CONSORTIUM_PARTNERS}}
- Team/Vorarbeiten: {{TEAM_CAPABILITIES}}
- TRL: {{TRLS_CURRENT_TARGET}}
- Constraints: {{KNOWN_CONSTRAINTS}}

ARBEITSWEISE / QUALITÄTSGATES
- Arbeite strikt evidenzorientiert: Trenne klar zwischen (a) Fakten aus Input, (b) plausiblen Annahmen, (c) offenen Punkten.
- Wo Informationen fehlen: erstelle eine "Open Questions"-Liste und biete jeweils 2–3 plausible Optionen (mit Trade-offs).
- Liefere keine Floskeln: jeder Abschnitt muss handlungsorientiert sein (Checklisten, Vorlagen, Beispiele, Entscheidungskriterien).
- Verwende konsistente Terminologie (Problem → Ziel → Ansatz → WPs → Deliverables → Impact → Risiken → Budget).
- Schreibe in {{LANGUAGE}} mit Tonalität {{TONE}}.

OUTPUT-FORMAT (Word, klare Überschriften)
1) Executive Summary (max. 12 Zeilen): was, warum, wie, Erfolgskriterien
2) Antragssystematik: typische Bewertungskriterien (wissenschaftlich, Impact, Machbarkeit, Team, Ressourcen, Risiko)
3) Storyline & Argumentationslogik:
   - Problemraum (Need) → Gap → Innovation → Evidenz → Lösungspfad → Wirkung
   - "Golden Thread”: RQ/Hypothesen ↔ Methoden ↔ Daten ↔ Deliverables ↔ Impact
4) Struktur-Vorlagen (Templates):
   - Abstract (2 Varianten: wissenschaftlich / industrie-nah)
   - Objectives & Research Questions (Formatvorlage)
   - State-of-the-Art + Gap Analysis (Gliederung + Beispielabsätze)
   - Methodik (Design, Messgrößen, Auswertung, Reproduzierbarkeit)
   - Data Management Plan (Kurztemplate: Datenarten, Zugriff, Speicherung, Sharing, Retention)
   - Ethics/Privacy/Security-Plan (Kurztemplate inkl. DPIA/Threat Modeling-Hinweis)
   - Verwertungs-/Dissemination-Plan (Publikationen, OSS, IP, Transfer, Stakeholder)
5) Workpackages & Projektplan:
   - WP-Definitionen (WP1…WPn), Ziele, Tasks, Deliverables, Milestones
   - Abhängigkeiten, Risiken pro WP, Qualitätsmetriken (Definition of Done)
   - Beispiel-Gantt in Textform (Monat 1–{{PROJECT_DURATION_MONTHS}})
6) Budget- und Ressourcenlogik (ohne rechtliche Beratung):
   - Kostenkategorien & typische Begründungslogik
   - Personalkalkulationsprinzipien (FTE, Rollen, Verantwortlichkeiten)
   - Beispiel-Budgetnarrativ (warum diese Ressourcen notwendig sind)
7) Risiko- und Qualitätsmanagement:
   - Risk Register (mind. 10 Risiken): Wahrscheinlichkeit/Impact/Mitigation/Owner
   - Review-Zyklen, interne Qualitätssicherung, Red-Team-Review des Antrags
8) Compliance-Check (DE/EU):
   - DSGVO/Ethik, Datenzugriff, Einwilligungen, Auftragsverarbeitung, Sicherheit-by-design
   - Forschungsintegrität: Reproduzierbarkeit, Bias, Transparenz
9) Einreichungs-Operationalisierung:
   - Timeline rückwärts von {{DEADLINE_DATE}} (Wochenplan)
   - Rollen/RACI (PI, Co-PI, PMO, Legal/DSB, Finance, Partner)
   - Artefakt-Liste (finale Dokumente, Anhänge, Letters of Support)
10) Open Questions (gezielt, priorisiert) + "Next Best Actions” (konkret, 7–14 Tage)
11) Qualitätsprüfung des Outputs (Self-Check):
   - Konsistenzcheck: Objectives ↔ WPs ↔ Deliverables ↔ Impact
   - Bewertungsrubrik (Score 1–5) je Kriterium + Verbesserungsvorschläge

WICHTIG
- Gib, wo sinnvoll, Beispieltexte in Antragsstil (kurz, präzise, ohne Füllwörter).
- Wenn {{ASSUMPTIONS_ALLOWED}} = Ja: markiere Annahmen explizit als "Annahme:".
- Keine Rechtsberatung; formuliere als Best Practices.
- Liefere am Ende eine "Copy-Paste"-Sektion: Abstract-Entwurf + Objectives + WP-Tabelle als Excel.

Starte jetzt und liefere den kompletten Leitfaden in einem einzigen, sauber strukturierten Word-Dokument.
```

---

## 2) Optional: Mini-Addon-Prompts (für Iterationen)

Diese Addons kannst du nach dem Master-Output verwenden, um einzelne Teile zu schärfen.

### 2.1 "Reviewer Mode" (harte Begutachtung)
```text
Handle als strenger Gutachter des Programms {{FUNDING_PROGRAM}}. Bewerte den vorliegenden Entwurf entlang:
- Scientific Excellence, Impact, Implementation, Risk/Compliance, Team Fit
Gib eine Scorecard (1–5), begründe jede Note mit konkreten Textstellen (Zitate max. 1–2 Sätze) und liefere anschließend konkrete Edit-Vorschläge (Rewrite) für die 5 schwächsten Passagen.
```

### 2.2 "WP & Milestones Debugger"
```text
Prüfe die Workpackages auf logische Lücken, fehlende Abhängigkeiten und unklare Deliverables. Erzeuge:
- eine korrigierte WP-Struktur (WP1…WPn),
- pro WP: Deliverables, Milestones, Messkriterien,
- eine Abhängigkeitsliste (DAG in Textform),
- und ein Risiko-Update.
```

### 2.3 "Budget-Narrativ Generator"
```text
Erzeuge ein plausibles Budget-Narrativ passend zu {{PROJECT_BUDGET_RANGE_EUR}} und {{PROJECT_DURATION_MONTHS}} Monaten:
- Rollen/FTE-Logik (ohne konkrete Gehälter),
- Sachmittelkategorien,
- Reisekosten/Dissemination,
- Subcontracts (falls sinnvoll),
und verknüpfe jede Budgetposition direkt mit WPs/Deliverables (Begründungspfad).
```

---

## 3) Verwendungsempfehlung (kurz)
1) Variablenblock ausfüllen  
2) Master-Prompt laufen lassen  
3) Reviewer-Addon ausführen → Schwachstellen fixen  
4) WP/Budget-Addons für Konsistenz & Plausibilität  
5) Finaler Copy-Paste-Block in Antragssystem übernehmen
