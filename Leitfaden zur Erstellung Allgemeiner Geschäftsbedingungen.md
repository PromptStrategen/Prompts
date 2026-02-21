> **Hinweis (Compliance):** Dieses Prompt-Template unterstützt bei der **Strukturierung und Formulierung eines AGB-Leitfadens**. Es ersetzt **keine Rechtsberatung** und **keinen Anwalt/keine Anwältin**. Für den produktiven Einsatz: **juristische Prüfung (Legal Review) zwingend**.

---

## 1) Copy-&-Paste Prompt (für LLM)

### Rolle & Zielbild
Du agierst als **Senior Legal Operations / Contract Engineer** mit Spezialisierung auf **DACH (Deutschland)**, **B2B-Services**, **digitale Dienstleistungen**, **IT/Marketing-Agenturen** und **DSGVO-konforme Prozesse**.  
Dein Auftrag: Erstelle einen **umsetzungsfertigen Leitfaden** zur Erstellung von **Allgemeinen Geschäftsbedingungen (AGB)** für eine Marketing-/Digitalagentur. Der Leitfaden ist **praxisnah**, **risikoorientiert**, **verständlich** und **modular**, sodass daraus AGB-Textbausteine abgeleitet werden können.

### Output-Standard (Qualitätskriterien)
- **Detailtiefe hoch:** klare Kapitelstruktur, Entscheidungspfade, Beispiele, Formulierungsvarianten (B2B/B2C), typische Fallstricke.
- **Aktueller Standard:** DSGVO, Auftragsverarbeitung (AVV), ePrivacy-relevante Touchpoints, digitale Leistungsmodelle (SaaS, Retainer, Projekt).
- **Juristische Genauigkeit (best effort):** keine erfundenen Urteile/Paragraphen, keine falschen Behauptungen. Wenn unsicher: **kennzeichnen**.
- **Umsetzbarkeit:** Checklisten, "Must-have"-Klauseln, Optionsklauseln, Eingabefragen, Review-Workflow.
- **Format:** Word Dokument, sauberer Aufbau, copy-ready.

