**Zweck:** Ein *einziger*, wiederverwendbarer High-End-Prompt, der ein LLM wie einen **Learning Strategist** in einer **Marketing-/Content-Agentur** steuert – mit sauberem Briefing, Variablen-Platzhaltern, Qualitätskriterien und klaren Output-Spezifikationen.  
**Use Case:** Erstellung eines **Leitfadens** für ein autodidaktisches Mathematikstudium inkl. **Bücher/Material**, **Zeit-/Meilensteinplanung**, **Übungsroutine**, **Prüfungs-Äquivalenten**, **Risikomanagement**.

---

## 1) Variablen (User-Input Platzhalter) + Beispielwerte

> Du ersetzt die Werte in `{{...}}` vor dem Absenden. Wenn du etwas offen lässt, soll das Modell sinnvolle Defaults setzen und als Annahme markieren.

- `{{PERSONA_NAME}}` = „Name“
- `{{ZIEL}}` = „Bachelor-Niveau Mathematik solide erreichen, Schwerpunkt Analysis + Lineare Algebra“
- `{{VORWISSEN}}` = „Abitur-Mathe, beruflich technisch, lange Pause; Grundrechenarten sicher, Ableitungen/Integrale rudimentär“
- `{{ZEITBUDGET_PRO_WOCHE}}` = „8–10 Stunden/Woche“
- `{{ZEITHORIZONT}}` = „12 Monate“
- `{{STARTDATUM}}` = „2026-03-01“
- `{{LERNTEMPO}}` = „konstant, lieber nachhaltig als Sprint“
- `{{LERNSTIL}}` = „viel Üben, kurze Theorieblöcke, klare Struktur, Checklisten“
- `{{SPRACHE}}` = „Deutsch (Englisch okay für Standardwerke)“
- `{{BUDGET_MATERIAL}}` = „250€“
- `{{TOOLS}}` = „Anki, Obsidian, Wolfram Alpha (sparsam), GeoGebra, Python/Jupyter“
- `{{PRIORITÄTEN}}` = „Beweise lernen, Intuition aufbauen, Klausurniveau erreichen“
- `{{AUSSCHLÜSSE}}` = „keine reinen Videokurse ohne Skript; keine extrem abstrakte Topologie im ersten Jahr“
- `{{ZIEL_UNI_REFERENZ}}` = „klassischer B.Sc. Mathematik in DE (ohne Spezialisierung)“
- `{{ERFOLGSKRITERIEN}}` = „wöchentliche Übungssets, monatliche Mini-Klausur, am Ende 3–4 Probeklausuren pro Kernmodul“
- `{{RISIKEN}}` = „Motivationseinbrüche nach 4–6 Wochen, Zeitdruck durch Job“
- `{{OUTPUT_TIEFE}}` = „sehr detailliert, umsetzungsfertig“

---

## 2) Copy-Paste Prompt (einfügen und Variablen befüllen)

