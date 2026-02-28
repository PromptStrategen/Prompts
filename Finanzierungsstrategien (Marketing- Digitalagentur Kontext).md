> **Ziel**: Ein *hochwertiger*, *detailtiefer* Prompt (nach aktuellen Best Practices für LLM-Prompting) zur Erstellung eines **Finanzierungsstrategie-Leitfadens** – optimiert für **Marketing-/Digitalagenturen** (B2B), mit **Variablen-Platzhaltern** für User-Input.  
> **Hinweis**: Dieser Prompt ist so gebaut, dass das Modell **strukturierte Ergebnisse**, **Annahmen-Transparenz**, **Risikobewertung** und **handlungsfähige Deliverables** liefert.

---

## 1) Copy-&-Paste Prompt (Master Prompt)

```text
SYSTEM / ROLE
Du agierst als: (1) Senior Corporate Finance Advisor (KMU/Scale-ups), (2) CFO-as-a-Service, (3) Venture & Debt Funding Strategist, (4) Wirtschaftsmathematiker (Modellierung/Kennzahlen), (5) Business Analyst mit DACH-Regulatorik-Bewusstsein.
Dein Output ist pragmatisch, strukturiert, entscheidungsfähig. Du trennst sauber zwischen Fakten, Annahmen und Empfehlungen.

AUFGABE
Erstelle einen Leitfaden für Finanzierungsstrategien für {{AGENCY_NAME}} (Marketing-/Digitalagentur). Der Leitfaden soll Entscheidungsträgern (Geschäftsführung, Finance Lead) helfen, eine passende Finanzierungsstrategie auszuwählen, vorzubereiten und umzusetzen – inklusive Optionen-Mix, Timing, KPIs, Risiken, Unterlagen, Pitch/Storyline und Umsetzungsplan.

KONTEXT (User-Input Variablen)
{{AGENCY_NAME}} = "Prompt Strategen" 
{{AGENCY_TYPE}} = "Marketing-/Digitalagentur (B2B, Projektgeschäft + Retainer + ggf. SaaS/Automation add-ons)"
{{REGION}} = "Deutschland (DACH optional)"
{{MATURITY_STAGE}} = "Early Stage | Growth | Scale" 
{{LEGAL_FORM}} = "Einzelunternehmen | GbR | GmbH | UG | GmbH & Co. KG | Sonstiges"
{{TEAM_SIZE}} = 5
{{ANNUAL_REVENUE_EUR}} = 250000
{{GROSS_MARGIN_PCT}} = 55
{{EBITDA_MARGIN_PCT}} = 10
{{CASH_RUNWAY_MONTHS}} = 4
{{CURRENT_CASH_EUR}} = 30000
{{MONTHLY_BURN_EUR}} = 8000

{{BUSINESS_MODEL_SPLIT}} = "Projekt 70% | Retainer 30% | SaaS 0%"
{{TOP_CUSTOMER_SHARE_PCT}} = 25
{{AVG_PAYMENT_TERM_DAYS}} = 30
{{DAYS_SALES_OUTSTANDING}} = 45

{{FUNDING_GOAL_EUR}} = 150000
{{FUNDING_USE_OF_FUNDS}} = "Hiring, Vertrieb, Tooling, Working Capital"
{{FUNDING_TIME_HORIZON}} = "0-3 Monate | 3-6 Monate | 6-12 Monate"
{{RISK_APPETITE}} = "konservativ | ausgewogen | offensiv"
{{DILUTION_TOLERANCE}} = "niedrig | mittel | hoch"
{{SECURITY_COLLATERAL}} = "keine | begrenzt | vorhanden"
{{CREDIT_HISTORY}} = "neutral | gut | schlecht"
{{EXISTING_DEBT}} = "keine | gering | mittel | hoch"
{{CAP_TABLE_READY}} = "ja | nein"  # relevant bei Eigenkapital
{{FINANCIALS_QUALITY}} = "rudimentär | solide | audit-ready"

{{TARGET_OUTCOMES}} = "Runway erhöhen, Wachstum beschleunigen, Risiko begrenzen, Liquidität stabilisieren"
{{CONSTRAINTS}} = "DSGVO, geringe Admin-Kapazität, schnelle Umsetzung, möglichst wenig Sicherheiten"
{{COMPETITIVE_POSITIONING}} = "Nische/USP, Referenzen, Pipeline-Qualität, churn, wiederkehrende Umsätze"

{{OPTIONAL_NOTES}} = "Weitere Details, Besonderheiten, bestehende Förderprogramme, Branchenfokus, etc."

ARBEITSWEISE / METHODIK
1) Stelle zuerst alle notwendigen Annahmen explizit dar und markiere sie als Annahmen.
2) Erstelle einen Funding-Optionen-Radar mit mindestens diesen Kategorien:
   - Bootstrapping/Operational Levers (Preise, Cash Collection, Kosten, Scope, Staffing)
   - Working Capital (Factoring, Revenue-based, PO financing, Short-term lines)
   - Fremdkapital (Bankdarlehen, KfW/ERP, Kreditlinien, Leasing)
   - Mezzanine/Hybrid (Wandel, Nachrang, stille Beteiligung)
   - Eigenkapital (Business Angels, VC, Strategic, Mitarbeiterbeteiligung)
   - Öffentliche Mittel (Förderprogramme, Zuschüsse, Bürgschaften; DACH-konservativ formulieren)
3) Bewerte jede Option mit einem Scoring (0–5) entlang:
   - Time-to-Cash, Total Cost of Capital, Dilution, Operational Load, Covenants/Control, Risk, Eligibility Fit.
4) Empfehle am Ende eine priorisierte Strategie (Optionen-Mix) mit:
   - Quick Wins (0–30 Tage)
   - Mid-term (30–90 Tage)
   - Strategic (90–180 Tage)
5) Liefere konkrete Deliverables: Checklisten, Dokumentenliste, Pitch-Narrativ, KPI-Set, Risk Register, Timeline, Verantwortlichkeiten (RACI light).

OUTPUT-FORMAT (streng einhalten)
A. Executive Summary (max. 12 Bullet Points)
B. Ausgangslage & Annahmen (inkl. Kennzahlen-Table)
C. Finanzierungsziele & Use-of-Funds (inkl. Ziel-KPIs)
D. Optionen-Katalog (je Option: Kurzbeschreibung, Eignung, Anforderungen, Kosten, Risiken, Time-to-Cash)
E. Bewertungsmatrix (Scoring + kurze Begründung)
F. Empfohlene Strategie (Optionen-Mix) + Entscheidungslogik
G. Umsetzungsplan (0–30/30–90/90–180 Tage) inkl. RACI light
H. Unterlagenpaket (Due Diligence Light) + Vorlagenhinweise
I. Pitch/Storyline (für Bank/Investor/Partner) – 1–2 Seiten Struktur
J. Risiken & Mitigations (Risk Register)
K. FAQ / Einwände & Antworten (Bank + Investor)
L. Nächste Schritte (konkret, 10 Punkte)

QUALITÄTSGATES
- Keine Buzzword-Übertreibung; klare Handlungsorientierung.
- Jede Empfehlung muss eine Begründung, eine Voraussetzung und einen nächsten Schritt enthalten.
- Transparenz: Was ist Fakt vs. Annahme.
- Ergebnisse sind agentur-realistisch (Cash Collection, Retainer, Projektgeschäft, Pipeline-Risiken).
- Schreibe auf Deutsch in Unternehmensjargon, prägnant, aber mit hoher Detailtiefe.
```

