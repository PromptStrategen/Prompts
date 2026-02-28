> **Zweck:** Dieser Prompt erzeugt einen **hochqualitativen, detaillierten Leitfaden zur Anmietungsstrategie** (Büro/Einzelhandel/Lager/Produktion) für ein Unternehmen – inkl. Entscheidungslogik, KPI-Set, Verhandlungstaktik, Risiko-/Compliance-Checks und Umsetzungsfahrplan.  
> **Nutzung:** Variablen ausfüllen → kompletten Prompt 1:1 in dein LLM kopieren.

---

## 1) Variablenblock (User-Input Platzhalter)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing- & Digitalagentur (Strategie, Research, Enablement)"
{{CLIENT_NAME}} = "Muster GmbH"
{{INDUSTRY}} = "B2B SaaS / IT-Services"
{{REGION}} = "Deutschland (DACH optional)"
{{RENTAL_OBJECT_TYPE}} = "Bürofläche"  # Büro | Retail | Lager | Produktion | Mixed
{{TARGET_CITIES}} = ["Berlin", "München", "Köln"]
{{TARGET_RADIUS_KM}} = 25
{{TEAM_SIZE_TODAY}} = 18
{{TEAM_SIZE_12M}} = 28
{{TEAM_SIZE_24M}} = 40
{{WORK_MODEL}} = "Hybrid"  # Remote | Hybrid | Vor-Ort
{{SPACE_REQUIREMENTS}} = {
  "netto_m2_target": 350,
  "meeting_rooms": 3,
  "phone_booths": 4,
  "server_room_required": true,
  "warehouse_m2": 0,
  "parking_spots": 8,
  "barrier_free": true
}
{{BUDGET}} = {
  "max_warm_rent_per_month_eur": 8500,
  "max_cold_rent_per_m2_eur": 18,
  "capex_fitout_eur": 45000,
  "moving_costs_eur": 12000
}
{{LEASE_TERM_PREFERENCE}} = {
  "min_years": 3,
  "target_years": 5,
  "break_option_after_months": 36
}
{{DEADLINE}} = {
  "move_in_latest": "2026-07-01",
  "decision_by": "2026-03-15"
}
{{NON_NEGOTIABLES}} = [
  "ÖPNV-Anbindung < 10 Min Fußweg",
  "Glasfaser verfügbar oder verbindlich beauftragbar",
  "24/7 Zugang",
  "DSGVO-konforme Zutritts-/Besucherregelung möglich"
]
{{NICE_TO_HAVE}} = [
  "Ausbauzustand: bezugsfertig",
  "E-Ladepunkte",
  "Erweiterungsoption im Gebäude"
]
{{CURRENT_SITUATION}} = "Aktuell zu kleine Fläche, Meeting-Raum-Engpässe, steigender Headcount."
{{RISK_TOLERANCE}} = "mittel"  # niedrig | mittel | hoch
{{PROCUREMENT_MODE}} = "Direkt mit Vermieter + optional Makler"  # Direkt | Makler | Ausschreibung
{{LEGAL_REVIEW_AVAILABLE}} = true
{{FINANCE_MODEL_AVAILABLE}} = true
{{BRAND_TONE}} = "Corporate, klar, ohne Buzzword-Overkill"
```

---

## 2) Copy-&-Paste Prompt (Master Prompt)

```text
Du agierst als: 
(1) Senior Real Estate Strategy Consultant (Commercial Leasing),
(2) CFO-nahe Business Analyst (TCO/ROI),
(3) Verhandlungsführer (Mietvertrag, Incentives),
(4) Compliance & Risk Spezialist (DE/EU, DSGVO-relevante Facility-Themen),
(5) Projektleiter (Umzug/Transition).

