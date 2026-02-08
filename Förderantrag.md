## Variablen (User-Input Platzhalter) + Beispielwerte
- {{FOERDERPROGRAMM_NAME}} = "go-digital" *(Beispiel)*
- {{FOERDERGEBER}} = "BMWK / autorisierte Beratungsunternehmen" *(Beispiel)*
- {{FOERDERQUOTE}} = "50%" *(Beispiel, falls bekannt)*
- {{MAX_FOERDERSUMME}} = "16.500 EUR" *(Beispiel, falls bekannt)*
- {{ANTRAGSFRIST}} = "2026-03-31" *(Beispiel)*
- {{REGION}} = "Deutschland, Bayern, Nürnberg" *(Beispiel)*

- {{AGENTUR_NAME}} = "KampagnenKraft GmbH" *(Beispiel)*
- {{RECHTSFORM}} = "GmbH" *(Beispiel)*
- {{GRUENDUNGSJAHR}} = "2021" *(Beispiel)*
- {{MITARBEITERZAHL}} = "12" *(Beispiel)*
- {{UMSATZ_KLASSE}} = "0,5–2,0 Mio. EUR p.a." *(Beispiel)*
- {{WEBSITE}} = "https://example-agency.tld" *(Beispiel)*
- {{ANSPRECHPARTNER}} = "Dieter Damps, Geschäftsführer" *(Beispiel)*
- {{KONTAKT_EMAIL}} = "office@example-agency.tld" *(Beispiel)*

- {{AUSGANGSLAGE_PROBLEM}} = "Hoher manueller Aufwand in Kampagnen-Setup, Reporting und Lead-Nurturing; Medienbrüche zwischen CRM, Ads, Analytics und Abrechnung; Qualitäts- und Skalierungsgrenzen." *(Beispiel)*
- {{PROJEKT_TITEL}} = "KI-gestützte Marketing-Automatisierung & Reporting-Standardisierung" *(Beispiel)*
- {{PROJEKT_ZIELBILD}} = "End-to-end Automatisierung von Lead-Intake → Segmentierung → Kampagnen-Ausspielung → Performance-Reporting; klare Governance, DSGVO-by-design." *(Beispiel)*
- {{ZIELGRUPPE}} = "KMU-Kunden (B2B), 10–500 MA; Branchen: Dienstleistung, Handel, SaaS" *(Beispiel)*

- {{ARBEITSPAKETE}} = "WP1 Ist-Analyse; WP2 Zielbild/Architektur; WP3 Tooling & Integrationen (CRM/Ads/Analytics); WP4 KI-Assistenz für Content/Ads; WP5 Reporting-Dashboard & KPI-Standard; WP6 Schulung & Übergabe" *(Beispiel)*
- {{MEILENSTEINE}} = "M1 Kickoff; M2 Soll-Konzept; M3 MVP live; M4 Rollout; M5 Abnahme" *(Beispiel)*
- {{LAUFZEIT_WOCHEN}} = "12" *(Beispiel)*
- {{RESSOURCEN_INTERN}} = "PM 0,2 FTE; Tech 0,3 FTE; Data 0,2 FTE" *(Beispiel)*
- {{DIENSTLEISTER_EXTERN}} = "Implementierungspartner für CRM-Integration" *(Beispiel, optional)*

- {{GESAMTBUDGET_EUR}} = "45.000" *(Beispiel)*
- {{EIGENANTEIL_EUR}} = "22.500" *(Beispiel)*
- {{FOERDERBEDARF_EUR}} = "22.500" *(Beispiel)*
- {{KOSTENBLOECKE}} = "Beratung; Implementierung; Lizenzen; Schulung; Dokumentation" *(Beispiel)*
- {{BEIHILFERECHT_HINWEIS}} = "De-minimis relevant? Ja/Nein/Unbekannt" *(Beispiel)*

