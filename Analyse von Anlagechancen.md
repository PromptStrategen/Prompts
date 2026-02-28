> **Wichtiger Hinweis (Compliance):** Dieser Prompt dient der **Informationsaufbereitung, Szenario- und Risikoanalyse**. Er ersetzt **keine** Anlageberatung, Steuer- oder Rechtsberatung. Verlange im Output stets eine klare **Abgrenzung**: *keine Empfehlung, keine Aufforderung zum Kauf/Verkauf*, sondern **strukturierte Analyse**.  

---

## 1) Copy-&-Paste Prompt (mit Variablen)

### System/Role (optional, aber empfohlen)
```text
Du bist ein: (1) Investment-Research-Analyst, (2) Risikomanager, (3) Datenprüfer (Fact-Checker), (4) Redakteur für Executive Briefings.
Dein Auftrag: Erstelle einen Leitfaden, mit dem ein Team Anlagechancen standardisiert analysiert. 
Arbeite strikt: belegbar, transparent, mit Annahmen, Szenarien, Unsicherheiten und Quality-Gates.
Keine Anlageempfehlung. Keine individuellen Handlungsanweisungen. Kein “Kaufen/Verkaufen/Halten”.
```

### User Prompt (Hauptprompt)
```text
# Kontext
Du arbeitest für {{AGENCY_NAME}} (Marketing-/Digitalagentur) und erstellst für {{CLIENT_BRAND}} einen professionellen Leitfaden, wie Anlagechancen analysiert werden können.
Der Leitfaden soll so strukturiert sein, dass er:
- von Nicht-Finanzprofis verstanden wird (Executive + Ops)
- aber methodisch auf dem Niveau eines Research-Teams bleibt
- jederzeit auditierbar ist (Annahmen, Quellenfelder, Rechenwege, Risiken)

# Zielbild (Definition of Done)
Erstelle einen Leitfaden inkl.:
1) Prozess-Blueprint (End-to-End) von Screening → Due Diligence → Entscheidungsvorlage → Monitoring
2) Bewertungs- & Risiko-Frameworks (z. B. Cashflow-Logik, Multiples, Risiko-Rendite, Sensitivitäten)
3) Daten-/Quellen-Checkliste + Validierung (inkl. Datenqualität, Bias, Widersprüche)
4) Szenarioanalyse (Base/Bull/Bear) + Trigger-Logik
5) Template für Executive Summary (1 Seite) + Deep-Dive (5–10 Seiten Struktur)
6) KPI- und Quality-Gates (z. B. Mindestdatenabdeckung, Plausibilitätschecks, Dokumentationsgrad)
7) Beispiel (durchgespielt) anhand eines fiktiven Assets/Unternehmens mit Dummy-Zahlen (klar als Beispiel markieren)
8) “Red Flags”-Katalog + typische Denkfehler (Cognitive Biases) und Gegenmaßnahmen
9) Monitoring-Plan (Rebalancing-Regeln auf Analyse-Ebene, nicht als Empfehlung), inkl. Alerts & Review-Zyklen
10) Ergebnis muss in sauberem Markdown mit Überschriften, Tabellen-Templates und Checklisten kommen.

# Input-Daten (User füllt aus)
{{ANALYSE_SCOPE}} = "Privatanleger-Leitfaden | KMU-Treasury | Family-Office light | Bildung/Content"
{{ASSET_KLASSE}} = "Aktien | ETFs | Anleihen | Immobilien | Krypto | Rohstoffe | Private Equity"
{{REGION}} = "DACH | EU | USA | Global | Emerging Markets"
{{ZEITHORIZONT}} = "kurz (0–12M) | mittel (1–5J) | lang (5–15J)"
{{RISIKOPROFIL}} = "konservativ | ausgewogen | chancenorientiert"
{{ZIELSETZUNG}} = "Kapitalerhalt | Wachstum | Cashflow | Diversifikation | Inflationsschutz"
{{WAEHRUNG}} = "EUR | USD | gemischt"
{{LIQUIDITAET}} = "täglich handelbar | monatlich | quartalsweise | illiquide"
{{RESTRIKTIONEN}} = "keine Hebelprodukte; ESG-Screening; Ausschlüsse; regulatorische Vorgaben; Steuerrahmen nur allgemein"
{{DATENVERFUEGBARKEIT}} = "hoch | mittel | niedrig"
{{KONKRETE_CHANCE}} = "Kurzbeschreibung der Anlagechance (wenn vorhanden)"
{{BENCHMARKS}} = "z. B. MSCI World, Bloomberg Aggregate, CPI, Euribor"
{{WETTBEWERBSUMFELD}} = "relevante Peers/Alternativen"
{{OUTPUT_TONALITAET}} = "Corporate, prägnant, faktenbasiert (kein Buzzword-Overkill)"
{{SPRACHE}} = "Deutsch"

# Regeln & Guardrails
- Markiere klar: Annahmen vs. Fakten.
- Nutze einheitliche Definitionen (Glossar).
- Baue “Daten fehlen”-Pfad ein: Was tun, wenn Zahlen nicht vorliegen?
- Zeige Berechnungslogik als Formeln/Schritte, ohne externe Tools vorauszusetzen.
- Keine Kursziele, keine Kauf-/Verkaufsempfehlungen.
- Jede Tabelle: Spalte “Quelle/Status (geprüft/ungeprüft)” und “Stand (Datum)”.

# Output-Format
Gib den Leitfaden in folgenden Kapiteln aus (Markdown):
A) Executive Overview (max. 15 Zeilen)
B) Begriffe & Grundlogik (Glossar)
C) Analyseprozess (Phasen + Deliverables)
D) Daten- und Quellen-Framework (Checklisten + Quality)
E) Bewertungsrahmen (Methoden + wann einsetzen)
F) Risiko-Framework (Risikoarten + Messlogik)
G) Szenarien & Sensitivitäten (Templates)
H) Entscheidungsvorlage (1-Pager Template) + Deep-Dive Struktur
I) Red Flags & Bias-Katalog
J) Monitoring & Review (Plan + Trigger)
K) Durchgespieltes Beispiel (Dummy-Daten) inkl. Tabellen
L) Appendix: Templates (copy-ready Tabellen)

# Starte jetzt.
```

