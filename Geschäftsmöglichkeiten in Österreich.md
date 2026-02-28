## 1) Ziel
Dieser Prompt erzeugt einen **strategischen, detailtiefen Leitfaden** zu **Geschäftsmöglichkeiten in Österreich** – inkl. Marktlogik, Wettbewerbsbild, Go‑to‑Market-Optionen, Risiken/Compliance, Förderkulisse und einem **umsetzbaren 90‑Tage Plan**.  

---

## 2) User‑Input – Variablenblock (Beispielwerte als Platzhalter)
> **Hinweis:** Werte anpassen/ersetzen. Alles in `{{...}}` sind Platzhalter.

```text
{{AGENCY_NAME}}            = "Prompt Strategen"
{{AGENCY_POSITIONING}}     = "B2B Marketing- & Automatisierungsagentur (AI/Automation-first)"
{{CLIENT_TYPE}}            = "KMU (50–500 MA) + Tech-Startups"
{{TARGET_INDUSTRIES}}      = ["IT-Services", "Industrie & Fertigung", "Energie/Netzbetreiber", "Call-Center/Customer Ops", "Handel"]
{{TARGET_REGIONS_AT}}      = ["Wien", "Oberösterreich", "Steiermark", "Tirol"]  # optional
{{BUSINESS_MODELS}}        = ["SaaS", "Managed Service", "Projekt + Retainer", "Marketplace/Partnervertrieb"]
{{TIME_HORIZON}}           = "2026–2028"
{{BUDGET_RANGE_EUR}}       = "2.000–25.000 €/Monat (Marketing/Automation)"
{{RISK_APPETITE}}          = "mittel"
{{DIFFERENTIATORS}}        = ["DSGVO-by-design", "schnelle MVPs (<30 Tage)", "messbarer ROI", "Security-First"]
{{CHANNEL_PRIORITIES}}     = ["LinkedIn", "SEO/Content", "Partner (Systemhäuser)", "Events/Meetups", "Outbound E-Mail"]
{{COMPETITOR_TYPES}}       = ["Systemhäuser", "No/Low-Code Agenturen", "Big4/Consulting", "Lokale Performance-Agenturen"]
{{SUCCESS_METRICS}}        = ["MRR", "CAC Payback < 6 Monate", "NRR > 110%", "SQL-Rate", "Pipeline-Wert"]
{{OUTPUT_LANGUAGE}}        = "Deutsch"
{{DEPTH_LEVEL}}            = "maximal"   # "kompakt" | "standard" | "maximal"
{{SOURCE_POLICY}}          = "Nur verlässliche Primär-/Autoritätsquellen; keine erfundenen Zitate."
{{RECENCY_RULE}}           = "Quellen bevorzugt aus den letzten 12–18 Monaten; ältere nur bei Grundlagen."
```

---

## 3) Copy‑&‑Paste Prompt (1 Prompt, vollständig)

