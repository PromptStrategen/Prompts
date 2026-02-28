> **Ziel dieses Prompts:** Du erzeugst einen **qualitativ maximal hochwertigen, detaillierten und praxisnahen Leitfaden** zur Erstellung/Strukturierung einer **Ausschreibung der öffentlichen Hand** – inklusive **Prozess, Rollen, Mustergliederung, Qualitätskriterien, Bewertungslogik, Checklisten** und **Textbausteinen**.  
> **Rolle/Absender:** Eine **Marketing-/Digitalagentur** (B2B) erstellt den Leitfaden für interne Nutzung oder zur Beratung eines öffentlichen Auftraggebers/Projektträgers.

---

## 1) Copy-&-Paste Prompt

```text
DU BIST:
Ein interdisziplinäres Expertenteam aus
(1) Vergabe-/Beschaffungs-Spezialist (öffentliche Hand, DE/EU, praxisorientiert),
(2) Projektmanager (Public Sector),
(3) Leistungsbeschreiber (Service Design),
(4) Juristisch vorsichtiger Redakteur (keine Rechtsberatung, aber compliance-sensibel),
(5) Qualitätsmanager (auditierbare Dokumentation),
(6) Marketing-/Kommunikationsstratege (klare Sprache, verständliche Struktur).

AUFGABE:
Erstelle einen umfassenden Leitfaden für die Erstellung einer Ausschreibung der öffentlichen Hand (Deutschland/EU-Kontext),
basierend auf den untenstehenden Variablen. Der Leitfaden soll den gesamten Lebenszyklus abdecken:
Bedarfsermittlung → Leistungsbeschreibung → Eignungs- und Zuschlagskriterien → Vertragsrahmen → Vergabeverfahren →
Bewertung/Scoring → Bieterkommunikation → Dokumentation/Revision → Risiken/Compliance.

KONTEXT:
Du arbeitest im Setup einer Marketing-/Digitalagentur, die (a) selbst als Bieter auftreten kann und (b) öffentliche Auftraggeber
bei der Ausschreibungsqualität unterstützt. Der Leitfaden muss deshalb:
- fachlich korrekt, praxisnah, auditierbar und operativ umsetzbar sein,
- typische Fehlerquellen der Praxis vermeiden (Unklarheit, fehlende Messkriterien, unrealistische SLAs, Medienbrüche),
- klare Qualitäts-Gates enthalten (Definition-of-Ready, Definition-of-Done),
- mit neutraler, vergabefester Sprache arbeiten (sachlich, nicht werblich),
- Variablen/Platzhalter sauber nutzen und in Mustern zeigen.

WICHTIGE RANDPARAMETER:
- Sprache: Deutsch (formal-sachlich, Behörden-/Vergabe-Tonalität)
- Struktur: Überschriften + Checklisten + Tabellen + Textbausteine + Beispiele
- Ergebnis muss ohne externe Verweise verständlich sein.
- Rechtlicher Hinweis: Keine Rechtsberatung. Wenn rechtliche Anforderungen berührt werden, als "Prüfpunkte" formulieren.
- Fokus: Digitale Leistungen / Marketing / Web / Software-nahe Dienstleistungen, aber übertragbar.

VARIABLEN (USERINPUT) – BITTE VERWENDEN:
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Konzeption, Umsetzung, Betrieb)"
{{CLIENT_TYPE}} = "Öffentlicher Auftraggeber / Behörde / kommunaler Träger"
{{REGION}} = "Deutschland"
{{PROCUREMENT_SCOPE}} = "Marketing- & Digitalleistungen (z.B. Website-Relaunch, Kampagnen, SEO/SEA, Content, Tracking/Analytics)"
{{PROJECT_NAME}} = "Digitale Sichtbarkeit & Serviceportal 2026"
{{PROJECT_BACKGROUND}} = "Modernisierung der digitalen Kommunikation und Serviceprozesse"
{{OBJECTIVES}} = ["Barrierearme Kommunikation", "Messbare Reichweite/Conversion", "Sichere & DSGVO-konforme Datenflüsse", "Betrieb/Support"]
{{TARGET_GROUPS}} = ["Bürger:innen", "Unternehmen", "interne Fachbereiche"]
{{CURRENT_STATE}} = "Bestehende Webpräsenz veraltet, fragmentierte Inhalte, uneinheitliches Tracking"
{{DESIRED_STATE}} = "Zentraler Auftritt, konsistente Inhalte, saubere Messbarkeit, wartbarer Betrieb"
{{BUDGET_RANGE_EUR}} = "150.000–300.000"
{{DURATION_MONTHS}} = 12
{{TIMEPLAN_MILESTONES}} = ["Kickoff", "Konzept", "Design", "Umsetzung", "Go-Live", "Betrieb"]
{{PROCUREMENT_PROCEDURE_HINT}} = "offen / nicht-offen / Verhandlungsverfahren (falls bereits präferiert)"
{{EVALUATION_FOCUS}} = ["Qualität der Methodik", "Team & Referenzen", "Barrierefreiheit", "Sicherheit/Datenschutz", "Wirtschaftlichkeit"]
{{MANDATORY_REQUIREMENTS}} = ["Barrierefreiheit nach geltenden Vorgaben", "DSGVO-Konzept", "Sicherheitskonzept", "Dokumentation", "Wartung/Support"]
{{NICE_TO_HAVE_REQUIREMENTS}} = ["Open-Source bevorzugt", "On-Prem/DE-Hosting optional", "Schulungen", "Redaktionsworkflows"]
{{CONSTRAINTS}} = ["Haushaltsjahr", "Interne Freigabezyklen", "Stakeholdervielfalt", "Legacy-Systeme"]
{{RISK_TOLERANCE}} = "niedrig"
{{SERVICE_LEVELS}} = {"Reaktionszeit":"<4h (kritisch)", "Entstörung":"<24h", "Verfügbarkeit":"99,5%"}
{{DELIVERABLES}} = ["Leistungsbeschreibung", "Bewertungsmatrix", "Vertrags-/SLA-Anhang", "Abnahmeprotokolle", "Bieterfragen-Template"]
{{COMPLIANCE_TOPICS}} = ["Datenschutz", "IT-Sicherheit", "Barrierefreiheit", "Dokumentationspflichten", "Nachvollziehbarkeit Bewertung"]
{{SCORING_MODEL_HINT}} = "100 Punkte gesamt, Preis/Leistung ausgewogen"
{{STAKEHOLDERS}} = ["Vergabestelle", "Fachbereich", "IT", "Datenschutz", "PR/Kommunikation"]
{{ASSUMPTIONS}} = ["Interne Projektleitung vorhanden", "Gremienfreigaben quartalsweise"]
{{EXCLUSIONS}} = ["Keine Hardwarebeschaffung", "Kein vollständiger Systemwechsel der Backend-Fachverfahren"]
{{OUTPUT_FORMAT}} = "Leitfaden + Mustergliederung + Checklisten + Tabellen + Textbausteine"

AUSGABE – LIEFERFORMAT (BITTE GENAU EINHALTEN):
1) Executive Summary (max. 12 Zeilen)
2) Kontext & Zielbild (IST/SOLL, Scope, Nicht-Ziele)
3) Rollen & Governance (RACI + Entscheidungswege)
4) Schritt-für-Schritt Prozess (von Bedarf bis Zuschlag, mit Artefakten)
5) Mustergliederung Ausschreibungsunterlagen (Kapitelstruktur mit Zweck je Kapitel)
6) Leistungsbeschreibung – Blaupause (inkl. Akzeptanzkriterien, DoR/DoD, Abnahme)
7) Eignungskriterien vs. Zuschlagskriterien (klar getrennt, Beispiele)
8) Bewertungsmatrix / Scoring (Tabelle: Kriterium, Gewicht, Nachweis, Bewertungsstufen 0–5, typische Fehler)
9) Preisblatt-Logik & Wirtschaftlichkeit (wie Vergleichbarkeit hergestellt wird)
10) Vertrags-/SLA-Anhang – Musterpunkte (Service Levels, Change, Doku, Security, Datenschutz, Eskalation)
11) Bieterkommunikation & Q&A (Prozess, Template, Umgang mit Bieterfragen)
12) Qualitäts- und Compliance-Gates (Checklisten pro Phase, Audit-Trail)
13) Risikoregister (Top 10 Risiken + Gegenmaßnahmen + Owner)
14) Textbausteine (neutral formuliert, copy-ready): Leistungsgegenstand, Umfang, Nachweise, Abnahme, Datenschutz, Sicherheit
15) Mini-Beispiel: 1 ausgefülltes Kapitel (z.B. "Leistungsgegenstand" oder "Zuschlagskriterien") anhand der Variablen
16) Abschluss: "Next Steps" für {{CLIENT_TYPE}} und {{AGENCY_NAME}}

QUALITÄTSANFORDERUNGEN:
- Alle Anforderungen müssen testbar sein (messbar oder prüfbar).
- Keine schwammigen Formulierungen ohne Kriterien ("intuitiv", "modern", "state of the art") – ersetze durch prüfbare Merkmale.
- Trenne MUSS/KANN sauber.
- Keine Diskriminierung/Verengung: Formulierungen vergabefest/neutral (keine Markenbindung).
- Explizite Nachweise/Artefakte je Kriterium.
- Schreibe so, dass eine Vergabestelle die Bewertung dokumentationssicher begründen kann.

ZUSATZ-PRÜFUNG (SELF-CHECK):
Am Ende: Kurzer "Vergabefestigkeits-Check" mit 10 Punkten: Widersprüche, Unklarheiten, Messbarkeit, Nachweisbarkeit,
Vergleichbarkeit, Zeit/SLAs, Datenschutz, Sicherheit, Barrierefreiheit, Dokumentationspflichten.

BEGINNE JETZT.
```

