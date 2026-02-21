## Variablen (User-Input Platzhalter)
> Fülle die Variablen aus (kurz & konkret). Alles, was fehlt: setze `TBD`.

- {{AGENCY_NAME}} = "Beispiel: NovaGrowth Marketing GmbH"
- {{REGION}} = "Beispiel: DACH"
- {{TIMEZONE}} = "Beispiel: Europe/Berlin"
- {{LANGUAGE_TONE}} = "Beispiel: businesslike, klar, ohne Fluff"
- {{CLIENT_TYPES}} = "Beispiel: KMU, Enterprise, Retainer-Kunden"
- {{SUPPORT_SCOPE}} = "Beispiel: Kampagnenbetrieb, Tracking/Analytics, AdOps, Web/LP, CRM/Automation"
- {{SUPPORT_CHANNELS}} = "Beispiel: Ticket (Jira/Zendesk), E-Mail, Slack/Teams, Telefon, Buchungslink"
- {{TOOLS_STACK}} = "Beispiel: Google Workspace, Slack, Jira Service Management, HubSpot, Meta/Google Ads, GA4/GTM"
- {{SERVICE_CATALOG}} = "
  Beispiel:
  - Incident: Tracking-Ausfall, Ads-Account gesperrt, Website down
  - Request: neues UTM-Schema, Conversion-Event anlegen, KPI-Report-Anpassung
  - Beratung: 30/60-min Ops-Check, Launch Readiness Review
"
- {{PRIORITY_LEVELS}} = "Beispiel: P1 kritisch, P2 hoch, P3 normal, P4 niedrig"
- {{BUSINESS_HOURS}} = "Beispiel: Mo–Fr 09:00–18:00"
- {{ONCALL_MODEL}} = "Beispiel: keine 24/7, aber Launch-Wochen On-Call 18:00–22:00"
- {{HOLIDAYS_RULE}} = "Beispiel: DE-Feiertage + Betriebsferien (Kalenderlink/Zeitraum)"
- {{CAPACITY_CONSTRAINTS}} = "
  Beispiel:
  - Max 6 Support-Termine/Tag
  - Max 2 P1-Slots/Tag (reserviert)
  - 20% Puffer für ungeplante Incidents
"
- {{BOOKING_POLICY}} = "
  Beispiel:
  - Mindestvorlauf: 4 Stunden
  - Max. Vorausbuchung: 14 Tage
  - Storno bis 2 Stunden vorher, sonst No-Show-Regel
  - Standard-Dauer: 30 min (Request), 60 min (Beratung), 15 min (P1-Triage)
"
- {{BLACKOUTS_AND_PEAKS}} = "
  Beispiel:
  - Blackout: Monatsabschluss Reporting (1.–3. Werktag) nur P1/P2
  - Peak: Kampagnen-Launch-Fenster Di–Do 10:00–16:00 reserviert
"
- {{SLA_TARGETS}} = "
  Beispiel:
  - P1: Reaktion 15 min, Workaround 2h
  - P2: Reaktion 2h, Lösung 1 AT
  - P3: Reaktion 1 AT, Lösung 3 AT
"
- {{APPROVAL_GATES}} = "Beispiel: Changes an Tracking/Ads nur mit 4-Augen-Prinzip + Change-Ticket"
- {{ESCALATION_PATH}} = "
  Beispiel:
  - L1 Ops Desk → L2 Specialist (AdOps/Tracking/Web) → Tech Lead → Account Director
"
- {{COMPLIANCE_NOTES}} = "Beispiel: DSGVO, keine sensiblen Kundendaten in Termintiteln, Logging minimiert"
- {{OUTPUT_FORMAT_PREF}} = "Beispiel: Policy + Tabellen + YAML/JSON-Konfig + Umsetzungsschritte"

---

## Prompt (zum Kopieren & Ausführen)

Du bist **Service Operations Architect** für eine **Marketing-Agentur** und erstellst ein belastbares Regelwerk für **Terminbeschränkungen / Buchungsregeln** zur **Betriebsunterstützung** (Operations Support). Ziel ist: maximale Planbarkeit, SLA-Einhaltung, klare Priorisierung, minimale Kontextwechsel.

