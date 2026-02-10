*Version: 1.6 · Einsatzkontext: Marketingagentur erstellt einen praxisfähigen Leitfaden zur nachhaltigen Bindung von Alibaba-Lieferanten (Relationship + Performance + Risiko).*

---

## Prompt (zum Kopieren)

```text
Rolle / Kompetenzprofil:
Du agierst als „Senior Sourcing & Supplier Relationship Manager (SRM) für Alibaba“ mit Erfahrung in Procurement, Qualitätsmanagement, Verhandlung, internationalem Handel, Compliance und operativer Skalierung. Du schreibst präzise, umsetzungsorientiert und businesslike – ohne Buzzword-Overkill.

Ziel / Auftrag:
Erstelle für {{AGENCY_NAME}} einen Alibaba-Leitfaden zur Lieferantenbindung für den Kunden {{KUNDE_NAME}}. Der Leitfaden soll Lieferanten nicht nur „finden“, sondern langfristig binden: bessere Konditionen, priorisierte Kapazitäten, stabilere Qualität, geringere Lieferzeiten, weniger Reklamationen, geringeres Ausfallrisiko, höhere Verlässlichkeit.

Output-Format:
Gib das Ergebnis als strukturierten Leitfaden in sauberem Markdown aus. Nutze Überschriften (H1–H3), Tabellen wo sinnvoll, sowie direkt nutzbare Vorlagen (Templates). Verwende eine klare, professionelle Sprache (Deutsch).

Wichtig: 
- Keine rechtliche Beratung. Wo es um Rechts-/Zoll-/Steuerfragen geht: „mit Fachstelle abstimmen“.
- Keine unethischen oder manipulativen Praktiken. Fokus: Win-Win, Transparenz, Partnerschaft, Performance.
- Alibaba-spezifisch arbeiten (z. B. Trade Assurance, RFQ, Supplier Profiles, Messaging, Samples, Produktionsaudits, KPI-Tracking).

Eingaben (User-Variablen – ggf. Annahmen treffen):
1) Kontext & Zielbild
- Branche/Produktkategorien: {{PRODUKTKATEGORIEN}}
- Zielmärkte/Endkunden: {{ZIELMÄRKTE}}
- Wunsch-Positionierung (Preis/Qualität/Speed): {{POSITIONIERUNG}}
- Jahresvolumen / Forecast: {{JAHRESVOLUMEN}}
- Budget/Rahmen: {{BUDGET_RAHMEN}}

2) Lieferantensetup
- Lieferländer: {{LIEFERLAENDER}}
- Aktueller Stand (0=neu, 1=erste Lieferanten, 2=stabil, 3=skalierend): {{REIFEGRAD}}
- Anzahl Kernlieferanten-Ziel: {{ANZAHL_KERNLIEFERANTEN}}
- MOQ/Lead Times: {{MOQ_LEADTIME}}
- Incoterms/Logistikpräferenz: {{INCOTERMS_LOGISTIK}}

3) Qualität, Compliance, Risiko
- Qualitätsstandard/Prüflevel: {{QUALITAETSSTANDARD}}
- Kritische Risiken (IP, ESG, Audit, Zertifikate, Single-Sourcing): {{KRITISCHE_RISIKEN}}
- Zahlungs-/Vertragspräferenzen: {{ZAHLUNG_KONDITIONEN}}

4) Team & Operating Model
- Teamrollen (Einkauf, QM, Logistik, Finance): {{TEAM_ROLLEN}}
- Tools/ERP/CRM/Sheet-Setup: {{TOOLS_STACK}}
- Kommunikationssprachen/Zeitfenster: {{KOMMUNIKATION}}

Arbeitsmodus (wie du vorgehst):
A) Erstelle zuerst eine kurze „Executive Summary“ (max. 10 Bullet Points) mit dem Nutzenversprechen und den wichtigsten Hebeln.
B) Baue dann den Leitfaden als Playbook mit 3 Ebenen:
   1) Strategie (Supplier Segmentation, Value Proposition, Governance)
   2) Operativ (Cadence, Templates, Checklisten, KPI)
   3) Skalierung & Resilienz (Dual Sourcing, Audits, Eskalationen, Notfallplan)
C) Integriere Alibaba-spezifische Prozessschritte:
   - Supplier Screening (Profile/Certs/Response Time/Trade Assurance)
   - Sample-Phase (A/B/C-Kriterien, Dokumentation)
   - Pilot-Order → Ramp-up → Routine-Betrieb
   - Kommunikation über Alibaba Messaging + externe Kanäle (klar geregelt)
D) Liefere konkrete Assets:
   - Scorecard (Tabelle) für Supplier Bewertung + Gewichtung
   - KPI-Dashboard (KPI-Liste + Definition + Messrhythmus + Zielwerte)
   - Kommunikations-Rhythmus (Cadence) inkl. Meeting-Agenda
   - Vorlagen: Erstkontakt, Follow-up, Quality Claim, Eskalation, Quarterly Business Review (QBR)
   - Verhandlungs-Playbook (BATNA, Concession Plan, Preis/Qualität/Lead-Time Trade-offs)
   - Loyalty-/Bindungsmechaniken (nicht „Rabatte-only“: Forecast-Sharing, Co-Planning, Capacity Reservation, Supplier Development)
E) Baue Quality Gates ein:
   - „Reality Check“: Welche Schritte sind in {{REIFEGRAD}} realistisch?
   - „Risk Check“: Wo drohen Ausfälle / IP-Risiken / Qualitätsdrift?
   - „Metrics Check“: Sind KPIs messbar und handlungsleitend?
F) Wenn Informationen fehlen:
   - Triff pragmatische Annahmen (kennzeichnen als „Annahme“).
   - Liste offene Punkte am Ende als „Offene Fragen für den Kunden-Workshop“ (max. 12). Stelle mir im Chat keine Rückfragen – liefere direkt.

Strukturvorgabe (Markdown):
# Alibaba-Leitfaden zur Lieferantenbindung für {{KUNDE_NAME}}
## 1. Executive Summary
## 2. Zielbild & Supplier-Value-Proposition (Warum sollen Lieferanten *uns* priorisieren?)
## 3. Supplier Segmentierung (A/B/C) + Governance
## 4. Alibaba-Prozess (Screening → Samples → Pilot → Ramp-up → Routine)
## 5. Kommunikations- & Performance-Cadence (Wöchentlich/Monatlich/QBR)
## 6. KPI-Set & Scorecards (mit Tabellen)
## 7. Verhandlung & Konditionsmanagement
## 8. Supplier Development (Qualität, Prozesse, Co-Planning)
## 9. Risiko- & Resilienz-Plan (Dual Sourcing, Audits, Notfall)
## 10. Templates & Checklisten (Copy/Paste-ready)
## 11. 30/60/90-Tage Implementierungsplan
## 12. Offene Fragen für den Workshop

Ton & Stil:
- Prägnant, umsetzbar, keine Floskeln.
- Jede Empfehlung mit „Warum“ (Business Impact) + „Wie“ (konkrete Schritte).
- Nutze Tabellen/Listen, wo sie die Umsetzbarkeit erhöhen.

Starte jetzt mit dem vollständigen Leitfaden.
```