```text
Du bist ein Senior-Strategie-Team aus {{AGENCY_NAME}} ({{AGENCY_POSITIONING}}): 
(1) AI/Automation Strateg:in, (2) B2B Growth Marketer:in, (3) Marktanalyst:in, (4) Legal/Compliance-Reviewer:in (AT/EU), (5) Finance/Unit-Economics Analyst:in. 
Dein Ziel ist ein auditierbarer, umsetzungsorientierter Leitfaden zu Geschäftsmöglichkeiten in Österreich.

KONTEXT
- Zielkunden: {{CLIENT_TYPE}}
- Zielbranchen: {{TARGET_INDUSTRIES}}
- Zielregionen in AT: {{TARGET_REGIONS_AT}}
- Bevorzugte Geschäftsmodelle: {{BUSINESS_MODELS}}
- Zeithorizont: {{TIME_HORIZON}}
- Budgetrahmen: {{BUDGET_RANGE_EUR}}
- Risikoappetit: {{RISK_APPETITE}}
- Differenzierung: {{DIFFERENTIATORS}}
- Go-to-Market Kanäle: {{CHANNEL_PRIORITIES}}
- Wettbewerbsumfeld (Typen): {{COMPETITOR_TYPES}}
- Erfolgsmetriken: {{SUCCESS_METRICS}}
- Sprache: {{OUTPUT_LANGUAGE}}
- Detailtiefe: {{DEPTH_LEVEL}}

ARBEITSMODUS / QUALITÄTSSTANDARD
1) Arbeite evidenzbasiert: Recherchiere aktuelle Daten/Regeln/Programme zu Österreich (AT) und EU. 
   - Bevorzuge Primär-/Autoritätsquellen (z. B. Behörden, Kammern/Verbände, offizielle Statistik/Reports, bekannte Research-Provider).
   - Halte dich an {{SOURCE_POLICY}} und {{RECENCY_RULE}}.
2) Keine Halluzinationen: Wenn Daten unsicher sind, kennzeichne sie als Annahme und liefere einen Verifikationspfad.
3) Trenne sauber: (a) Fakten mit Quelle, (b) Annahmen, (c) Schlussfolgerungen/Empfehlungen.
4) Ergebnis muss „Executive-ready“ sein: klarer Business-Nutzen, priorisiert, mit Next Steps, Risiken und KPIs.
5) Verwende Unternehmensjargon, aber bleibe präzise und ohne Buzzword-Watte.

AUFGABE
Erstelle einen Leitfaden: „Geschäftsmöglichkeiten in Österreich (AT) – Opportunity Playbook für {{CLIENT_TYPE}}“.
Der Leitfaden soll die attraktivsten Opportunities im österreichischen Markt identifizieren, erklären und priorisieren – mit konkreten, realistischen Umsetzungswegen für Marketing, Vertrieb und (falls relevant) Automation/AI.

ERWARTETE DELIVERABLES (Struktur zwingend einhalten)
A) Executive Summary (max. 1 Seite)
   - Top 5 Opportunities (kurz + warum jetzt)
   - Erwarteter Impact (qualitativ + wenn möglich quantitativ)
   - Quick Wins (0–30 Tage) vs. Strategic Bets (30–180 Tage)

B) Markt- & Umfeldanalyse Österreich (AT)
   - Makro-Trends (PESTEL: Politisch/Ökonomisch/Sozial/Technologisch/Ökologisch/Recht)
   - Branchenlogik je Zielbranche: Treiber, Budgetverhalten, Kaufprozesse, typische Entscheider
   - Nachfrageindikatoren (Suchtrends, Investitionssignale, Förderprogramme, Cluster, Events)

C) Opportunity Map (Priorisierungsmatrix)
   - Mindestens 10 Opportunities als Liste
   - Pro Opportunity:
     1) Problem/Need (aus Kundensicht)
     2) Zielkunden-Segment (ICP) + Buying Center
     3) Value Proposition (klar in 1–2 Sätzen)
     4) Monetarisierung (Preismodell + grobe Preisanker)
     5) Go-to-Market Ansatz (Kanal + Messaging + Offer)
     6) Aufwand/Komplexität (Low/Med/High)
     7) Risiko/Compliance (DSGVO, Branchenregeln, Werbung, Daten, Security)
     8) Messbare KPIs (Leading + Lagging)
     9) Evidenz (Quellen/Indizien)
   - Danach: Priorisierung nach „Impact × Feasibility“ inkl. kurzer Begründung.

D) Wettbewerbsbild & Differenzierung
   - Typische Wettbewerber je Opportunity ({{COMPETITOR_TYPES}})
   - Differenzierungshebel mit {{DIFFERENTIATORS}}
   - „Win-Themes“ (3–5 zentrale Argumentationslinien) + Gegenargumente

E) Förder- & Partnerlandschaft (AT)
   - Relevante Förder-/Finanzierungsoptionen, Programme, Anlaufstellen (mit Quellen)
   - Partnerkanäle: Kammern/Verbände/Cluster, Systemhäuser, Plattformen, Events
   - „Partner Play“: Wie wir binnen 30 Tagen 3–5 Partner-Intro-Gespräche erzeugen

F) Go-to-Market Blueprint (operativ)
   - Positionierung (1 Satz) + Kernbotschaft (3 Varianten)
   - Angebotsarchitektur: 3 Pakete (Entry / Growth / Premium) mit Umfang, Ergebnis, Preisanker
   - Funnel: TOFU/MOFU/BOFU Content- und Sales-Assets (konkret)
   - Outbound-Sequenz (E-Mail + LinkedIn) als Template
   - Landingpage-Struktur (Sektionen + Copy‑Hinweise)

G) 90‑Tage Umsetzungsplan (wöchentlich)
   - Woche 1–2: Setup & Research, Woche 3–6: Pipeline-Building, Woche 7–12: Conversion & Delivery
   - Für jede Woche: Ziele, Maßnahmen, Owner-Rollen, Artefakte, KPIs, Risiken/Mitigations

H) KPI‑Dashboard (Definitionsreif)
   - KPI‑Tabelle: Definition, Formel, Datenquelle, Zielwert, Reporting-Frequenz

I) Risiken, Annahmen, offene Punkte
   - Top 10 Risiken + Gegenmaßnahmen
   - Annahmenliste + wie zu validieren
   - Offene Fragen, die ein reales Projekt-Kickoff klärt

J) Quellenverzeichnis
   - Saubere Quellenliste (Titel + Herausgeber + Datum + Link)
   - Keine erfundenen Quellen.

FORMAT
- Gib alles als Markdown aus.
- Nutze Tabellen, wo sie die Lesbarkeit erhöhen (Opportunity-Liste, KPI-Dashboard, 90‑Tage Plan).
- Schreibe {{OUTPUT_LANGUAGE}}.

ABSCHLUSS-CHECK (Selbstprüfung, im Output kurz dokumentieren)
- Sind Aussagen zu Programmen/Regeln in AT zeitlich aktuell ({{RECENCY_RULE}})?
- Sind alle Zahlen/Claims entweder belegt oder als Annahme markiert?
- Ist die Priorisierung nachvollziehbar?
- Ist der 90‑Tage Plan operativ ausführbar?
```

---

## 4) Operativer Tipp (für maximale Ergebnisqualität)
- **Depth Tuning:** Setze `{{DEPTH_LEVEL}}` auf `maximal`, wenn du Tabellen + konkrete Textbausteine willst.  
- **Scope-Guard:** Wenn du weniger Output willst, setze `{{DEPTH_LEVEL}} = kompakt` und reduziere Opportunities auf Top 5.

---

## 5) Mini‑Beispiel (wie du den Prompt startest)
Du kopierst Abschnitt **3** und ersetzt nur den Variablenblock in **2**. Dann schickst du den Prompt ans Modell.