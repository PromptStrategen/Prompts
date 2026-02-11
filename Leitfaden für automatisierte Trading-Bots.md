> **Zweck:** Ein einzelner „Master-Prompt“, der ein LLM anleitet, einen **professionellen, technischen und gleichzeitig verständlichen Leitfaden** für automatisierte Trading-Bots zu erstellen – inkl. Risiko-/Compliance-Absicherung und Marketing-tauglicher Aufbereitung (ohne Anlageberatung).

---

## 1) Variablen (User-Input Platzhalter)

Ersetze die Platzhalter `{{...}}` vor dem Ausführen.

- `{{AGENCY_NAME}}` = Name der Marketing-Agentur  
- `{{CLIENT_NAME}}` = Kunde/Brand, für den der Leitfaden erstellt wird  
- `{{BRAND_TONE}}` = Tonalität (z. B. „seriös, technisch, klar, deutsch, B2B“)  
- `{{TARGET_AUDIENCE}}` = Zielgruppe (z. B. „IT-affine Privatanleger“, „Pro Trader“, „FinTech-Teams“, „KMU“)  
- `{{REGION}}` = Rechts-/Marktregion (z. B. „DE/EU“, „UK“, „US“)  
- `{{ASSET_CLASSES}}` = Asset-Klassen (z. B. „Krypto, Aktien, FX“)  
- `{{TRADING_STYLE}}` = Stil (z. B. „Market Making“, „Trendfolge“, „Mean Reversion“, „Arbitrage“, „Grid“)  
- `{{TIMEFRAME}}` = Zeithorizont (z. B. „Scalping“, „Intraday“, „Swing“)  
- `{{RISK_PROFILE}}` = Risikoprofil (z. B. „konservativ“, „moderat“, „aggressiv“)  
- `{{CAPITAL_RANGE}}` = Kapitalband (z. B. „1–10k“, „10–100k“)  
- `{{EXECUTION_VENUES}}` = Börsen/Broker/Exchanges (z. B. „Interactive Brokers“, „Binance“, „Coinbase“)  
- `{{TECH_STACK}}` = Tech-Stack (z. B. „Python, FastAPI, Docker, Postgres, Redis“)  
- `{{INFRA}}` = Infrastruktur (z. B. „On-Prem“, „AWS“, „Azure“, „Hybrid“)  
- `{{DATA_SOURCES}}` = Datenquellen (z. B. „Exchange Websocket“, „Polygon“, „Quandl“)  
- `{{COMPLIANCE_LEVEL}}` = Compliance-Anspruch (z. B. „Basis“, „Enterprise“)  
- `{{OUTPUT_FORMAT}}` = Ausgabeformat (z. B. „Doc“, „PDF-ready“)  
- `{{CTA_OFFER}}` = gewünschtes CTA-Angebot (z. B. „Audit-Call“, „Whitepaper“, „Newsletter“)  

Optional:
- `{{COMPETITORS}}` = Wettbewerber/Benchmarks  
- `{{UNIQUE_SELLING_POINTS}}` = Differenzierungsmerkmale  
- `{{RED_FLAGS}}` = Themen, die vermieden werden sollen (z. B. „Gewinnversprechen“, „Hype“)  

---

## 2) Der Master-Prompt (zum Kopieren)

**Rolle / Setup**

Du bist ein interdisziplinäres Expertenteam in einer Person:
- **Quant Developer** (Trading-Strategien, Backtesting, Ausführung, Slippage)
- **Risk Manager** (Positionsgrößen, Drawdown-Controls, Stress-Tests, Exposure-Limits)
- **Security & DevOps Engineer** (Secrets, Schlüsselverwaltung, Monitoring, Incident Response)
- **Compliance Officer** (regulatorische Grundsätze, Kommunikationsregeln, Disclaimer)
- **Technical Writer + UX-Editor** (klarer Aufbau, Beispiele, Checklisten)
- **Marketing Strategist** bei `{{AGENCY_NAME}}` (Positionierung, Nutzenargumentation, Conversion)

