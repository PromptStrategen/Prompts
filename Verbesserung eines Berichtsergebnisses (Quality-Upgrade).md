> **Zweck:** Dieser Prompt erzeugt einen **umsetzungsorientierten Leitfaden**, um ein bestehendes **Berichtsergebnis** (Report/Analyse/Statusbericht/Performance-Report) **messbar zu verbessern**: inhaltlich, strukturell, visuell, argumentativ und hinsichtlich Entscheidungsrelevanz.  
> **Output:** Klarer Maßnahmenplan mit Priorisierung, Quick Wins, Qualitätskriterien, Redaktions- und Review-Workflow sowie Beispiel-Textbausteinen.

---

## 1) Copy-&-Paste Prompt (mit Variablen)

### Rolle & Kontext
Du agierst als **Senior Consultant für Reporting & Analytics** in einer **Marketing-/Digitalagentur**. Du kombinierst **Business-Storytelling, Datenanalyse, KPI-Design, Executive-Kommunikation, UX/Visualisierung, Qualitätsmanagement und redaktionelle Exzellenz**.  
Du arbeitest **DSGVO-konform**, nutzt **prüfbare Annahmen**, kennzeichnest Unsicherheiten und vermeidest Buzzword-Overkill.

### Ziel
Erstelle einen **Leitfaden zur Verbesserung** des folgenden Berichtsergebnisses – so, dass er **entscheidungsreif (Executive-ready)** ist und **messbar** bessere Wirkung erzielt (Verständlichkeit, Vertrauen, Handlungsfähigkeit, ROI/Nutzenargumentation).

---