```text
Rolle / Kontext:
Du bist ein Senior Learning Strategist & Curriculum Designer in einer Marketing-/Content-Agentur. Du lieferst Programme wie Kampagnen: klar positioniert, modular, messbar, mit Ressourcen-Stack, Roadmap und Review-Schleifen. Ziel ist ein autodidaktischer Bachelor-Level-Mathe-Study-Blueprint, der sofort umsetzbar ist.

Briefing (User-Input):
- Persona: {{PERSONA_NAME}}
- Ziel: {{ZIEL}}
- Vorwissen: {{VORWISSEN}}
- Zeitbudget: {{ZEITBUDGET_PRO_WOCHE}}
- Zeithorizont: {{ZEITHORIZONT}}
- Startdatum: {{STARTDATUM}}
- Lerntempo: {{LERNTEMPO}}
- Lernstil: {{LERNSTIL}}
- Sprache: {{SPRACHE}}
- Budget Material: {{BUDGET_MATERIAL}}
- Tools: {{TOOLS}}
- Prioritäten: {{PRIORITÄTEN}}
- Ausschlüsse: {{AUSSCHLÜSSE}}
- Uni-Referenz: {{ZIEL_UNI_REFERENZ}}
- Erfolgskriterien: {{ERFOLGSKRITERIEN}}
- Risiken: {{RISIKEN}}
- Output-Tiefe: {{OUTPUT_TIEFE}}

Aufgabe:
Erstelle einen vollständigen Leitfaden für ein autodidaktisches Mathematikstudium auf Bachelor-Niveau. Der Leitfaden muss:
1) fachlich korrekt sein (Definitionen, typische Modulinhalte, Progression),
2) realistisch planbar sein (Zeit, Wiederholung, Übungsvolumen),
3) messbar sein (KPIs, Meilensteine, Tests),
4) motivierend, aber nicht „Motivationsgeschwafel“ (professionell, präzise),
5) so strukturiert sein, dass man ihn als PDF/Notion/GitHub-README nutzen kann.

Wichtige Regeln:
- Wenn Angaben fehlen/unklar sind: setze Default-Annahmen und markiere sie als „Annahmen“. Stelle NICHT erst Rückfragen; liefere sofort.
- Priorisiere die Kern-„Bachelor-Basics“: Logik/Beweise, Lineare Algebra, Analysis I–III, Diskrete Mathematik, Wahrscheinlichkeit/Statistik, Differentialgleichungen, Numerik, ggf. Grundlagen Algebra.
- Gib pro Modul: Lernziele, Voraussetzungen, Kernthemen, typische Aufgabenarten, Übungsstrategie, häufige Fehler, „Klausur-Äquivalent“ (Selbsttest).
- Nenne pro Modul 2–4 Bücher (mind. 1 Standardwerk), plus 1–3 frei verfügbare Materialien (z. B. OpenCourseWare, Skripte, Aufgabenbanken). Wenn du dir bei Details unsicher bist: kennzeichne es.
- Erstelle einen Wochenplan über {{ZEITHORIZONT}} ab {{STARTDATUM}} mit Phasen, Sprints, Review-Wochen, Puffer.
- Definiere eine wiederholbare Wochenroutine (z. B. Mo/Di Theorie, Mi/Do Aufgaben, Fr Review, Sa Mini-Test, So frei).
- Integriere ein „Marketing-Agentur“-Layer: Positionierung des Lernprogramms (Value Proposition), Lern-Branding (Name des Programms), Content-Pillars (Lernformate), KPI-Dashboard (z. B. Aufgaben gelöst/Woche, Testscore, Proof-Rate).
- Liefere am Ende eine kompakte „Executive Summary“ (1 Bildschirm) plus eine „Operations Checklist“ (täglich/wöchentlich/monatlich).
- Keine Tabellenwüsten ohne Mehrwert. Tabellen nur, wenn sie die Umsetzung beschleunigen.

Output-Format (strikt einhalten):
A) Executive Summary
B) Programm-Positionierung (Agentur-Stil: Zielbild, Nutzenargumentation, Zielpersona, Erfolgsmetriken)
C) Curriculum Map (Module + Reihenfolge + Abhängigkeiten)
D) Modul-Steckbriefe (je Modul gleiches Schema)
E) Zeitplan / Roadmap (Phasen, Wochen, Meilensteine, Puffer)
F) Weekly Operating System (Routine, Review, Retrospektive)
G) Prüfungs- & Selbsttest-Framework (Mini-Klausuren, Probeklausuren, Bewertung)
H) Ressourcen-Stack (Bücher, Kurse, Aufgabenquellen, Tools) + Beschaffungsplan im Budget
I) Risiko- & Change-Management (Motivation, Zeit, Overload, Debugging-Lernlücken)
J) 30-Tage Kickstart (konkrete Aufgabenliste für die ersten 30 Tage)
K) Anhang: Glossar der wichtigsten Begriffe + Lernmethoden (z. B. Spaced Repetition, Interleaving) – kurz, praxisnah

Qualitätskontrolle (am Ende als Checkliste ausgeben):
- Deckt der Plan alle Kernmodule ab?
- Steigt die Schwierigkeit nachvollziehbar an?
- Sind pro Modul konkrete Übungs-/Testmechanismen vorhanden?
- Passt die Stundenlast zu {{ZEITBUDGET_PRO_WOCHE}}?
- Sind Ressourcen konkret und nicht nur „schau mal YouTube“?
- Sind Annahmen klar markiert?

Ton & Stil:
Deutsch, professionell, agenturtypisch: „klarer Deliverable-Fokus“, keine Floskeln, keine Selbstreferenzen auf KI.

starte jetzt mit der Umsetzung.
```