---

## 2) Anwendungshinweise (kurz, operativ)

- **Variablenblock zuerst ausfüllen**, danach Prompt 1:1 an dein LLM geben.  
- Wenn du **nur ein Artefakt** brauchst (z. B. Bewertungsmatrix), setze `{{OUTPUT_FORMAT}}` entsprechend (z. B. `"nur Bewertungsmatrix + Scoring"`).  
- Für **Vergabeverfahren**: Wenn `{{PROCUREMENT_PROCEDURE_HINT}}` leer ist, soll das Modell **Optionen neutral** darstellen und **Prüfpunkte** statt Festlegungen liefern.

---

## 3) Beispiel-Variablen (für schnelle Tests)

```text
{{PROJECT_NAME}} = "Website-Relaunch & Bürgerportal"
{{BUDGET_RANGE_EUR}} = "80.000–120.000"
{{DURATION_MONTHS}} = 6
{{EVALUATION_FOCUS}} = ["Barrierefreiheit", "Methodik", "Betrieb/Support", "Wirtschaftlichkeit"]
{{SCORING_MODEL_HINT}} = "100 Punkte; Preis 30 / Qualität 70"
```

---

## 4) Output-Qualitätskriterien (Abnahmeliste)

- Enthält **RACI**, **Bewertungsmatrix**, **Textbausteine**, **Risikoregister**, **Gate-Checklisten**
- Jede MUSS-Anforderung ist **prüfbar** (Nachweis + Messkriterium)
- Bewertungslogik ist **vergleichbar** (0–5 Stufen mit klaren Beschreibungen)
- Sprache ist **neutral** und **nicht anbieterspezifisch**
- Enthält **Self-Check** zur Konsistenz und Dokumentationsfähigkeit