### Kontext
- Agentur: {{AGENCY_NAME}} | Region: {{REGION}} | Zeitzone: {{TIMEZONE}}
- Support-Umfang: {{SUPPORT_SCOPE}}
- Support-Kanäle: {{SUPPORT_CHANNELS}}
- Tool-Stack: {{TOOLS_STACK}}
- Kundenarten: {{CLIENT_TYPES}}
- Service-Katalog: {{SERVICE_CATALOG}}
- Prioritäten: {{PRIORITY_LEVELS}}
- Geschäftszeiten: {{BUSINESS_HOURS}} | On-Call: {{ONCALL_MODEL}}
- Feiertage/Betriebsferien: {{HOLIDAYS_RULE}}
- Kapazitätsgrenzen: {{CAPACITY_CONSTRAINTS}}
- Buchungsrichtlinien: {{BOOKING_POLICY}}
- Blackouts/Peaks: {{BLACKOUTS_AND_PEAKS}}
- SLA-Ziele: {{SLA_TARGETS}}
- Approval Gates: {{APPROVAL_GATES}}
- Eskalation: {{ESCALATION_PATH}}
- Compliance: {{COMPLIANCE_NOTES}}
- Ausgabepräferenz: {{OUTPUT_FORMAT_PREF}}
- Tonalität: {{LANGUAGE_TONE}}

### Arbeitsauftrag
1) **Service-Typen konsolidieren**
   - Normalisiere {{SERVICE_CATALOG}} in 4–8 klaren **Termin-/Ticket-Kategorien** (z. B. P1-Triage, Incident Deep-Dive, Standard Request, Beratung, Change-Fenster).
   - Weise je Kategorie zu: Standarddauer, benötigte Rolle (L1/L2/Lead), Vorbedingungen (Ticket/Briefing), erlaubte Kanäle.

2) **Terminbeschränkungen definieren (hart vs. weich)**
   - Erstelle verbindliche Regeln für:
     - **Buchungsfenster** (Mindestvorlauf, maximale Vorausbuchung)
     - **Verfügbarkeitsfenster** (Geschäftszeiten, On-Call, Sonderzeiten)
     - **Puffer/Buffer** (vor/nach Terminen, Fokuszeiten, Kontextwechsel-Reduktion)
     - **Kapazität** (max Termine/Tag, reservierte Slots pro Priorität)
     - **Blackouts/Change-Freeze** (Reporting-Zyklen, Launch-Fenster, Feiertage)
     - **Storno/No-Show** + **Rebooking-Regeln**
     - **Zugriffsregeln** (wer darf was buchen: Kunde/AM/Intern)
     - **Datenhygiene** (Betreff/Notizen ohne sensible Daten)

3) **SLA- und Eskalationslogik in Buchungsregeln übersetzen**
   - Leite aus {{SLA_TARGETS}} konkrete **Triage-Regeln** ab:
     - Wann wird ein Termin angeboten vs. wann Ticket-only?
     - Welche Priorität bekommt **fix reservierte Slots**?
     - Welche Fälle gehen **direkt in On-Call**?
   - Baue {{ESCALATION_PATH}} als operatives Runbook ein (kurz, eindeutig).

4) **Output erstellen (präzise, implementierbar, auditierbar)**
   - Liefere die Ergebnisse in folgendem Format (alles in Word Dokument):
     A) **Executive Summary** (max. 10 Zeilen)
     B) **Constraint-Matrix** (Tabelle: Kategorie | Dauer | Buchungsfenster | Verfügbarkeit | Buffer | Kapazität | Vorbedingungen | Owner)
     C) **Kalender-/Scheduler-Regeln** als **maschinenlesbare Konfiguration**:
        - 1× YAML (generisch) + optional JSON-Variante
        - Felder: appointment_types, availability, buffers, lead_time, max_future_booking, capacity, blackout_periods, priority_reservations, cancellation_policy, data_rules
     D) **Implementierungsleitfaden** (Schritte für z. B. Microsoft Bookings / Calendly / Google Appointment Schedules – tool-neutral formuliert)
     E) **Risiko- & Edge-Case-Check** (mind. 12 Checks, z. B. Feiertage, Zeitzonen, Doppelbuchungen, Launch-Überbuchung, P1-Kollision)
     F) **KPIs & Monitoring** (z. B. SLA-Compliance, Auslastung, No-Show-Rate, Mean Time To Triage)

### Qualitäts-Gates (Pflicht)
- Keine Widersprüche zwischen Business Hours, On-Call und Blackouts.
- Jede Kategorie hat **klare Zugangsvoraussetzungen** (Ticket/Briefing/Owner).
- Reservierte Slots für P1/P2 sind realistisch im Verhältnis zu {{CAPACITY_CONSTRAINTS}}.
- Regeln sind **kurz operationalisierbar** (keine Floskeln, konkrete Zeiten/Schwellen).
- Datenschutz: keine sensiblen Daten in Termintiteln; Logging-Minimum.

### Output-Regeln
- Gib **nur** das finale Ergebnis aus (keine Gedankengänge, keine Zwischenfragen).
- Wenn Informationen fehlen, setze sinnvolle Defaults und markiere sie als **TBD**.
- Sprache: Deutsch. Ton: {{LANGUAGE_TONE}}.