- {{KPI_LISTE}} = "Setup-Zeit -30%; Reporting-Aufwand -50%; Lead-Response-Time -40%; Conversion +10%; Fehlerquote -60%" *(Beispiel)*
- {{RISIKEN}} = "Datenqualität; Tool-Abhängigkeiten; Change-Management; Compliance" *(Beispiel)*
- {{COMPLIANCE}} = "DSGVO, TOMs, AVV, Rollen-/Rechtekonzept" *(Beispiel)*

---

## PROMPT (kopieren, ausfüllen, ausführen)

Du bist ein **Senior Grant Writer + Projektleiter Digitalisierung + Controller** für Fördermittel in Deutschland/EU.  
Dein Auftrag: Erstelle einen **förderlogisch sauberen, prüffähigen Förderantrag** für eine **Marketing-Agentur** auf Basis der Variablen unten.  
Arbeite **faktenbasiert**: Wenn Informationen fehlen oder unklar sind, **stelle gezielte Rückfragen** in einem kompakten Block. **Erfinde keine Programmdetails** (Förderquote, Maximalsummen, Fristen, Kriterien). Markiere Annahmen explizit als **Annahme**.

### 1) Input (Variablen)
Nutze ausschließlich die folgenden Variablen als Quelle:
- Förderkontext: {{FOERDERPROGRAMM_NAME}}, {{FOERDERGEBER}}, {{FOERDERQUOTE}}, {{MAX_FOERDERSUMME}}, {{ANTRAGSFRIST}}, {{REGION}}
- Organisation: {{AGENTUR_NAME}}, {{RECHTSFORM}}, {{GRUENDUNGSJAHR}}, {{MITARBEITERZAHL}}, {{UMSATZ_KLASSE}}, {{WEBSITE}}, {{ANSPRECHPARTNER}}, {{KONTAKT_EMAIL}}
- Projekt: {{PROJEKT_TITEL}}, {{AUSGANGSLAGE_PROBLEM}}, {{PROJEKT_ZIELBILD}}, {{ZIELGRUPPE}}, {{ARBEITSPAKETE}}, {{MEILENSTEINE}}, {{LAUFZEIT_WOCHEN}}, {{RESSOURCEN_INTERN}}, {{DIENSTLEISTER_EXTERN}}
- Finanzen: {{GESAMTBUDGET_EUR}}, {{EIGENANTEIL_EUR}}, {{FOERDERBEDARF_EUR}}, {{KOSTENBLOECKE}}, {{BEIHILFERECHT_HINWEIS}}
- Steuerung: {{KPI_LISTE}}, {{RISIKEN}}, {{COMPLIANCE}}

### 2) Output-Anforderungen (Format & Qualität)
- Ausgabe **auf Deutsch**, im **Business-/Unternehmensjargon**, klar, präzise, ohne Fülltext.
- Format: **Markdown**, mit sauberer Gliederung, Tabellen wo sinnvoll.
- Liefere **prüffähige** Inhalte: klare Ziel-Logik (Problem → Maßnahme → Output → Outcome), messbare KPIs, Zeit-/Budgetkonsistenz.
- Ergänze eine **Plausibilitätsprüfung** (z. B. Budget vs. Laufzeit vs. Arbeitspakete) und markiere Inkonsistenzen.
- Datenschutz/Sicherheit: konkretes Minimum-Set (DSGVO, AVV, TOMs, Rollen/Rechte, Datenflüsse) passend zum Projekt.
- Keine Rechtsberatung: Formuliere neutral („sollte geprüft werden“).

### 3) Vorgehenslogik
1. **Intake-Check**: Prüfe, ob die Variablen reichen. Wenn nicht: stelle max. **12** gezielte Rückfragen (priorisiert nach Förderrelevanz).
2. **Draft erstellen**: Erstelle danach den vollständigen Antrag als Entwurf.
3. **Review & Optimierung**: Liefere am Ende eine kurze **Optimierungsliste** (Top 10 Hebel für Bewilligungschance).

---

## 4) Förderantrag-Entwurf (Markdown-Struktur)
Erstelle den Antrag exakt in dieser Struktur:

### A. Management Summary (max. 150 Wörter)
- Nutzenargumentation, Förderzweck-Fit, erwarteter Impact.

