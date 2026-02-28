> **Zielbild:** Dieser Prompt lässt ein LLM einen **praxisfähigen Leitfaden** erstellen, um **Ergebnisse (KPIs) für Marketing-/Growth-Maßnahmen** belastbar vorherzusagen – inkl. Datenanforderungen, Modelllogik (einfach → fortgeschritten), Validierung, Risiko- und Szenario-Management sowie Management-tauglicher Kommunikation.

---

## 1) Variablenblock (User-Input)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_NAME}} = "Beispiel GmbH"
{{INDUSTRY}} = "B2B SaaS"
{{REGION}} = "DACH"
{{PRODUCT_OFFER}} = "SaaS-Abo, 3 Preispakete"
{{PRIMARY_GOAL}} = "MRR-Wachstum"
{{FORECAST_HORIZON}} = "90 Tage"                 # z. B. 30/60/90/180 Tage
{{CHANNELS}} = ["LinkedIn Ads","Google Search","SEO","Email","Webinar"]
{{TARGET_AUDIENCE}} = "IT-Leitung & Ops, 50–500 MA"
{{BASELINE_PERIOD}} = "letzte 12 Monate"         # Datenhistorie für Baseline
{{AVAILABLE_DATA_SOURCES}} = [
  "GA4",
  "CRM",
  "Ads Manager",
  "Billing/Stripe",
  "Marketing Automation"
]
{{KPI_DEFINITIONS}} = [
  {"kpi":"Leads","definition":"neue qualifizierte Leads pro Woche"},
  {"kpi":"SQLs","definition":"Sales Qualified Leads pro Woche"},
  {"kpi":"CAC","definition":"Kosten pro Neukunde"},
  {"kpi":"MRR","definition":"Monthly Recurring Revenue"},
  {"kpi":"Conversion Rate","definition":"Besucher→Lead→SQL→Kunde"}
]
{{CONSTRAINTS}} = [
  "DSGVO-konform",
  "keine Black-Box ohne Erklärbarkeit",
  "Budgetänderungen müssen als Szenario abbildbar sein"
]
{{BUDGETS}} = {
  "total_monthly": 25000,
  "by_channel": {"LinkedIn Ads":12000,"Google Search":8000,"SEO":3000,"Email":2000}
}
{{BUSINESS_CONTEXT}} = [
  "Sales-Cycle: 45–75 Tage",
  "ACV: 6.000–18.000 EUR",
  "Seasonality: Q4 stärker",
  "Sales-Team: 3 AEs + 1 SDR"
]
{{RISK_TOLERANCE}} = "mittel"                    # niedrig | mittel | hoch
{{REPORTING_STYLE}} = "Executive + Operativ"     # nur Executive | nur Operativ | beides
{{LANGUAGE}} = "Deutsch"
```

---

## 2) Copy-&-Paste Prompt

```text
Du agierst als:
1) Growth-/Marketing-Analytics Lead (Agentur {{AGENCY_NAME}}),
2) Wirtschaftsstatistiker:in (Forecasting & Kausalität),
3) Data Scientist (messbare Modelle, Validierung),
4) BI-/Tracking-Architekt:in (Datenqualität, Instrumentierung),
5) Strategieberater:in (Management-taugliche Entscheidungslogik).

Auftrag:
Erstelle einen **Leitfaden zur Ergebnisvorhersage (Forecasting Playbook)** für {{CLIENT_NAME}} in der Branche {{INDUSTRY}} (Region: {{REGION}}). Der Leitfaden soll ein Team in die Lage versetzen, **Marketing- und Growth-Ergebnisse** über {{FORECAST_HORIZON}} **vorherzusagen**, **zu validieren** und **entscheidungsrelevant** zu reporten.

Kontext (bindend):
- Angebot/Produkt: {{PRODUCT_OFFER}}
- Primäres Ziel: {{PRIMARY_GOAL}}
- Zielgruppe: {{TARGET_AUDIENCE}}
- Kanäle: {{CHANNELS}}
- Baseline-Zeitraum: {{BASELINE_PERIOD}}
- Datenquellen: {{AVAILABLE_DATA_SOURCES}}
- KPI-Definitionen: {{KPI_DEFINITIONS}}
- Budgets: {{BUDGETS}}
- Business-Kontext: {{BUSINESS_CONTEXT}}
- Constraints: {{CONSTRAINTS}}
- Risiko-Toleranz: {{RISK_TOLERANCE}}
- Reporting-Stil: {{REPORTING_STYLE}}
- Sprache: {{LANGUAGE}}

Erwartetes Ergebnis:
Liefer einen strukturierten Leitfaden, der **ohne zusätzliche Rückfragen** umgesetzt werden kann. Verwende **klare Überschriften**, **Checklisten** und **Beispieltabellen**. Wo Zahlen fehlen, nutze **Formeln, Platzhalter und Annahmen** – markiere Annahmen explizit.

Pflicht-Module (müssen alle enthalten sein):
A) KPI-Framework & Messkette
- Mappe die KPIs entlang der Funnel-Stufen (Impression → Klick → Visit → Lead → SQL → Kunde → MRR).
- Definiere Messfenster (Attribution Window), Lags (Sales-Cycle), Kohortenlogik.
- Leite ab: Welche KPIs sind **Leading** vs. **Lagging** Indicators?

