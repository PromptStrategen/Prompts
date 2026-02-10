> **Zweck:** Dieser Prompt erzeugt einen **praxisnahen, detailtiefen Leitfaden** zur **Analyse von Datenverstößen** (Data Breach) – inklusive Rollen/RACI, Checklisten, Artefakten, Kommunikations- und PR-Plan, DSGVO/GDPR-Fristen (z. B. 72h) sowie Reporting-Struktur.  
> **Nutzung:** Variablen ausfüllen → Prompt in dein LLM kopieren → Output als internen Leitfaden verwenden (kein Rechtsrat).

---

## 1) Variablen (User-Input Platzhalter)

Kopiere den Block und fülle die Werte aus:

```yaml
{{AGENCY_NAME}}: "Beispiel: BrightPulse Marketing GmbH"
{{CLIENT_NAME}}: "Beispiel: BeispielShop24 GmbH"
{{CLIENT_INDUSTRY}}: "Beispiel: E-Commerce / Retail"
{{REGION_LAW}}: "Beispiel: EU / Deutschland (DSGVO)"
{{BREACH_SCENARIO}}: "Beispiel: Unberechtigter Zugriff auf CRM-Export (Kundendaten)"
{{DATA_TYPES}}: ["Name", "E-Mail", "Telefon", "Adresse", "Bestellhistorie"]
{{SENSITIVE_DATA}}: "Beispiel: Nein (keine Zahlungsdaten), evtl. Login-Hash: unklar"
{{BREACH_DETECTED_AT}}: "YYYY-MM-DD HH:MM (TZ)"
{{SYSTEMS_AFFECTED}}: ["CRM", "Newsletter-Tool", "Ticket-System"]
{{SUSPECTED_VECTOR}}: "Beispiel: kompromittierter Admin-Account / Phishing"
{{CURRENT_STATUS}}: "Beispiel: Zugriff blockiert, Passwort-Reset, Forensik läuft"
{{KNOWN_IMPACT}}: "Beispiel: 12.400 Datensätze potentiell betroffen"
{{STAKEHOLDERS}}: ["Geschäftsführung", "IT/Sec", "DPO/DSB", "PR", "Customer Support"]
{{AVAILABLE_TEAMS}}: ["Agentur-PR", "Inhouse-IT", "External Forensics", "Legal"]
{{TIME_CONSTRAINTS}}: "Beispiel: Erstinfo an GF in 2h; Behörden-Entscheid in 24h"
{{TONE_OF_VOICE}}: "Beispiel: transparent, souverän, nicht-defensiv"
{{OUTPUT_LANGUAGE}}: "Deutsch"
{{DEPTH_LEVEL}}: "High (Enterprise-ready)"
{{ASSUMPTIONS_ALLOWED}}: "Ja – aber alle Annahmen explizit kennzeichnen"
```

---

## 2) Der Master-Prompt (Copy/Paste)

> **Hinweis:** Der Prompt ist so gebaut, dass das Modell **zuerst saubere Annahmen & Scope** setzt, dann ein **umsetzbares Playbook** liefert und am Ende eine **Qualitätsprüfung** macht.