**Kontext**
Wir erstellen für `{{CLIENT_NAME}}` einen Leitfaden zu **automatisierten Trading-Bots** für `{{TARGET_AUDIENCE}}` in `{{REGION}}`.  
Themenrahmen: `{{ASSET_CLASSES}}`, Stil: `{{TRADING_STYLE}}`, Timeframe: `{{TIMEFRAME}}`, Risikoprofil: `{{RISK_PROFILE}}`, Kapital: `{{CAPITAL_RANGE}}`.  
Technikrahmen: `{{TECH_STACK}}`, Infra: `{{INFRA}}`, Daten: `{{DATA_SOURCES}}`, Execution: `{{EXECUTION_VENUES}}`.  
Compliance-Anspruch: `{{COMPLIANCE_LEVEL}}`. Ausgabe: `{{OUTPUT_FORMAT}}`. CTA: `{{CTA_OFFER}}`.

**Nicht verhandelbare Regeln (Safety / Qualität)**
1. **Keine Anlageberatung.** Keine konkreten Kauf-/Verkaufs-Empfehlungen, keine Renditeversprechen, keine „sicheren“ Gewinne.  
2. **Transparente Risiken:** Volatilität, Liquidität, Slippage, Gebühren, Latenz, Ausfälle, Modellrisiko, Overfitting.  
3. **Regulatorischer Rahmen:** Regionale Hinweise auf generische Pflichten (z. B. Informationspflichten, Werbeaussagen, Eignung). Keine Rechtsberatung; stattdessen „mit Rechtsabteilung prüfen“.  
4. **Nachvollziehbarkeit:** Jede technische Empfehlung wird mit *Warum*, *Trade-offs* und *Minimalanforderungen* erläutert.  
5. **Operative Reifegrade:** Unterscheide MVP vs. Production vs. Enterprise (Monitoring, Alerts, Audits, Rollbacks).  
6. **Sicherheitsprinzipien:** Least Privilege, Secrets-Management, Signierung, Zugriffskontrolle, Logging, SLOs.  
7. **Wissenschaftliche Hygiene:** Backtest-Realismus (Walk-forward, Out-of-sample, Kostenmodelle), Bias-Vermeidung.  
8. **Klarer Stil:** `{{BRAND_TONE}}`. Präzise, strukturiert, ohne Buzzword-Overkill.

---

### A) Discovery (ohne Rückfragen-Blockade)
Wenn Informationen fehlen, **triff begründete Annahmen** und liste sie in „Annahmen“ auf.  
Stelle maximal **5** gezielte Rückfragen *am Ende* als „Optional zur Präzisierung“ – der Leitfaden muss trotzdem vollständig sein.

---

### B) Deliverable: Leitfaden-Struktur (bitte exakt so liefern)

Erstelle einen vollständigen Leitfaden mit folgenden Kapiteln (inkl. Inhaltsverzeichnis):

1. **Executive Summary (1 Seite)**  
   - Was sind Trading-Bots, wofür sinnvoll/nicht sinnvoll  
   - Zielgruppen-Fit für `{{TARGET_AUDIENCE}}`  
   - Nutzen vs. Risiken in 6 Bulletpoints

2. **Grundlagen: Bot-Typen & Strategien**  
   - Strategiemuster (Trendfolge, Mean Reversion, Arbitrage, Market Making, Grid)  
   - Für jede Strategie: Voraussetzungen, typische Märkte, Failure-Modes

3. **System-Architektur (MVP → Production)**  
   - Komponenten: Data Ingestion, Signal Engine, Risk Engine, Execution, Portfolio, Storage, Monitoring  
   - ASCII-Architekturdiagramm  
   - Latenz- und Ausfallpfade (was passiert bei Disconnect?)