---

## 2) Erwarteter Output (Blueprint) – Strukturvorgabe

### A) Executive Overview (max. 15 Zeilen)
- Ziel, Scope, Assetklasse, Zeithorizont  
- High-level Prozess (Screening → DD → Memo → Monitoring)  
- Qualitätsprinzipien (Auditierbarkeit, Transparenz, Szenarien, Unsicherheit)  

### B) Begriffe & Grundlogik (Glossar)
**Muss enthalten (Beispiele):**  
- Rendite (nominal/real), Volatilität, Drawdown, Liquidität, Duration, Kreditrisiko, Korrelation  
- “Margin of Safety” (Sicherheitsmarge) als Konzept (ohne Empfehlung)  
- Unterschied: **Prognose** vs. **Szenario** vs. **Annahme**  

---

## 3) Templates (Copy-ready) – Tabellen & Checklisten

### 3.1 Screening-Template (Shortlist)
| Kriterium | Definition | Wert | Bewertung (1–5) | Notizen | Quelle/Status | Stand |
|---|---|---:|---:|---|---|---|
| These | Warum interessant? |  |  |  |  |  |
| Assetklasse | Kategorie |  |  |  |  |  |
| Liquidität | Handelbarkeit |  |  |  |  |  |
| Komplexität | Verständnis/Struktur |  |  |  |  |  |
| Hauptrisiken | Top-3 |  |  |  |  |  |
| Datenlage | Verfügbarkeit/Qualität |  |  |  |  |  |
| Fit zu Zielsetzung | Cashflow/Wachstum/etc. |  |  |  |  |  |

### 3.2 Daten-Qualitätsgate (Minimum)
**Pass/Fail Kriterien (Beispiel, anpassbar):**
- Mindestdatenabdeckung: **{{MIN_DATENABDECKUNG}} = 80%** der Kernfelder  
- Keine Widersprüche in Kernzahlen (Umsatz/CF/Schulden) ohne Erklärung  
- Quellenstatus: ≥ **2 unabhängige** Primär-/Sekundärquellen pro Kernannahme (wenn möglich)  
- Aktualität: Datenstand ≤ **{{MAX_DATENALTER}} = 12 Monate** (oder begründen)  

### 3.3 Due-Diligence Checkliste (DD)
- **Business/Case-Logik:** Werttreiber, Preissetzung, Wettbewerb, Moat/Kommoditisierung  
- **Finanzen:** Umsatzqualität, Margen, Cash Conversion, Verschuldung, Covenants  
- **Risiko:** Markt, Kredit, Liquidität, Operativ, Regulatorik, Tail-Risks  
- **Struktur:** Gebühren, Vehikel, Kontrahenten, Verwahrung  
- **Recht/Steuer:** nur allgemeine Hinweise, Verweis auf Fachprüfung  
- **ESG/Exclusions:** falls Restriktionen gesetzt  

