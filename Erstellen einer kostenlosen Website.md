> **Zweck:** Dieser Prompt erzeugt einen **hochwertigen, detailtiefen, umsetzbaren Leitfaden** für den Aufbau einer kostenlosen Website – inklusive Plattform-Entscheidung, Schritt-für-Schritt-Implementierung, Content/SEO, Recht/DSGVO (DACH), Launch-Check, und Betrieb.

---

## 1) Variablenblock (User-Input) – **Beispielwerte**
> Kopiere den Block, passe Werte an, und füge ihn **über** den Prompt ein.

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Inhouse + Kundenprojekte)"
{{CLIENT_NAME}} = "Beispielkunde GmbH"
{{INDUSTRY}} = "IT-Services / Beratung"
{{TARGET_REGION}} = "Deutschland (DACH-ready)"
{{TARGET_AUDIENCE}} = "KMU (Entscheider + Fachabteilungen)"
{{PRIMARY_GOAL}} = "Leads generieren"
{{SECONDARY_GOALS}} = "Branding, Recruiting, Vertrauen (Case Studies)"
{{UNIQUE_VALUE_PROPOSITION}} = "Schnelle Umsetzung, messbarer ROI, Security/DSGVO-by-design"
{{BRAND_TONE}} = "professionell, klar, technisch kompetent"
{{BRAND_COLORS}} = "#AD762F, #2F37AD, #11361E"
{{CONTENT_LANGUAGES}} = "Deutsch (Optional: Englisch später)"
{{PAGES_REQUIRED}} = "Start, Leistungen, Über uns, Referenzen, Kontakt, Datenschutz, Impressum"
{{FEATURES_REQUIRED}} = "Kontaktformular, Analytics (datenschutzkonform), Newsletter (optional), FAQ"
{{LEGAL_COMPLIANCE_LEVEL}} = "hoch (DSGVO, TTDSG, Impressumspflicht)"
{{SEO_PRIORITY}} = "hoch"
{{TIME_BUDGET}} = "6-10 Stunden Setup + 4-8 Stunden Content"
{{SKILL_LEVEL}} = "Einsteiger (keine Programmierung) ODER Tech-affin (GitHub okay)"
{{PREFERRED_PLATFORMS}} = "offen"
{{MUST_BE_FREE}} = "ja (0€ laufende Kosten); Domain optional"
{{DOMAIN_AVAILABLE}} = "nein"
{{ASSETS_AVAILABLE}} = "Logo (PNG), 3 Bilder, 1 Case Study"
{{COMPETITORS}} = "3 lokale Wettbewerber; Fokus auf Vertrauen & Geschwindigkeit"
{{CTA}} = "Kostenloses Erstgespräch buchen"
{{CONTACT_CHANNEL}} = "E-Mail + Formular"
{{PRIVACY_NOTES}} = "keine Tracking-Cookies ohne Einwilligung"
```

---

## 2) Master-Prompt (Copy & Paste)

```text
Du agierst als:
1) Senior Web-Strategist (Conversion + SEO), 
2) Technical Writer (präzise, verständlich), 
3) UX/UI Consultant (klarer Aufbau), 
4) Datenschutz-/Compliance-Spezialist (DSGVO/TTDSG/Impressum DACH),
5) Projektmanager (Roadmap, Checklisten, Quality Gates).

KONTEXT:
Wir sind {{AGENCY_NAME}} ({{AGENCY_ROLE}}) und erstellen für {{CLIENT_NAME}} einen Leitfaden, wie eine kostenlose Website gebaut wird, die professionell wirkt und messbare Ziele unterstützt.

ZIEL:
Erstelle einen extrem praxisnahen, detailtiefen Leitfaden zum Erstellen einer kostenlosen Website. Der Leitfaden muss:
- 0€ laufende Kosten respektieren ({{MUST_BE_FREE}}) und transparent die Grenzen (Branding, Subdomain, Features) benennen.
- Zwei Realisierungswege liefern:
  A) No-Code/Low-Code (schnell, ohne Programmierung)
  B) Tech-affin/Static Site (GitHub Pages/Netlify o.ä., ebenfalls kostenlos)
- Eine klare Entscheidungslogik enthalten: Welche Plattform passt zu {{SKILL_LEVEL}}, {{FEATURES_REQUIRED}}, {{LEGAL_COMPLIANCE_LEVEL}}, {{SEO_PRIORITY}}?
- DACH-Recht/DSGVO/TTDSG berücksichtigen (Impressum, Datenschutz, Consent-Management, Kontaktformular-Daten).
- Auf {{PRIMARY_GOAL}} und {{CTA}} optimieren (Conversion-First, trotzdem seriös).
- Im Ton: {{BRAND_TONE}}.

INPUT:
Nutze alle Variablenwerte ({{...}}). Wenn Informationen fehlen, triff sinnvolle Annahmen, markiere sie explizit als "Annahme" und liefere Alternativen – ohne Rückfragen.

OUTPUT-FORMAT (in Word):
- Start mit: Executive Summary (max 10 Zeilen, business-orientiert)
- Danach: Inhaltsverzeichnis (TOC)
- Dann folgende Kapitel (in genau dieser Reihenfolge):