### Kontext (Userinput als Variablen)
Nutze folgende Variablen als Input. Wenn Informationen fehlen, **erstelle zuerst eine kompakte Rückfragenliste** (max. 12 Fragen) und arbeite danach mit **Annahmen**, die du transparent markierst.

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{LEGAL_FORM}} = "UG | GmbH | AG | Kleinunternehmer | GbR"
{{COUNTRY}} = "Deutschland"
{{TARGET_MARKET}} = "DACH"
{{BUSINESS_MODEL}} = "B2B Dienstleistungen (Projekt + Retainer)"
{{INDUSTRIES_SERVED}} = "KMU (50–500 MA), IT-nahe Teams, Ops/Support"
{{CORE_SERVICES}} = "Marketingberatung, Webentwicklung, Automatisierung, KI-Workflows, Support/Managed Services"
{{DELIVERY_MODE}} = "Remote / Hybrid"
{{CONTRACTING_STYLE}} = "Angebot + Leistungsbeschreibung (SOW) + AGB"
{{PRICING_MODELS}} = "Festpreis, Zeit & Material, Retainer, Paketpreise"
{{PAYMENT_TERMS_DEFAULT}} = "14 Tage netto"
{{ACCEPTANCE_PROCESS}} = "Abnahme je Meilenstein + schriftliches Protokoll"
{{CHANGE_REQUESTS}} = "Change-Request-Prozess mit Aufwandsschätzung"
{{THIRD_PARTY_TOOLS}} = "n8n, Zapier, Google Workspace, Microsoft 365, AWS/Azure, OpenAI/LLM APIs"
{{IP_POLICY}} = "Nutzungsrechte nach Zahlung, Quellcode-Übergabe optional"
{{WARRANTY_POLICY}} = "B2B Gewährleistung minimiert, klare Mängelrügefristen"
{{LIABILITY_RISK_APPETITE}} = "konservativ (Haftungsbegrenzung, typische Ausschlüsse)"
{{DATA_PROCESSING}} = "DSGVO-konform, AVV bei Bedarf"
{{SUBPROCESSORS}} = "Cloud-/SaaS-Anbieter, Liste pflegbar"
{{SECURITY_MEASURES}} = "TOMs, Zugriffskontrollen, Protokollierung, Least Privilege"
{{MARKETING_CONSENT}} = "Newsletter nur mit Einwilligung, Double-Opt-In"
{{B2C_OPTION}} = "nein"
{{SPECIAL_REGULATIONS}} = "keine"
{{GOVERNING_LAW_PREF}} = "deutsches Recht"
{{JURISDICTION_PREF}} = "Sitz der Agentur (B2B)"
{{DOCUMENT_LANGUAGE}} = "Deutsch"
{{TONE}} = "klar, professionell, ohne Buzzword-Overkill"
```

### Lieferumfang (was du erzeugen sollst)
Erstelle einen **Leitfaden** mit den folgenden Artefakten:

1. **AGB-Blueprint (Kapitelstruktur)**  
   - Kapitelüberschriften + Zweck + Risiko/Benefit + typische Varianten.
2. **Klausel-Bibliothek (Textbausteine)**  
   - je Klausel: Ziel, empfohlene Formulierung, Alternativen (konservativ / ausgewogen / kundenfreundlich), No-Go’s.
3. **Entscheidungsmatrix**  
   - wann welche Option (B2B vs. B2C, Projekt vs. Retainer, SaaS/Tools, IP-Übergabe, Abnahme, Haftung).
4. **Checklisten**  
   - Pre-Contract, Vertragsanlage/SOW, Onboarding, Projektabnahme, Offboarding.
5. **DSGVO-/Datenschutz-Integration**  
   - Schnittstellen AGB ↔ Datenschutzerklärung ↔ AVV ↔ TOMs; klare Verantwortlichkeiten.
6. **Risiko-Register**  
   - Top-Risiken (Scope Creep, Zahlungsverzug, IP-Streit, Third-Party-Ausfälle, Datenschutz), Gegenmaßnahmen.
7. **Review- & Freigabeprozess**  
   - Legal Review, Versionierung, Änderungslog, Rollout an Website/Angebote.

### Inhaltliche Mindestklauseln (Coverage)
Der Leitfaden muss mindestens diese Themen abdecken (mit Beispieltexten):
- Geltungsbereich, Begriffsdefinitionen, Vertragsgegenstand
- Vertragsschluss, Angebot/Annahme, Textformklauseln
- Leistungsumfang, Mitwirkungspflichten Kunde, Eskalation
- Abnahme, Teilabnahmen, Mängelrüge, Nachbesserung
- Vergütung, Nebenkosten, Reisekosten, Abrechnung, Zahlungsverzug, Zurückbehaltungsrechte
- Change Requests, Scope-Management, Priorisierung
- Nutzungsrechte/IP, Open-Source/Third-Party, Referenznennung
- Vertraulichkeit/NDA-Logik (AGB-kompatibel)
- Haftung, Haftungsbegrenzung (B2B), typische Ausschlüsse, Force Majeure
- Gewährleistung/Verjährung (B2B), Support/SLAs (falls relevant)
- Laufzeit, Kündigung, außerordentliche Kündigung, Retainer-Logik
- Datenschutz/AVV, Subunternehmer, Datenübermittlung Drittland (nur als Leitfadenpunkte)
- Schlussbestimmungen: Gerichtsstand, anwendbares Recht, Salvatorische Klausel (vorsichtig), Rangfolge Dokumente

### Arbeitsweise (Algorithmus)
1. **Kontext prüfen:** passt das Modell zu {{BUSINESS_MODEL}} / {{CORE_SERVICES}}? Abweichungen markieren.  
2. **Annahmen:** fehlende Werte als Annahmen notieren.  
3. **Blueprint bauen:** Kapitelstruktur + Ziel & Risiko.  
4. **Klauseln liefern:** pro Kapitel konkrete Klauseltexte + Varianten + Hinweise.  
5. **Entscheidungsmatrix:** Optionen sauber ableiten.  
6. **Checklisten + Risiko-Register:** operationalisieren.  
7. **Legal-Review-Hinweise:** wo zwingend Anwalt ran muss (rot markiert).

### Formatvorgaben
- Nutze Überschriften `#`, `##`, `###`
- Klauseln in **Codeblöcken** (```text)
- Jede Klausel erhält: **Name**, **Zweck**, **Standardtext**, **Alternativen**, **Fallstricke**
- Markiere Annahmen mit `⚠️ Annahme: ...`
- Markiere Legal-Pflichtprüfung mit `🚨 Legal Review erforderlich: ...`

### Start
Beginne mit:
1) einer **kompakten Zusammenfassung** (max. 10 Zeilen)  
2) dann direkt dem **AGB-Blueprint**  
3) anschließend **Klausel-Bibliothek**, **Matrix**, **Checklisten**, **Risiko-Register**, **Review-Prozess**.

---

## 2) Mini-Briefing für Anwalt/Legal Review (optional im Output)
Erzeuge am Ende eine Seite "**Legal Review Brief**":  
- Kontext, Zielgruppe, Risikoprofil  
- offene Punkte / Annahmen  
- Klauseln mit hohem Risiko (Haftung, IP, Datenschutz, Gerichtsstand)  
- Empfehlung zur finalen Prüfung

---

## 3) Empfehlung für den operativen Einsatz (Best Practice)
- AGB als **Basisdokument**, Details in **Leistungsbeschreibung/SOW** (Scope, Deliverables, Abnahme, SLAs).
- Für Datenschutz: AGB nur **Schnittstellen** definieren, AVV/TOMs als **Anlagen** pflegen.
- Versionierung: `AGB_v{{YYYY}}-{{MM}}-{{DD}}` + Changelog.

---

## 4) Quick-Start: Beispiel-Aufruf (Prompt-Run)
Kopiere den Prompt aus Abschnitt 1, setze deine Variablen, und ergänze:
- konkrete Leistungsarten (z. B. "Landingpages", "Tracking-Setup", "Automations")
- typische Kunden (B2B IT-Leitung, KMU)
- Haftungsappetit (konservativ/ausgewogen)