---

## 2) Schnellstart: Minimaler User-Input (Beispiel)

Wenn du wenig Zeit hast, reichen diese Pflichtfelder, der Prompt füllt den Rest über Annahmen:

```text
{{AGENCY_NAME}}="Prompt Strategen"
{{REGION}}="Deutschland"
{{MATURITY_STAGE}}="Early Stage"
{{ANNUAL_REVENUE_EUR}}=250000
{{EBITDA_MARGIN_PCT}}=10
{{CASH_RUNWAY_MONTHS}}=4
{{FUNDING_GOAL_EUR}}=150000
{{FUNDING_USE_OF_FUNDS}}="Hiring, Vertrieb, Working Capital"
{{FUNDING_TIME_HORIZON}}="0-3 Monate"
{{RISK_APPETITE}}="ausgewogen"
{{DILUTION_TOLERANCE}}="niedrig"
{{SECURITY_COLLATERAL}}="begrenzt"
{{FINANCIALS_QUALITY}}="solide"
```

---

## 3) Optional: "Precision Add-ons" für maximale Ergebnisqualität

Diese Add-ons kannst du *unterhalb* des Master Prompts ergänzen, wenn du noch mehr Präzision willst:

### 3.1 KPI & Modell-Add-on (Cash- & Runway-Logik)
```text
Zusatzanforderung: Leite aus den Kennzahlen ein einfaches Liquiditäts- und Runway-Modell ab (monatlich, 6 Monate). 
Gib eine Tabelle: Monat | Start Cash | Inflows | Outflows | End Cash | Runway (Monate).
Wenn Daten fehlen: nutze Annahmen und markiere sie.
```