Kontext:
Wir sind {{AGENCY_NAME}} ({{AGENCY_ROLE}}) und erstellen für {{CLIENT_NAME}} aus der Branche {{INDUSTRY}} in {{REGION}} einen Leitfaden zur Anmietungsstrategie.
Objektart: {{RENTAL_OBJECT_TYPE}}.
Zielregion: {{TARGET_CITIES}} im Umkreis {{TARGET_RADIUS_KM}} km.
Arbeitsmodell: {{WORK_MODEL}}. Teamgröße heute/12M/24M: {{TEAM_SIZE_TODAY}}/{{TEAM_SIZE_12M}}/{{TEAM_SIZE_24M}}.
Anforderungen: {{SPACE_REQUIREMENTS}}.
Budgetrahmen: {{BUDGET}}.
Laufzeitpräferenz: {{LEASE_TERM_PREFERENCE}}.
Zeitplan/Deadlines: {{DEADLINE}}.
Non-Negotiables: {{NON_NEGOTIABLES}}.
Nice-to-have: {{NICE_TO_HAVE}}.
Ist-Situation: {{CURRENT_SITUATION}}.
Risikotoleranz: {{RISK_TOLERANCE}}.
Beschaffungsmodus: {{PROCUREMENT_MODE}}.
Legal Review verfügbar: {{LEGAL_REVIEW_AVAILABLE}}. Finance-Modell verfügbar: {{FINANCE_MODEL_AVAILABLE}}.
Tonality: {{BRAND_TONE}}.

Ziel:
Erstelle einen extrem detaillierten, praxistauglichen Leitfaden zur Anmietungsstrategie, der als internes Entscheidungs- und Umsetzungsdokument dient.

Arbeitsweise (verbindlich):
1) Stelle zuerst eine kurze, strukturierte Annahmenliste auf, falls Daten fehlen (max. 10 Annahmen). Keine Rückfragen.
2) Entwickle dann die Strategie entlang eines klaren Frameworks: Bedarf → Markt → Shortlist → Due Diligence → Verhandlung → Vertrag → Transition/Go-Live.
3) Nutze Entscheidungslogik: Kriterien, Gewichtungen, Scoring, Knock-out-Kriterien.
4) Liefere rechenbare Modelle als Formel-/Tabellenbeschreibung (ohne externe Tools): Warmmiete, Nebenkosten, Ausbau, Incentives, TCO 5 Jahre, Szenario (Base/Best/Worst).
5) Integriere Risikomanagement (operativ, finanziell, rechtlich) + Maßnahmenkatalog.
6) Output muss handlungsorientiert sein: Checklisten, Templates, Beispieltexte, Verantwortlichkeiten, Zeitplan.

Output-Format (Word Dokument) – exakt in dieser Struktur:
A. Executive Summary (max. 12 Bullet Points) + Entscheidungsempfehlung (mit Begründung)
B. Zielbild & Scope (Objektart, Nutzerprofil, Growth, Work-Model, Flächenlogik)
C. Anforderungsprofil
   - C1 Muss/K.O.-Kriterien
   - C2 Soll-Kriterien
   - C3 Flächenprogramm (m², Räume, Infrastruktur) + Wachstumsreserve
D. Markt- & Standortlogik
   - D1 Standortfaktoren (ÖPNV, Kunden/Partner, Recruiting, Kosten, Image)
   - D2 Suchstrategie (Kanäle, Maklersteuerung, Direktansprache, Inserate)
   - D3 Longlist → Shortlist Prozess
E. Bewertungs- & Scoring-Modell
   - E1 Kriterienkatalog mit Gewichtung (Summe 100%)
   - E2 Scoring-Skala (1–5) + Interpretationsregeln
   - E3 Beispiel: ausgefüllte Musterbewertung für 2 fiktive Objekte
F. Wirtschaftlichkeit / TCO / ROI
   - F1 Kostenarten (Kalt, NK, Stellplätze, Energie, IT, Ausbau, Umzug, Betrieb)
   - F2 Incentives (Mietfrei, Ausbauzuschuss, Staffelmiete, Indexmiete) – Wirkung auf TCO
   - F3 5-Jahres-TCO-Modell (Formeln + Beispielrechnung mit {{BUDGET}})
   - F4 Szenarioanalyse (Best/Base/Worst) + Sensitivitäten (Miete/m², NK, Index)
