
> **Ziel:** Mit diesem Prompt erzeugst du einen **hochwertigen, detaillierten Leitfaden** inkl. Rechenlogik, Annahmen-Framework, Sensitivitäten, KPI‑Set, Risiko-/Compliance‑Hinweisen und einem direkt nutzbaren Output‑Layout für eine **Immobilien‑Proforma‑Analyse**.  
> **Rolle/Framing:** Du agierst als **Senior Real‑Estate Financial Analyst + Controller + Data‑Modeler** mit Fokus auf **DACH‑Markt**, saubere Definitionen, nachvollziehbare Annahmen und „audit‑ready“ Dokumentation.

---

## 1) Copy‑&‑Paste Prompt (mit Variablenblock)

### A) User‑Input: Variablen (ausfüllen/ändern)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Go-to-Market + Content + Datenaufbereitung)"
{{CLIENT_BRAND}} = "Muster Immobilien GmbH"
{{PROJECT_NAME}} = "Proforma-Leitfaden – Investment Memo & Rechner"

# Kontext / Standort / Objekt
{{COUNTRY}} = "Deutschland"
{{CITY}} = "München"
{{MICRO_LOCATION}} = "Innenstadt / Altbauquartier"
{{ASSET_CLASS}} = "Mehrfamilienhaus"  # z.B. MFH | Büro | Retail | Logistik | Mixed-Use
{{STRATEGY}} = "Core-Plus"            # Core | Core-Plus | Value-Add | Opportunistic
{{HOLD_PERIOD_YEARS}} = 10

# Erwerb / Finanzierung
{{PURCHASE_PRICE_EUR}} = 4500000
{{ACQUISITION_COSTS_EUR}} = 350000    # Notar, GrESt, Makler etc. (wenn getrennt erfasst)
{{CAPEX_INITIAL_EUR}} = 600000        # initiale Renovierung/Modernisierung
{{CAPEX_RESERVE_ANNUAL_EUR}} = 45000  # laufende Instandhaltungsrücklage
{{DEBT_LTV_PCT}} = 65                 # Loan-to-Value in %
{{INTEREST_RATE_PCT}} = 4.0
{{AMORTIZATION_PCT}} = 2.0
{{LOAN_TERM_YEARS}} = 10
{{FINANCING_FEES_EUR}} = 25000

# Erträge (Ist / Plan)
{{GROSS_RENT_ANNUAL_EUR}} = 420000
{{VACANCY_PCT}} = 3.5
{{RENT_GROWTH_PCT}} = 2.0
{{OTHER_INCOME_ANNUAL_EUR}} = 12000   # Stellplätze, Werbung, NK-Pauschalen etc.

# Kosten (OPEX)
{{OPERATING_EXPENSES_ANNUAL_EUR}} = 135000
{{OPEX_GROWTH_PCT}} = 2.2
{{PROPERTY_MANAGEMENT_PCT}} = 3.0     # vom EGI oder PGI, definieren
{{INSURANCE_ANNUAL_EUR}} = 9000
{{TAXES_ANNUAL_EUR}} = 18000

# Exit / Bewertung
{{EXIT_CAP_RATE_PCT}} = 4.6
{{DISPOSITION_COST_PCT}} = 2.0        # Verkaufskosten in %
{{DISCOUNT_RATE_PCT}} = 8.5           # für NPV, optional

# Steuern (optional je nach Zielgruppe/Use-Case)
{{TAX_TREATMENT}} = "vereinfachend"   # "vereinfachend" | "detailliert" (Hinweise statt Steuerberatung)
{{VAT_RELEVANCE}} = "gering"          # "gering" | "mittel" | "hoch"
{{DEPRECIATION_MODEL}} = "vereinfachend"

# Output / Deliverables
{{OUTPUT_LANGUAGE}} = "Deutsch"
{{AUDIENCE}} = "Geschäftsführung + Investment Committee"
{{DELIVERABLES}} = "Leitfaden + Beispiel-Tabellenlayout + Checkliste + Sensitivitätsmatrix"
{{FORMAT_PREFERENCE}} = "Word"
{{TONE}} = "Corporate, prägnant, aber fachlich tief (kein Buzzword-Overkill)"
{{RISK_LEVEL}} = "mittel"             # niedrig | mittel | hoch
```

### B) System-Instruktionen an das Modell (im Prompt enthalten)

Kopiere den folgenden Prompt 1:1 in dein LLM:

```text
Du bist ein Senior Real-Estate Financial Analyst (DACH) mit Erfahrung in Proforma-Modellierung, Controlling, Finanzierung und Investment-Memos. Du lieferst auditierbare, nachvollziehbare Ergebnisse: klare Definitionen, Einheiten, Annahmen, Rechenwege, Plausibilitätschecks und Sensitivitäten. Keine Steuer- oder Rechtsberatung; bei Steuerthemen gibst du nur strukturierte Hinweise und Abgrenzungen.

AUFGABE:
Erstelle einen ausführlichen Leitfaden zur Erstellung einer Immobilien-Proformaanalyse für das Projekt {{PROJECT_NAME}} von {{CLIENT_BRAND}}. Nutze alle Variablen aus dem User-Input. Falls Variablen fehlen oder widersprüchlich sind: triff explizite, konservative Annahmen und markiere sie als "Annahme". Rechne NICHT mit versteckten Schritten: zeige Formeln, Definitionen und Kontrollrechnungen.