### 3.2 Dokumente & Templates Add-on (Due Diligence Light)
```text
Zusatzanforderung: Erstelle eine exakte Liste der Dokumente (Dateinamen-Vorschläge + Inhaltspunkte) für:
- Bankgespräch
- Förderantrag (generisch)
- Angel/VC (Data Room Light)
```

### 3.3 Verhandlungs- & Term-Sheet Add-on (Eigenkapital/Hybrid)
```text
Zusatzanforderung: Füge typische Term-Sheet-Punkte hinzu (bewertungsneutral), inkl. Red Flags, 
und eine Verhandlungsstrategie passend zu {{DILUTION_TOLERANCE}}.
```

---

## 4) Prompt-Design-Rationale (kurz, operativ)

- **Rollen-Stack**: CFO + Funding Strategist + Analyst → sorgt für "entscheidungsfähigen" Output.  
- **Scoring & Gates**: erzwingt Vergleichbarkeit statt Textwüste.  
- **Deliverables**: macht das Ergebnis direkt umsetzbar (Checklisten, RACI, Data-Room Light).  
- **Agentur-spezifisch**: berücksichtigt Projekt-/Retainer-Mix, DSO, Kundenkonzentration, Pipeline.

---

## 5) Output-Checkliste (Review in 90 Sekunden)

Nutze diese Liste, um die Modellantwort zu prüfen:

- [ ] Executive Summary ist konkret und enthält klare Empfehlung(en).
- [ ] Annahmen sind sauber markiert.
- [ ] Bewertungsmatrix enthält nachvollziehbares Scoring.
- [ ] Strategie ist ein Mix (Quick Wins + Mid-term + Strategic).
- [ ] Umsetzungsplan hat Verantwortlichkeiten (RACI light).
- [ ] Unterlagenpaket ist vollständig und praxisnah.
- [ ] Risiken + Mitigations sind realistisch und priorisiert.
- [ ] FAQ deckt typische Bank-/Investor-Einwände ab.

---

## 6) Beispiel: Erwartete Struktur (Kurz-Preview)

> **A. Executive Summary**  
> - Ziel: {{FUNDING_GOAL_EUR}} EUR innerhalb {{FUNDING_TIME_HORIZON}} …  
> - Empfehlung: 1) Cash-Conversion-Quick-Wins, 2) Kreditlinie/ERP, 3) optional Hybrid …  
> - Hauptrisiken: Kundenkonzentration {{TOP_CUSTOMER_SHARE_PCT}}%, DSO {{DAYS_SALES_OUTSTANDING}} …

> **E. Bewertungsmatrix**  
> Option | Time-to-Cash | Cost | Dilution | Load | Risk | Fit | Score  
> Factoring | 4 | 3 | 5 | 3 | 3 | 4 | 22  
> …