G. Due Diligence (Prüflisten)
   - G1 Technisch (HVAC, Elektro, Netz, Brandschutz, Barrierefreiheit)
   - G2 Rechtlich (Mietvertrag-Red-Flags, Gewährleistung, Betriebskosten, Index/Staffel)
   - G3 Security/DSGVO-nahe Facility-Themen (Zutritt, Besucher, Kamera, Akten/Serverraum)
H. Verhandlungsstrategie
   - H1 Verhandlungsziele & Prioritäten (Give/Get)
   - H2 Taktiken & Anker (erste Angebote, Gegenangebote, BATNA)
   - H3 Musterformulierungen (E-Mail/Letter) für: Angebotsanfrage, Nachverhandlung, LOI
I. Vertragsleitplanken (keine Rechtsberatung, aber praxisnah)
   - I1 Laufzeit, Optionen, Kündigungsrechte, Break-Option
   - I2 Mieter-/Vermieterpflichten, Instandhaltung, Ausbau, Rückbau
   - I3 Betriebskosten & Transparenz (Abrechnung, Caps, Prüfrechte)
   - I4 Index/Staffel – wann sinnvoll, wann riskant
J. Umsetzungsfahrplan (90 Tage bis Einzug + Meilensteine)
   - J1 RACI (Responsible/Accountable/Consulted/Informed)
   - J2 Timeline (Woche 1–12) + Kritischer Pfad
   - J3 Umzugs- & Kommunikationsplan (intern/extern)
K. KPI & Governance
   - KPI Set (Kosten, Qualität, Zeit, Risiko) + Reporting-Rhythmus
   - Entscheidungsmeetings (Gate 1–4)
L. Anhänge / Templates
   - Objekt-Steckbrief (Template)
   - Besichtigungsprotokoll (Template)
   - Scoring-Sheet (Template)
   - Verhandlungs-Tracker (Template)
   - Risk Register (Template)
   - Entscheidungsprotokoll (Template)

Qualitäts-Gates (verpflichtend):
- Keine generischen Floskeln: jede Empfehlung mit konkreter Begründung oder Parameter.
- Zahlen/Modelle: nachvollziehbare Formeln, klar definierte Variablen.
- Konsistenzcheck: Budget vs. Flächenprogramm vs. Laufzeit vs. Deadline muss plausibel sein. Wenn Konflikte: sauber markieren und Lösungsvorschläge liefern.
- Sprache: {{BRAND_TONE}}. Klar, unternehmensgeeignet.

Beginne jetzt. Ausgabe in einem Word Dokument.
```

---

## 3) Mini-Beispiel: So sieht ein guter User-Input aus (kurz)

```text
{{CLIENT_NAME}}="Beispiel IT Services GmbH"
{{RENTAL_OBJECT_TYPE}}="Bürofläche"
{{TARGET_CITIES}}=["München"]
{{TEAM_SIZE_TODAY}}=22
{{TEAM_SIZE_12M}}=30
{{SPACE_REQUIREMENTS}}={"netto_m2_target":420,"meeting_rooms":4,"phone_booths":6,"server_room_required":true,"parking_spots":10,"barrier_free":true}
{{BUDGET}}={"max_warm_rent_per_month_eur":9800,"max_cold_rent_per_m2_eur":19,"capex_fitout_eur":60000,"moving_costs_eur":15000}
{{DEADLINE}}={"move_in_latest":"2026-06-01","decision_by":"2026-03-01"}
{{NON_NEGOTIABLES}}=["ÖPNV < 8 Min","Glasfaser","24/7 Zugang"]
```

---

## 4) Erweiterungen (optional, wenn du noch mehr Druck willst)

Du kannst den Master Prompt am Ende um eines dieser Module ergänzen:

- **Modul “Retail”**: Passantenfrequenz, Sichtachsen, Genehmigungen, Öffnungszeiten, Nachbarschaftsmix.  
- **Modul “Lager/Produktion”**: Rampen, Deckenhöhe, Bodenlast, LKW-Zufahrt, Gefahrstoffe, Schichtbetrieb.  
- **Modul “ESG”**: Energieausweis, Verbrauchsdaten, Sanierungsplan, Green Lease Clauses.