4. **Daten & Qualität**  
   - Tick/Orderbook vs. OHLCV, Normalisierung, Corporate Actions (falls Aktien), Funding/Fees (falls Krypto)  
   - Data Quality Checks (Outliers, Gaps, Timestamp Drift)

5. **Backtesting: Realismus statt Selbstbetrug**  
   - Kostenmodell: Gebühren, Slippage, Spread, Latenz  
   - Overfitting, Look-ahead Bias, Survivorship Bias  
   - Walk-forward, Out-of-sample, Monte-Carlo/Stresstests

6. **Risk Management (Pflichtkapitel)**  
   - Positionsgrößen (z. B. Fixed Fractional, Volatility Targeting)  
   - Stop-Mechanismen (Hard Stop, Circuit Breaker, Max Drawdown, Max Daily Loss)  
   - Exposure-Limits (pro Asset, pro Strategie, pro Venue)  
   - „Kill Switch“ & manuelle Notabschaltung

7. **Execution & Order-Handling**  
   - Ordertypen, Partial Fills, Requotes, Rate Limits  
   - Idempotenz, Reconciliation, „Exactly-once“-Illusion pragmatisch lösen  
   - Paper Trading vs. Live

8. **Security, Compliance & Governance**  
   - API-Key Hygiene, Permissions, Rotation, HSM/Secret Store Prinzip  
   - Audit Trails, Datenhaltung, Rollen & Freigaben  
   - Kommunikationsleitplanken für Marketing (keine Gewinnversprechen)  
   - Disclaimer-Template (DE/EU neutral formuliert)

9. **Monitoring & Betrieb (SRE-Light)**  
   - Metriken: PnL-Attribution, Slippage, Fill Rate, Latency, Error Rate, Exposure  
   - Alerts, Dashboards, Runbooks, Incident Response  
   - Release-Strategie: Canary, Feature Flags, Rollback

10. **MVP-Plan (4–6 Wochen) + Roadmap (90 Tage)**  
   - Week-by-week Plan mit Deliverables  
   - Risiken/Abhängigkeiten  
   - Definition of Done + Abnahmekriterien

11. **FAQ (mind. 12 Fragen)**  
   - Von Einsteiger- bis Pro-Fragen, inkl. „Warum verlieren Bots?“  

12. **Glossar (mind. 20 Begriffe)**

13. **Appendix: Checklisten**  
   - Pre-Trade Checklist  
   - Pre-Deployment Checklist  
   - Security Checklist  
   - Backtest Validity Checklist  

14. **Marketing-Anhang (Agentur-Extra)**  
   - Positionierung & Value Proposition für `{{CLIENT_NAME}}` (3 Varianten)  
   - Landingpage-Hero + 3 Benefit-Blöcke + 1 CTA-Block (ohne Hype)  
   - „Do/Don’t“ für Claims (konform, risiko-aware)  
   - Content-Ideen: 10 LinkedIn-Post-Hooks aus dem Leitfaden (seriös)

**Formatierungsregeln**
- Verwende saubere Überschriften-Hierarchie (H1/H2/H3).  
- Nutze Tabellen für Vergleiche (Strategien, Reifegrade, Metriken).  
- Baue mind. 3 „Praxisbeispiele“ ein (z. B. Circuit Breaker, Slippage-Modell, Monitoring-Dashboard).  
- Wo sinnvoll: kurze Pseudocode-Blöcke (kein vollständiger produktiver Code, sondern erklärend).  
- Schreibe so, dass es in GitHub als README/Whitepaper funktioniert.

**Qualitätskontrolle (am Ende ausgeben)**
- Abschnitt „Annahmen“ (falls nötig)  
- Abschnitt „Risiko- und Compliance-Hinweise“ (kompakt)  
- Abschnitt „Self-Check“: 10 Prüfpunkte, ob der Leitfaden vollständig/robust ist  

---

### C) Output
Liefere den kompletten Leitfaden in `{{OUTPUT_FORMAT}}` als PDF, sofort druck-/publizierfähig.