```text
Rolle:
Du bist ein interdisziplinäres Incident-Response- und Kommunikations-Team (Security Lead + Forensik-Koordinator + DSB/Compliance-Advisor + PR/Marketing-Lead + Customer Ops Lead). Du arbeitest für {{AGENCY_NAME}} und lieferst für den Kunden {{CLIENT_NAME}} einen Leitfaden, der operativ sofort nutzbar ist.

Kontext:
- Branche: {{CLIENT_INDUSTRY}}
- Rechtsraum/Regeln: {{REGION_LAW}}
- Vorfall-Szenario: {{BREACH_SCENARIO}}
- Betroffene Systeme: {{SYSTEMS_AFFECTED}}
- Datentypen: {{DATA_TYPES}}
- Sensible Daten: {{SENSITIVE_DATA}}
- Entdeckt am: {{BREACH_DETECTED_AT}}
- Vermuteter Angriffsvektor: {{SUSPECTED_VECTOR}}
- Aktueller Status: {{CURRENT_STATUS}}
- Bekannter Impact: {{KNOWN_IMPACT}}
- Stakeholder: {{STAKEHOLDERS}}
- Verfügbare Teams: {{AVAILABLE_TEAMS}}
- Zeitdruck: {{TIME_CONSTRAINTS}}
- Tonalität: {{TONE_OF_VOICE}}
- Sprache: {{OUTPUT_LANGUAGE}}
- Detailtiefe: {{DEPTH_LEVEL}}
- Annahmen erlaubt: {{ASSUMPTIONS_ALLOWED}}

Ziel:
Erstelle einen **umfassenden Leitfaden zur Analyse von Datenverstößen** (Data Breach Analysis Guide), der sowohl technische Analyse als auch Compliance- und Kommunikationsanforderungen abdeckt. Der Leitfaden muss für ein gemischtes Publikum (Management, IT/Sec, DSB, PR/Support) verständlich sein und zugleich fachlich präzise bleiben.

Wichtige Leitplanken:
- Kein „Hacking“, keine offensiven Anleitungen. Fokus auf **Analyse, Eindämmung, Beweissicherung, Compliance, Kommunikation**.
- Wenn Infos fehlen: triff **minimale, realistische Annahmen**, markiere sie klar unter „Annahmen“.
- Nutze Best Practices: **Chain of Custody**, Evidenz-Handling, Timeline, Root Cause, Scope, Impact, Lessons Learned.
- Beachte {{REGION_LAW}}: insbesondere **Melde-/Benachrichtigungslogik** (z. B. 72h bei DSGVO) – ohne Rechtsberatung zu behaupten. Formuliere als „Hinweis/Prüfpunkt“.
- Output muss **handlungsorientiert** sein: Checklisten, Rollen, Artefakte, Vorlagen, Metriken.

Output-Format (streng einhalten):
1) **Executive Summary (1 Seite)**
   - Was ist passiert (kurz), aktueller Stand, Top-Risiken, nächste 24h Prioritäten

2) **Scope & Annahmen**
   - Was ist bekannt vs. unklar
   - Annahmen (klar markiert)
   - Definition „Betroffen“ (Personen, Systeme, Daten)

3) **Incident-Triage & Severity**
   - Schweregrad-Matrix (Impact × Likelihood) inkl. Einstufung für dieses Szenario
   - Entscheidungspunkte (Go/No-Go) für Eskalation, externe Forensik, Legal

4) **Technischer Analyse-Playbook (End-to-End)**
   - A) Beweissicherung: Logs, Snapshots, Export, Hashing, Zugriffsrechte, Chain-of-Custody-Form
   - B) Timeline-Rekonstruktion: Ereignisse, Timezone-Normalisierung, Indikatoren
   - C) Angriffsvektor-Validierung: Phishing/Creds, API-Keys, Misconfig, Malware (nur defensiv)
   - D) Scope-Erweiterung: lateral movement Indikatoren, Datenabfluss-Indizien, ungewöhnliche Exporte
   - E) Root-Cause-Analyse (RCA): Hypothesen → Tests → Evidenz → Schlussfolgerung
   - F) Containment/Eradication: priorisierte Maßnahmenliste (kurzfristig/mittelfristig)
   - G) Recovery & Hardening: Security Header, MFA, Least Privilege, Secrets Rotation, Monitoring
   - Für jede Phase: **Ziele, Inputs, Schritte, Tools/Artefakte, Output, Owner, Dauer-Schätzung (S/M/L)**

5) **Compliance & Meldepflichten (Prüfpfad)**
   - Entscheidungsbaum: „Meldepflicht wahrscheinlich?“
   - Welche Informationen braucht der DSB/Legal zur Entscheidung?
   - Checkliste: Art. 33/34 DSGVO als **Prüfpunkte** (keine Rechtsberatung)
   - Dokumentationspflichten: Incident Register / Berichtspflichten intern

6) **Kommunikations- & PR-Plan (Agentur-Perspektive)**
   - Kommunikationsprinzipien (Transparenz, Fakten, Timing, Tone of Voice)
   - Zielgruppen & Kanäle (Kunden, Mitarbeiter, Partner, Presse, Social)
   - Freigabeprozess (Legal/DSB/Management)
   - Q&A / Holding Statements / Updates (Wording-Leitplanken)
   - Risiko: Reputationsschaden vs. Überkommunikation – klare Dos & Don’ts

7) **Customer Support Enablement**
   - Ticket-Makros / FAQ-Struktur
   - Eskalationspfad (VIP, sensible Fälle)
   - Monitoring: Volumen, Sentiment, Top-Fragen
   - SLA-Vorschlag für die ersten 7 Tage

8) **Artefakte & Templates (sofort verwendbar)**
   - Incident-Log (Tabellenstruktur)
   - Chain-of-Custody-Form
   - Stakeholder-Update (Kurzformat)
   - Presse-/Kunden-Statement (2 Varianten: kurz + ausführlich)
   - Interne All-Hands Notiz (Mitarbeiter)
   - Post-Incident Review Agenda

9) **Metriken & Reporting**
   - KPIs: MTTD, MTTR, „Time to Contain“, Ticket-Deflection, Sentiment
   - Reporting-Rhythmus (0–24h, 24–72h, Woche 1)
   - Dashboard-Skizze (welche Felder, welche Views)

10) **Qualitätscheck**
   - Liste „Häufige Lücken“ (z. B. fehlende Logs, unklare Datenklassifizierung)
   - Selbstprüfung: Konsistenz, fehlende Annahmen, nächste Schritte klar?
   - „Top 10 Next Actions“ priorisiert nach Aufwand/Impact

Stil:
- Businesslike, präzise, keine Floskeln.
- Verwende klare Überschriften, nummerierte Checklisten, Tabellen wo sinnvoll.
- Keine langen theoretischen Exkurse. Fokus auf umsetzbare Schritte.
```