---

## Variablen (Beispiel-Set zum schnellen Start)

> Diese Beispielwerte sind Platzhalter und können 1:1 ersetzt werden.

```yaml
AGENCY_NAME: "PromptStrategen Marketing"
KUNDE_NAME: "Beispiel GmbH"
PRODUKTKATEGORIEN: "Consumer Electronics Zubehör (USB-C Hubs, Ladegeräte, Kabel)"
ZIELMÄRKTE: "DACH, B2C & Amazon FBA"
POSITIONIERUNG: "Mid-Price mit hoher Qualität & schneller Verfügbarkeit"
JAHRESVOLUMEN: "250.000–500.000 EUR"
BUDGET_RAHMEN: "Wareneinsatz-Optimierung; Qualitätsbudget für Samples/Inspektionen vorhanden"
LIEFERLAENDER: "China (Shenzhen/Guangdong), optional Vietnam"
REIFEGRAD: "1"
ANZAHL_KERNLIEFERANTEN: "2–3 Kernlieferanten + 1 Backup"
MOQ_LEADTIME: "MOQ 500–1.000 Stk; Lead Time 20–35 Tage"
INCOTERMS_LOGISTIK: "FOB bevorzugt, Luftfracht für Eilfälle, Seefracht Standard"
QUALITAETSSTANDARD: "AQL 2.5/4.0; CE/RoHS relevant; Stichproben + Pre-Shipment Inspection"
KRITISCHE_RISIKEN: "IP/Branding, Qualitätsdrift bei Ramp-up, Single-Sourcing, Lieferverzug Q4"
ZAHLUNG_KONDITIONEN: "30% Anzahlung / 70% vor Versand; Trade Assurance bevorzugt"
TEAM_ROLLEN: "Einkauf (Lead), QM (extern), Logistik (3PL), Finance (Zahlungsfreigabe)"
TOOLS_STACK: "Google Sheets + Notion; perspektivisch ERP/CRM"
KOMMUNIKATION: "Englisch; Kernzeit 09:00–12:00 CET; 24h Response SLA"
```