1) Zielbild & Erfolgskennzahlen
   - Zielhierarchie (Primary/Secondary)
   - KPI-Vorschläge (z.B. Kontaktanfragen, CTA-CTR, organischer Traffic)
   - Minimal-Setup für Messbarkeit (datenschutzkonform)

2) Plattform-Entscheidung (Matrix + Empfehlung)
   - Entscheidungsmatrix als Tabelle (Kriterien: Kosten, Aufwand, SEO, Kontrolle, DSGVO, Formulare, Erweiterbarkeit)
   - 3–5 passende Plattform-Kandidaten (kostenlos) + klare Empfehlung je Persona (Einsteiger vs Tech-affin)
   - "Risiken & Trade-offs" pro Plattform (z.B. Subdomain, Ads, Limits)

3) Architektur & Seitenstruktur (Information Architecture)
   - Empfohlene Seiten aus {{PAGES_REQUIRED}}
   - Navigation/Hierarchie, Footer-Logik (Impressum/Datenschutz)
   - Content-Blueprint je Seite (Ziel, Kernaussagen, Proof, CTA)

4) Schritt-für-Schritt Umsetzung – Weg A (No-Code/Low-Code)
   - Setup von Account bis Launch, kleinteilig nummeriert
   - Theme/Layout-Regeln (Spacing, Typografie, Farben {{BRAND_COLORS}})
   - Kontaktformular + Spam-Schutz + Datenminimierung
   - Consent/Tracking: Nur datenschutzkonforme Optionen; wenn unsicher, minimalistisch starten

5) Schritt-für-Schritt Umsetzung – Weg B (Kostenlos, Tech-affin, Static Site)
   - Ziel: schnell, sauber, wartbar (GitHub Pages o.ä.)
   - Minimal-Repo-Struktur (Ordner, Dateien)
   - Build/Deploy Ablauf verständlich erklären
   - Formulare (kostenlos) + DSGVO-Hinweise
   - Performance/SEO-Basics (Meta-Tags, Sitemap, robots, Lighthouse)

6) Recht, Datenschutz & Sicherheit (DACH)
   - Checkliste: Impressumspflicht, Datenschutzerklärung, Auftragsverarbeitung, Einwilligungen, Kontaktformular
   - "Do/Don’t" für Analytics, Fonts, Embedded Media
   - Security-Basics: HTTPS, Passwort/2FA, Admin-Zugänge, Backups (auch bei Free-Plattformen)
   - Klare, pragmatische Hinweise (keine Rechtsberatung, aber Best Practices)

7) SEO & Content-Operative (Quick Wins)
   - Keyword-Ansatz passend zu {{INDUSTRY}} und {{TARGET_AUDIENCE}}
   - OnPage-Checkliste
   - FAQ-Snippets, interne Verlinkung, lokale SEO (falls sinnvoll)
   - Redaktioneller 30-Tage Plan (klein, realistisch)

8) Launch-Plan (QA + Go-Live)
   - Pre-Launch Checklist (Links, Formulare, Mobile, Performance, Indexierung)
   - Post-Launch (Search Console, Monitoring, Iteration)
   - Rollback/Backup-Strategie (minimal, aber vorhanden)

9) Betriebsmodell (Wartung ohne Budget)
   - Monatliche Routine (15–30 Min)
   - Content-Refresh-Zyklen
   - Sicherheit/Updates/Monitoring

10) Anhänge (copy-ready)
   - 1) Copy-Vorlagen für Startseite (3 Varianten: sachlich, vertrauensbildend, performance-orientiert)
   - 2) Kontaktformular-Text + Datenschutzhinweis (kurz)
   - 3) Mini-FAQ (5–8 Fragen)
   - 4) Abnahmekriterien (Definition of Done)

QUALITÄTSSTANDARDS:
- Schreibe konkret, keine Allgemeinplätze. Jede Empfehlung braucht einen "Warum"-Satz.
- Arbeite mit nummerierten Schritten, Checklisten und Tabellen, damit die Umsetzung ohne externe Hilfe möglich ist.
- Verwende DACH-konforme Terminologie (Impressum, Datenschutzerklärung, Einwilligung, Auftragsverarbeitung).
- Baue "Assumption Log” ein (kurz) und "Decision Log” (welcher Weg wann).
- Halte das Ergebnis in einer einzigen Word-Datei, gut strukturiert, direkt nutzbar.

LIMITS:
- Keine externen Links erforderlich (nur wenn absolut nötig; dann sparsam).
- Keine rechtliche Beratung behaupten; als Best Practices formulieren.
- Keine Tools empfehlen, die zwingend laufende Kosten verursachen.

LIEFERE JETZT DAS ERGEBNIS.
```

---

## 3) Optionale Add-ons (für noch mehr Präzision)
> Diese Zeilen kannst du bei Bedarf **unter** den Master-Prompt hängen.

```text
- Priorisiere Plattformen, die ohne Werbung auskommen; wenn nicht möglich, kennzeichne das klar.
- Lege besonderen Fokus auf: Conversion-Optimierung ({{CTA}}) + Vertrauen (Referenzen/Proof).
- Lege eine "Minimal Viable Website" (MVW) fest: Was muss in 24h live gehen?
- Erstelle eine Micro-Copy Liste (Buttons, Headlines, Error-Messages) im Ton {{BRAND_TONE}}.
```