---

## 3) Beispiel (ausgefüllte Variablen – Demo)

```yaml
{{AGENCY_NAME}}: "BrightPulse Marketing GmbH"
{{CLIENT_NAME}}: "BeispielShop24 GmbH"
{{CLIENT_INDUSTRY}}: "E-Commerce / Retail"
{{REGION_LAW}}: "EU / Deutschland (DSGVO)"
{{BREACH_SCENARIO}}: "Unberechtigter Zugriff auf CRM-Export (Kundendaten)"
{{DATA_TYPES}}: ["Name", "E-Mail", "Telefon", "Adresse", "Bestellhistorie"]
{{SENSITIVE_DATA}}: "Keine Zahlungsdaten; Passwort-Hashes unklar"
{{BREACH_DETECTED_AT}}: "2026-02-09 18:35 (CET)"
{{SYSTEMS_AFFECTED}}: ["CRM", "Newsletter-Tool", "Ticket-System"]
{{SUSPECTED_VECTOR}}: "kompromittierter Admin-Account (Phishing)"
{{CURRENT_STATUS}}: "Zugriff gesperrt, Passwort-Reset, Token-Rotation läuft, Forensik beauftragt"
{{KNOWN_IMPACT}}: "12.400 Datensätze potentiell betroffen"
{{STAKEHOLDERS}}: ["GF", "IT/Sec", "DSB", "PR", "Customer Support"]
{{AVAILABLE_TEAMS}}: ["Agentur-PR", "Inhouse-IT", "External Forensics", "Legal"]
{{TIME_CONSTRAINTS}}: "Erstinfo an GF in 2h; Meldeentscheidung in 24h"
{{TONE_OF_VOICE}}: "transparent, souverän, nicht-defensiv"
{{OUTPUT_LANGUAGE}}: "Deutsch"
{{DEPTH_LEVEL}}: "High (Enterprise-ready)"
{{ASSUMPTIONS_ALLOWED}}: "Ja – alle Annahmen explizit kennzeichnen"
```

---

## 4) Optionale Erweiterungen (Modular)

Diese Add-ons kannst du in den Prompt ergänzen (bei Bedarf):

- **Branchenspezifisch:** Healthcare / Finance (höhere Anforderungen, strengere Kommunikationspfade)
- **Technik-Stack:** Microsoft 365, Google Workspace, AWS/Azure – mit Log-Quellenliste
- **Threat Intel:** defensiver IOC-Check, aber ohne offensive Inhalte
- **Übung:** Tabletop-Exercise-Agenda + Scorecard

---

## 5) Governance-Hinweis

Dieser Leitfaden unterstützt operative Exzellenz, ersetzt aber keine rechtliche Beratung. Meldeentscheidungen und Wortlaut von Behörden-/Betroffenenkommunikation sind in {{REGION_LAW}} mit Legal/DSB final abzustimmen.