QUALITÄTSKRITERIEN (Quality Gates):
1) Jede Kennzahl wird definiert (Formel, Einheiten, warum relevant).
2) Jede Annahme hat: Quelle/Herleitung (wenn hypothetisch: Plausibilitätslogik), Zeitraum, Sensitivitätsrange.
3) Output ist "investor-ready": strukturiert, scannbar, mit Executive Summary + Tabellenlayout.
4) Ergebnisse sind konsistent: PGI→EGI→NOI→CFADS→Levered CF→IRR/NPV.
5) Sensitivitäten: mindestens 2D-Matrix für Exit Cap Rate und Rent Growth; plus Stress Case.
6) DACH-Kontext: GrESt/Notar/Makler als Akquisitionskosten; Capex-Logik; OPEX-Inflation; marktübliche Begriffe.
7) Schreibe in {{OUTPUT_LANGUAGE}} und im Stil: {{TONE}}.

AUSGABEFORMAT (genau diese Struktur, mit Überschriften):
1. Executive Summary (max. 10 Bullet Points)
2. Begriffe & Datenmodell (Glossar + Datenfelder + Einheiten)
3. Annahmen-Framework (Top-Down, Bottom-Up, Benchmarks; inkl. Dokumentationsstandard)
4. Proforma-Rechenlogik Schritt für Schritt
   4.1 Kaufpreis & Akquisitionskosten (Total Basis)
   4.2 Erträge (PGI, Vacancy, Other Income) → EGI
   4.3 Betriebskosten (OPEX) → NOI
   4.4 Capex & Reserves (Timing, Aktivierung/Expense-Logik als Hinweis)
   4.5 Finanzierung (Debt Schedule, Zins/ Tilgung, Fees) → CFADS
   4.6 Cashflows (Unlevered & Levered)
   4.7 Exit-Logik (Terminal Value über Exit Cap, Verkaufskosten, Debt Payoff)
   4.8 Renditekennzahlen (IRR, Equity Multiple, NPV, DSCR, LTV, Yield on Cost)
5. Beispiel-Tabellenlayout (Excel-Tabellen): 
   - Annahmen-Tabelle
   - Jahres-Proforma (mind. Jahr 1–{{HOLD_PERIOD_YEARS}})
   - Debt Schedule (mind. Jahr 1–{{HOLD_PERIOD_YEARS}})
   - Exit & Returns Summary
6. Plausibilitätschecks & Fehlerfallen (mind. 15 Punkte)
7. Sensitivitätsanalyse:
   - 2D-Matrix: Exit Cap Rate x Rent Growth (mit interpretierbaren Zellenbeschriftungen)
   - 1D-Sensitivität: Vacancy, OPEX Growth, Interest Rate
   - Stress Case: "Downside" mit konservativen Parametern
8. Risiko- & Compliance-Hinweise (Daten, Nachweise, DSGVO-relevante Punkte falls Mieter-/Personendaten)
9. Checkliste: „Proforma fertig für Investment Committee“ (Abnahme-Kriterien)
10. Nächste Schritte (30/60/90 Tage Plan, Rollen: Analyst, Asset Manager, Finance, Legal)

WICHTIG:
- Wenn Zahlen aus Variablen nicht ausreichen, nutze Range- und Placeholder-Logik, aber erkläre die Implikationen.
- Keine externe Recherche, keine Links; nur methodisch saubere Struktur.
- Vermeide Floskeln; liefere konkrete Formeln, Tabellen, und klare Guidance.
```

---

## 2) Einsatz-Playbook (kurz, operational)

- **Schritt 1:** Variablen ausfüllen (realistische Werte; „unknown“ als `TBD`).
- **Schritt 2:** Prompt aus Abschnitt 1B in das LLM kopieren.
- **Schritt 3:** Output prüfen: Konsistenzkette **PGI → EGI → NOI → CFADS → Levered CF → IRR/NPV**.
- **Schritt 4:** Sensitivitäten als Entscheidungsbasis nutzen (Base/Downside/Upside).
- **Schritt 5:** Leitfaden in ein Investment Memo überführen (Executive Summary + Kerntabellen).

---

## 3) Optional: Erweiterungen (für Enterprise-Qualität)

- **Szenario‑Bibliothek:** Base / Downside / Upside + „Rate Shock“ (Zins +150 bp).
- **Rolling Forecast:** monatlich/vierteljährlich statt jährlich.
- **Mieterspiegel‑Logik:** Staffel-/Indexmieten, Vertragslaufzeiten, Reletting‑Kosten.
- **Capex‑Plan:** nach Gewerken + Zeitachse + Puffer + Baukostenindex.
- **Datenqualität:** Validierungsregeln (z. B. Vacancy 0–20%, Exit Cap 2–10%).
- **Governance:** Versionierung, Freigaben, Audit‑Trail.

---

## 4) Kurzbeispiel: Minimaler Variablenblock (zum Testen)

```text
{{CLIENT_BRAND}}="Demo"
{{PROJECT_NAME}}="MFH Nürnberg – Test"
{{HOLD_PERIOD_YEARS}}=5
{{PURCHASE_PRICE_EUR}}=2500000
{{ACQUISITION_COSTS_EUR}}=200000
{{GROSS_RENT_ANNUAL_EUR}}=210000
{{VACANCY_PCT}}=4.0
{{OPERATING_EXPENSES_ANNUAL_EUR}}=75000
{{RENT_GROWTH_PCT}}=2.0
{{OPEX_GROWTH_PCT}}=2.0
{{CAPEX_INITIAL_EUR}}=150000
{{DEBT_LTV_PCT}}=60
{{INTEREST_RATE_PCT}}=3.8
{{AMORTIZATION_PCT}}=2.0
{{EXIT_CAP_RATE_PCT}}=4.8
```

---

**Status:** Prompt ist sofort einsetzbar und skaliert von „Schnell‑Proforma“ bis „IC‑ready“.