## 2) Variablenblock (User-Input) – bitte ausfüllen/ändern

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_NAME}} = "Beispielkunde GmbH"
{{INDUSTRY}} = "B2B SaaS"
{{REPORT_TITLE}} = "Q1 Performance Report"
{{REPORT_TYPE}} = "Marketing Performance / Management Summary / Projektstatus / Audit / Research"
{{TARGET_AUDIENCE}} = "CEO, CMO, Head of Sales, Team Leads"
{{DECISION_CONTEXT}} = "Budgetfreigabe, Priorisierung, Strategie-Adjustments"
{{REPORT_GOAL}} = "Transparenz schaffen und nächste Maßnahmen ableiten"
{{TIMEFRAME}} = "2026-01-01 bis 2026-03-31"
{{CHANNELS_SCOPE}} = "LinkedIn, Google Ads, SEO, Email"
{{PRIMARY_KPIS}} = "SQLs, CAC, ROAS, Conversion Rate, Pipeline"
{{DATA_SOURCES}} = "Google Ads, LinkedIn Campaign Manager"
{{KNOWN_CONSTRAINTS}} = "Limitierte Tracking-Qualität, kleine Stichprobe, Budgetdeckel"
{{CURRENT_REPORT_TEXT}} = """
[HIER DAS AKTUELLE BERICHTSERGEBNIS EINFÜGEN – Text, Gliederung, Bullet Points, ggf. Tabellen als Text]
"""
{{VISUALS_AVAILABLE}} = "Keine / Screenshots / Charts / Tabellen"
{{TONE}} = "Corporate, prägnant, faktenbasiert"
{{OUTPUT_LANGUAGE}} = "Deutsch"
{{LENGTH_TARGET}} = "2–4 Seiten"
{{DELIVERY_FORMAT}} = "Word Dokument / Google Doc / PPT-Outline"
{{SUCCESS_CRITERIA}} = "C-Level versteht in 5 Minuten die Lage + Top-3 Entscheidungen"
```

---

## 3) Arbeitsauftrag an das Modell

### A) Diagnose (Ist-Zustand)
1. **Executive Summary Check:** Ist die Kernaussage in 5–7 Sätzen klar?  
2. **KPI-Logik & Messbarkeit:** Sind KPIs eindeutig definiert (Formel, Quelle, Zeitraum)?  
3. **Narrative & Begründung:** Gibt es eine stringente Argumentationskette (Problem → Befund → Ursache → Empfehlung → Wirkung)?  
4. **Struktur & Leseführung:** Überschriften, Reihenfolge, Informationshierarchie, Scannability.  
5. **Datenqualität & Risiken:** Tracking-Lücken, Bias, Ausreißer, Unsicherheiten (transparent markiert).  
6. **Handlungsfähigkeit:** Sind Maßnahmen konkret, priorisiert, mit Owner/Impact/Timing?  
7. **Visuelle Klarheit (falls Visuals):** Chart-Typ passend? Achsen/Legenden/Skalen/Annotierungen sauber?  
8. **Compliance & Credibility:** Quellen, Definitionen, Annahmen, DSGVO-Check.

> **Output A:** Eine **kurze, harte Diagnose** als Tabelle: *Befund · Risiko · Verbesserung · Priorität (P0–P2)*.

### B) Zielbild (Soll-Zustand)
Definiere ein **“Gold-Standard”-Gerüst** für diesen Report-Typ:
- 1 Seite: **Management Summary** (Key Outcomes, Top-3 Insights, Top-3 Actions, Risks)  
- 1–2 Seiten: **Performance & Treiberanalyse** (KPI-Tree, Ursachen)  
- 1 Seite: **Empfehlungen & Plan** (Roadmap, Quick Wins, Experimente, Budget-Implikationen)  
- Appendix: **Definitionen, Datenquellen, Methodik, Annahmen**

> **Output B:** Ein **konkretes Inhaltsverzeichnis + Abschnittszweck + “Done-Definition”** je Abschnitt.

### C) Maßnahmenplan (mit Priorisierung)
Erstelle einen Plan in 3 Stufen:
- **Quick Wins (0–48h):** Sofortige Qualitätshebel (Klarheit, Struktur, Executive Summary)  
- **Short Term (1–2 Wochen):** KPI-Definitionen, Datenchecks, Visual-Upgrade, Konsistenz  
- **Mid Term (3–6 Wochen):** Automatisierung, Templates, Governance, QA-Prozess, Dashboarding

Für jede Maßnahme:  
- **Was genau ändern?** (konkret)  
- **Warum?** (Impact)  
- **Wie?** (Schritte)  
- **Owner-Rolle** (z. B. Analyst, PM, Designer, Account Lead)  
- **Aufwand** (S/M/L)  
- **Erfolgsmessung** (KPI oder Qualitätskriterium)

> **Output C:** Eine **priorisierte Maßnahmenliste** (P0/P1/P2) als Tabelle.

### D) Qualitätskriterien (Quality Gates)
Definiere **prüfbare Kriterien**, z. B.:
- Kernaussage in **< 90 Sekunden** verständlich  
- Jede KPI hat **Definition, Quelle, Zeitraum, Vergleich**  
- Jede Empfehlung hat **Impact-Hypothese + Messplan**  
- Charts: **ein Insight pro Visual**, klare Annotation  
- Risiken & Unsicherheit **explizit** (Confidence-Level)  
- Maßnahmen mit **Owner + Deadline**

> **Output D:** Checkliste „**Ready for Client**“ (max. 20 Punkte).

### E) Redaktion & Review (Agentur-Workflow)
Erstelle einen **professionellen Produktionsprozess**:
- Rollen (Lead, Analyst, Reviewer, QA, Design)  
- Review-Schleifen (Faktencheck, Narrative, Compliance)  
- Versionierung/Change-Log  
- Standard-Templates (Executive Summary, KPI-Karten, Recommendations)

> **Output E:** Ein **Workflow** inkl. RACI (Responsible/Accountable/Consulted/Informed).

### F) Beispiel-Verbesserungen direkt am Text
Nimm 1–2 Abschnitte aus `{{CURRENT_REPORT_TEXT}}` und:
- schreibe sie **in “Executive-ready” Version** um  
- zeige **Vorher/Nachher**  
- kommentiere kurz, **welcher Qualitätshebel** genutzt wurde

> **Output F:** Vorher/Nachher + kurze Annotation.

---

## 4) Output-Format (verbindlich)

Gib die Ergebnisse in dieser Reihenfolge aus:
1. **Kurz-Fazit (5–7 Sätze)**  
2. **Output A – Diagnose-Tabelle**  
3. **Output B – Zielbild/Gliederung**  
4. **Output C – Maßnahmenplan (priorisiert)**  
5. **Output D – Quality Gates Checkliste**  
6. **Output E – Workflow + RACI**  
7. **Output F – Vorher/Nachher**  
8. **Annahmen & offene Punkte** (falls Daten fehlen, klar markieren)

Formatierung: **{{DELIVERY_FORMAT}}**, Sprache: **{{OUTPUT_LANGUAGE}}**, Ton: **{{TONE}}**.  
Wenn Informationen fehlen: stelle **maximal 5** gezielte Rückfragen – ansonsten arbeite mit **transparenten Annahmen**.

---

## 5) Optional: “Power-Add-ons” (nur wenn passend)
- KPI-Tree / North Star Metric  
- Confidence-Scoring (hoch/mittel/niedrig) pro Insight  
- “So what?”-Abschnitt: Konsequenzen bei Nicht-Handeln  
- Mini-Experiment-Backlog (Hypothesen, Metriken, Aufwand, Risiko)