### 3.4 Bewertungs-Toolkit (Wann welche Methode?)
| Methode | Geeignet für | Benötigte Daten | Stärken | Grenzen | Output |
|---|---|---|---|---|---|
| DCF (Discounted Cashflow) | stabile Cashflows | CF-Prognosen, WACC | logikbasiert | stark annahmengetrieben | Fair-Value-Spanne |
| Multiples (P/E, EV/EBITDA) | Peer-Vergleich | Peers, Kennzahlen | schnell | Zyklus-/Accounting-Bias | Vergleichsspanne |
| Szenario-NPV | Projekte/Realoptionen | Szenarien, Wahrscheinlichkeiten | Unsicherheit explizit | Subjektive Wahrscheinlichkeiten | Erwartungswert |
| Risiko-Parität (konzeptionell) | Portfolio-Sicht | Volas/Korr. | Diversifikation | Dateninstabilität | Risiko-Beiträge |

### 3.5 Risiko-Katalog (Taxonomie)
| Risikotyp | Beschreibung | Messgröße(n) | Frühindikatoren | Mitigation auf Analyse-Ebene |
|---|---|---|---|---|
| Marktrisiko | Preis/Indexschocks | Volatilität, Beta, VaR* | Makro-Daten, Sentiment | Szenarien, Stress-Test |
| Liquiditätsrisiko | Spread/Exit | Spread, Volumen | Orderbuch, News | Liquiditätsabschlag |
| Kreditrisiko | Ausfall/Spread | Rating, CDS, DSCR | Covenants, Refinanzierung | Bonitätsanalyse |
| Regulatorik | Regeln ändern | Qualitativ + Trigger | Gesetzesentwürfe | Compliance-Review |

\*VaR nur als Konzept/Orientierung erläutern, nicht als Sicherheitsgarantie darstellen.

### 3.6 Szenario-Template (Base/Bull/Bear)
| Variable | Base | Bull | Bear | Begründung | Quelle/Status | Stand |
|---|---:|---:|---:|---|---|---|
| Wachstum |  |  |  |  |  |  |
| Marge |  |  |  |  |  |  |
| Diskontsatz |  |  |  |  |  |  |
| Multiple |  |  |  |  |  |  |

---

## 4) Beispiel (Dummy) – Mini-Demo (kompakt)

> **Beispiel-Asset:** “FiktiveTech AG” (Achtung: Dummy-Zahlen, nur Demonstration)

**Annahmen (Dummy):**
- Umsatz aktuell: 100 Mio. EUR, Wachstum Base: 8% p.a.  
- EBITDA-Marge Base: 18%  
- Diskontsatz (WACC) Base: 10%  
- Terminal-Multiple (EV/EBITDA) Base: 10x  

**Output in der Analyse:**
- Fair-Value-Spanne (nicht Punktwert)  
- Sensitivität: Wachstum ±2pp, WACC ±1pp, Multiple ±2x  
- Red Flags: Konzentrationsrisiko (Top-3 Kunden), Working-Capital Sprünge, regulatorische Abhängigkeit  

---

## 5) Qualitätssicherung (Quality Gates)

### QG1 – Daten
- Kernfelder vollständig oder sauber begründet fehlend  
- Quellenstatus dokumentiert (geprüft/ungeprüft)  
- “Single Source of Truth”-Felder definiert  

### QG2 – Modelllogik
- Formeln nachvollziehbar beschrieben  
- Einheiten konsistent (EUR vs. USD, nominal vs. real)  
- Sensitivitäten gerechnet/erklärt  

### QG3 – Risiko
- Top-5 Risiken mit Frühindikatoren  
- Tail-Risks explizit benannt  
- Korrelationen/Abhängigkeiten adressiert  

### QG4 – Entscheidungsvorlage
- Executive Summary 1 Seite, klare Kernaussagen  
- Annahmen/Fakten getrennt  
- Offene Fragen + ToDos für Fachprüfung  

---

## 6) Output-Pakete (Deliverables)

1) **Executive Brief (1 Seite)**  
2) **Research Memo (5–10 Seiten Struktur, inkl. Tabellen)**  
3) **Model-Logik (Formel- und Rechenschritte in Textform)**  
4) **Monitoring-Plan (Trigger, Frequenz, Verantwortlichkeiten)**  

---

## 7) Bonus: Prompt-Add-ons (für maximale Tiefe)

### 7.1 “Skeptischer Prüfer” (Red Team)
```text
Übernimm die Rolle eines skeptischen Prüfers. Suche aktiv nach:
- Annahme-Overreach, Datenlücken, Narrative Bias
- Widersprüchen in Zahlen/Logik
- Missing Risks, die typischerweise übersehen werden
Gib eine Liste mit “Critical Issues” + “Fix/Check Actions”.
```

### 7.2 “Uncertainty First”
```text
Erzeuge eine Unsicherheits-Matrix:
- Welche Aussagen sind robust?
- Welche sind fragil (annahmengetrieben)?
- Welche Daten würden die Aussage am stärksten verändern?
```