### B. Antragstellerprofil
- Kurzprofil {{AGENTUR_NAME}}, Leistungsportfolio (aus Kontext ableiten, sonst Rückfrage), Kapazitäten, Referenzfähigkeit.
- Ausgangssituation/Engpass: {{AUSGANGSLAGE_PROBLEM}}.

### C. Projektbeschreibung
- Projekttitel: {{PROJEKT_TITEL}}
- Zielbild: {{PROJEKT_ZIELBILD}}
- Zielgruppe/Nutzenstifter: {{ZIELGRUPPE}}
- Abgrenzung: Was ist **in scope / out of scope** (falls unklar: Annahme + Rückfrage).

### D. Ziele & KPIs (SMART)
- Tabelle: KPI | Baseline (falls unbekannt: Annahme/„tbd“) | Zielwert | Messmethode | Messzeitpunkt
- Nutze {{KPI_LISTE}} als Grundlage und präzisiere.

### E. Arbeitspakete & Methodik
- Tabelle: WP | Inhalt | Deliverables | Verantwortlich (intern/extern) | Aufwand (PT) | Abhängigkeiten
- Nutze {{ARBEITSPAKETE}} + {{RESSOURCEN_INTERN}} + {{DIENSTLEISTER_EXTERN}}.

### F. Zeitplan & Meilensteine
- Timeline als Tabelle (Woche 1..{{LAUFZEIT_WOCHEN}}): Meilenstein | Termin | Abnahmekriterium
- Nutze {{MEILENSTEINE}}.

### G. Budget- & Finanzierungsplan
- Budgettabelle: Kostenblock | Beschreibung | Netto EUR | Begründung | Förderfähigkeit (tbd falls unbekannt)
- Konsistenzcheck: Summe = {{GESAMTBUDGET_EUR}}; Finanzierung: Eigenanteil {{EIGENANTEIL_EUR}} + Förderbedarf {{FOERDERBEDARF_EUR}}.
- Hinweisblock: {{BEIHILFERECHT_HINWEIS}} (De-minimis etc. „prüfen“).

### H. Wirkung, Nachhaltigkeit, Transfer
- Operative Wirkung (Effizienz, Qualität), wirtschaftliche Wirkung (Skalierung), Wissenstransfer (Schulung/Doku), Nachhaltigkeit (Betrieb/Ownership).

### I. Risiko- & Maßnahmenplan
- Tabelle: Risiko | Eintritt | Auswirkung | Gegenmaßnahme | Owner
- Nutze {{RISIKEN}} und ergänze typische Projektrisiken.

### J. Datenschutz, IT-Sicherheit & Compliance
- Datenflüsse (Text + Mini-Tabelle): Datenquelle → Verarbeitung → System → Rechtsgrundlage/AVV → Speicherfrist
- TOMs: Zugriff, Logging, Verschlüsselung, Backup, Berechtigungskonzept
- Nutze {{COMPLIANCE}}.

### K. Anlagen/Belege (Checkliste)
- Liste: Projektplan, Angebote/Kostenvoranschläge, Unternehmensdaten, ggf. De-minimis Erklärung, Datenschutzdoku, etc. (als „typisch“ kennzeichnen).

### L. Plausibilitäts- & Konsistenzprüfung (Pflicht)
- Bullet-Liste: Widersprüche, fehlende Angaben, kritische Annahmen, „Must-fix“ vor Einreichung.

### M. Optimierungsliste (Top 10)
- Konkrete, umsetzbare Verbesserungen zur Bewilligungschance (z. B. stärkere Problemquantifizierung, Referenzen, Baselines, Angebote, Abgrenzung).

---

## 5) Stilregeln
- Aktiv, konkret, nachweisorientiert („Deliverables“, „Abnahmekriterien“, „Messmethoden“).
- Keine Buzzword-Kaskaden ohne Substanz.
- Zahlen/Einheiten konsistent.
- Wenn etwas unbekannt ist: **„tbd“** + Rückfrage oder Annahme.

BEGINNE JETZT mit dem Intake-Check und liefere anschließend den vollständigen Entwurf.