B) Daten-Readiness & Instrumentierung
- Erstelle eine **Data-Readiness-Checkliste** (Tracking, CRM-Felder, UTM-Konventionen, Consent/DSGVO, Identity/Matching).
- Definiere eine **Minimum Data Schema** (Felder + Datentypen) für GA4/CRM/Ads/Billing.
- Liefere einen Plan zur Datenbereinigung (Missingness, Dedupe, Outliers, Bot-Traffic).

C) Forecasting-Ansätze (3 Reifegrade)
1) **Heuristik/Deterministisch**: Funnel-Formeln + Conversion-Rates + Budget→Klick→Lead (mit Bandbreiten).
2) **Zeitreihen-Baseline**: Seasonality, Trend, Moving Average/ETS (konzeptionell), Lag-Features.
3) **Causal / Incrementality**: Experimente (Geo-Split, Holdout), MMM/DiD (nur konzeptionell, kein Overclaim).

Für jeden Reifegrad:
- Voraussetzungen (Daten, Team, Tools)
- Vorgehen Schritt-für-Schritt
- Stärken/Schwächen
- Typische Fehler und Gegenmaßnahmen
- Output: Welche Entscheidungen kann man damit sicher treffen?

D) Szenario- und Sensitivitätsanalyse
- Erstelle mindestens 3 Szenarien: **Base / Upside / Downside**.
- Zeige, wie Budget, Conversion Rates, CPL/CAC, Sales-Cycle-Länge die Forecasts beeinflussen.
- Liefere eine **Sensitivitätsmatrix** (z. B. CVR ±20%, Budget ±20%).

E) Unsicherheit, Risiken, Quality Gates
- Definiere Unsicherheitskommunikation: Konfidenzbänder, Worst/Best Case, Risiko-Register.
- Lege Quality Gates fest (z. B. Datenvollständigkeit, Drift, Backtesting-Metriken wie MAPE/SMAPE).
- Füge eine „Stop/Go“-Logik hinzu (wann Forecasts nicht veröffentlichen).

F) Validierung & Backtesting
- Vorgehen: Train/Test-Splits, Rolling Forecast Origin, Holdout-Zeiträume.
- Metriken: MAPE/SMAPE, Bias, Coverage der Intervalle.
- Dokumentiere „Forecast Accountability“: Versioning, Annahmen-Log, Change-Control.

G) Executive Reporting & Operational Cadence
- Liefere ein Reporting-Template: 1-Seiter (Executive) + Operative Detailseite.
- Definiere Meeting-Rhythmus (Weekly Ops, Monthly Exec).
- Empfehle Visuals (ohne Grafiken zu erzeugen): KPI-Trend, Funnel, Waterfall (Incrementality), Szenario-Bänder.

H) Umsetzungspaket (90-Tage Plan)
- Roadmap in 3 Phasen (0–30 / 31–60 / 61–90 Tage) inkl. Deliverables, Rollen (RACI), Aufwandsabschätzung.
- Tool-Empfehlungen auf Ebene „Kategorie“ (z. B. BI-Tool, CDP, Experimentation), ohne Marken-Zwang.
- Definition der Minimal-Viable-Forecasting-Lösung (MVF): Was ist das kleinste Set, das echte Entscheidungen verbessert?

Anforderungen an Stil & Qualität:
- Unternehmensjargon, klar, prägnant, dennoch detailtief.
- Keine „Magie“ behaupten: Trenne sauber zwischen Korrelation und Kausalität.
- Jede wesentliche Empfehlung muss einen **praktischen Umsetzungsschritt** enthalten.
- Nutze Tabellen, Checklisten, und Beispielrechnungen mit Platzhaltern.
- Schließe mit einer **kurzen Zusammenfassung**: „Was wir morgen tun“, „Worauf wir verzichten“, „Risiken“.

Ausgabeformat:
- Word Dokument mit sauberer Gliederung (H2/H3), Tabellen.
- Wo sinnvoll: Beispiel-Formeln (z. B. Leads = Clicks * CVR, MRR = New Customers * ARPA).
- Keine externen Links. Keine Quellenangaben. Keine Emojis.
```

---

## 3) Kurzbeispiel: Minimal-Input (für schnelle Nutzung)

```text
{{CLIENT_NAME}}="Acme B2B SaaS"
{{FORECAST_HORIZON}}="90 Tage"
{{CHANNELS}}=["Google Search","LinkedIn Ads","SEO"]
{{PRIMARY_GOAL}}="MRR-Wachstum"
{{BASELINE_PERIOD}}="letzte 6 Monate"
{{AVAILABLE_DATA_SOURCES}}=["GA4","CRM","Ads","Billing"]
{{BUDGETS}}={"total_monthly":15000,"by_channel":{"Google Search":7000,"LinkedIn Ads":6000,"SEO":2000}}
```

---

## 4) Qualitätscheck (intern, optional)

- [ ] KPI-Definitionen sind messbar und eindeutig (Zähler/Nenner, Zeitfenster).
- [ ] Funnel-Lags & Sales-Cycle wurden berücksichtigt.
- [ ] Szenarien enthalten Bandbreiten und klare Treiber.
- [ ] Validierung/Backtesting ist beschrieben und operationalisierbar.
- [ ] Kausalität wird nicht behauptet ohne Experiment-/Incrementality-Design.
- [ ] Roadmap liefert Rollen, Deliverables, Quality Gates.