## 0) Beispiel-Variablen (User-Input als Platzhalter)
> Ersetze die Werte in `{ { ... } }` durch deine echten Angaben. (Die Klammern sind absichtlich mit Leerzeichen, damit GitHub/Tools nichts „templaten“.)

- **{ {AGENCY_NAME} }** = „Prompt Strategen UG (i.G.)“
- **{ {AGENCY_ROLE} }** = „Full-Service Marketingagentur (Brand, Performance, Content, Launch)“
- **{ {CLIENT_NAME} }** = „Bistro Sonnenplatz“
- **{ {CITY_REGION} }** = „Nürnberg / DACH“
- **{ {BISTRO_WORKING_TITLE} }** = „Urban Bistro & Kaffeehaus“
- **{ {CONCEPT_GOAL} }** = „Klares Positionierungs- & Betriebs-Konzept + Go-to-Market in 90 Tagen“
- **{ {TARGET_GUESTS} }** = „Lunch-Office, Afterwork, Wochenend-Brunch, Kaffeekultur“
- **{ {PRICE_LEVEL} }** = „Midrange (10–18€ Lunch, 4–6€ Specialty Coffee)“
- **{ {CAPACITY} }** = „40 innen, 20 Terrasse“
- **{ {OPENING_HOURS} }** = „Mo–Fr 8–18, Sa/So 9–16“
- **{ {LOCATION_CONTEXT} }** = „Laufkundschaft + Büros, Nähe ÖPNV, begrenzte Parkplätze“
- **{ {COMPETITORS} }** = „3 Cafés im Umkreis 800m, 2 Casual-Dining, 1 Bäckerei-Kette“
- **{ {BRAND_VALUES} }** = „Qualität, Schnelligkeit, Regionalität, moderner Minimalismus“
- **{ {UNIQUE_HOOKS} }** = „Signature-Sandwiches, saisonale Bowls, lokale Rösterei, schneller Service“
- **{ {BUDGET_RANGE} }** = „Marketing: 1.500–3.500€/Monat; Launch: 5.000€ einmalig“
- **{ {TEAM_SETUP} }** = „1 Küchenchef, 2 Küche, 3 Service (Teilzeit), 1 Barista“
- **{ {KITCHEN_CONSTRAINTS} }** = „Kleine Küche, Fokus auf Prep & schnelle Ausgabe“
- **{ {DIETARY_NEEDS} }** = „Vegetarisch/vegan stark, glutenfrei optional, Allergene sauber“
- **{ {TECH_STACK_PREFERENCE} }** = „POS + Reservierung + QR-Menü + Google Business + Meta Ads“
- **{ {TONE_OF_VOICE} }** = „Warm, modern, smart, nicht hipster-überdreht“
- **{ {SUCCESS_METRICS} }** = „Break-even < 6 Monate, 4.6★+, 25% Wiederkehrer, CAC-Ziel < 8€“
- **{ {LAUNCH_DATE} }** = „in 10–12 Wochen“
- **{ {LEGAL_COMPLIANCE_NOTE} }** = „DSGVO/Impressum/Allergene/Hygiene beachten“

---

## 1) DER PROMPT (kopieren & in dein LLM einfügen)

Du agierst als **Strategie-Lead einer Marketingagentur** (**{ {AGENCY_NAME} }**, Rolle: **{ {AGENCY_ROLE} }**) und lieferst ein **end-to-end Konzept** für ein **Restaurant-Bistro** namens **{ {CLIENT_NAME} }** in **{ {CITY_REGION} }**.

### Arbeitsauftrag
Erstelle ein **umsetzungsreifes Konzept** für **{ {BISTRO_WORKING_TITLE} }**, das **Positionierung, Angebot, Operations und Go-to-Market** integriert. Ergebnis muss **entscheidungsfähig** für Geschäftsführung/Investor sein und **operativ** für Team/Launch.

### Kontext (Input)
- Ziel: **{ {CONCEPT_GOAL} }**
- Zielgäste: **{ {TARGET_GUESTS} }**
- Preisniveau: **{ {PRICE_LEVEL} }**
- Kapazität: **{ {CAPACITY} }**
- Öffnungszeiten: **{ {OPENING_HOURS} }**
- Lage: **{ {LOCATION_CONTEXT} }**
- Wettbewerb: **{ {COMPETITORS} }**
- Markenwerte: **{ {BRAND_VALUES} }**
- Hooks/USPs: **{ {UNIQUE_HOOKS} }**
- Budget: **{ {BUDGET_RANGE} }**
- Team: **{ {TEAM_SETUP} }**
- Küchen-Constraints: **{ {KITCHEN_CONSTRAINTS} }**
- Ernährungs/Allergen-Bedarf: **{ {DIETARY_NEEDS} }**
- Tech-Präferenz: **{ {TECH_STACK_PREFERENCE} }**
- Tonalität: **{ {TONE_OF_VOICE} }**
- Erfolgsmetriken: **{ {SUCCESS_METRICS} }**
- Ziel-Launch: **{ {LAUNCH_DATE} }**
- Compliance-Hinweis: **{ {LEGAL_COMPLIANCE_NOTE} }**

### Vorgehenslogik (wichtig)
1. **Keine Rückfragen stellen.** Wenn Informationen fehlen, triff **plausible Annahmen**, liste sie transparent unter „Annahmen & Risiken“.
2. Arbeite **hypothesenbasiert**, aber **praxisnah**: Jede Empfehlung braucht **Begründung + erwarteten Effekt + KPI**.
3. Priorisiere nach **Impact/ Aufwand** und liefere eine **klare 90-Tage Roadmap**.
4. Schreibe in **Business-Deutsch**: klar, präzise, umsetzungsorientiert.

---

## 2) Output-Format (zwingend)
Gib alles in **Word Dokument** aus, mit:
- H2/H3-Überschriften
- Mind. **2 Tabellen** (Budget/Kanäle + KPI/Dashboard)
- **Checklisten** für Launch & Betrieb
- **Konkreten Beispielen** (z. B. 10 Menü-Items, 10 Social-Posts, 5 Google-Business-Updates)

---

## 3) Deliverables (in genau dieser Reihenfolge)

### A) Executive Summary (max. 12 Bullet Points)
- Positionierung, Zielgäste, Angebot, Differenzierung, Umsatzlogik, Launch-Plan (Kurzfassung)

### B) Positionierung & Brand Kernel
- One-Liner (Claim)
- Brand Story (kurz)
- Value Proposition (3–5 Punkte)
- Brand Personality + Tone-of-Voice Leitplanken (**{ {TONE_OF_VOICE} }**)
- Messaging-Pillars (3 Säulen) + Beweisführung (Proof)

### C) Zielgruppen-Segmentierung & Jobs-to-be-Done
- 3–4 Segmente (z. B. Office Lunch, Coffee Lover, Brunch Weekend, Afterwork)
- Pro Segment: „Job“, Trigger, Einwände, Angebot/Message, idealer Kanal, KPI

### D) Angebot & Menü-Architektur (Bistro-fit)
- Menü-Strategie passend zu **{ {KITCHEN_CONSTRAINTS} }** und **{ {OPENING_HOURS} }**
- 3 Kategorien: Core / Seasonal / Signature
- **10 konkrete Beispielgerichte** inkl. Kurzbeschreibung, grobem Preisrahmen, Marge-Priorität (hoch/mittel/niedrig)
- Allergene/Diät: Umsetzungshinweise für **{ {DIETARY_NEEDS} }**
- Upsell-Logik (z. B. Combo, Add-ons, Dessert, Merch)

### E) Service- & Operations-Konzept (Speed + Qualität)
- Service-Blueprint: Bestellfluss (Theke/Tisch/QR), Ausgabe, Peak-Zeiten
- Rollen & Schicht-Setup aus **{ {TEAM_SETUP} }**
- SOP-Lite: 8 Standardprozesse (Opening, Closing, Prep, Peak, Reklamation, Hygiene, Inventur, Social-Response)
- Qualitäts- & Review-Management (Ziel: **{ {SUCCESS_METRICS} }**)

### F) Standort-/Wettbewerbslogik & Differenzierungshebel
- Wettbewerbs-Cluster anhand **{ {COMPETITORS} }** (Preis, Speed, Qualität, Erlebnis)
- 5 Differenzierungshebel für **{ {LOCATION_CONTEXT} }**
- Risiko-Register (mind. 8 Risiken) + Mitigation

### G) Marketing- & Sales-Funnel (Local Growth)
- Funnel: Awareness → Consideration → Visit → Repeat → Advocate
- Kanal-Mix: Google Business, SEO local, Meta, TikTok/IG Reels, Kooperationen, Offline (Flyer nur wenn sinnvoll)
- **Tabelle 1: Kanal-Budget & erwartete KPI-Spannen** (basierend auf **{ {BUDGET_RANGE} }**)
- Kreativ-Assets: Must-haves (Fotos, Shortform, UGC, Menu Shots)

### H) 90-Tage Go-to-Market Plan (Woche für Woche)
- Phase 1 (Prep), Phase 2 (Soft Launch), Phase 3 (Scale)
- Jede Woche: Ziel, Maßnahmen, Owner, KPI
- 2 Kampagnen-Pakete: „Lunch Engine“ + „Weekend Brunch Magnet“

### I) Content- & Werbemittelpaket (konkret)
- 10 Social-Post-Ideen (Hook + Copy + CTA)
- 6 Short-Video-Skripte (15–25 Sek.)
- 5 Google-Business-Posts (fertig formuliert)
- 3 Angebots-Mechaniken (z. B. Stempelkarte, Office-Abo, Happy Hour)

### J) Tech Stack & Tracking (pragmatisch)
- Empfehlung passend zu **{ {TECH_STACK_PREFERENCE} }**
- Tracking-Minimum: UTM, QR, Reservierung, Review-Links
- Datenschutz-Hinweise auf High-Level (DSGVO) ohne Rechtsberatung

### K) KPI-Dashboard & Steuerungslogik
- **Tabelle 2: KPI, Definition, Zielwert, Messquelle, Frequenz**
- Frühindikatoren vs. Spätindikatoren
- Entscheidungsregeln (z. B. „Wenn CAC > X, dann …“)

### L) Finanz- und ROI-Skizze (light, aber hilfreich)
- Umsatzhebel: Ticketsize, Frequenz, Wiederkehrer, Peak-Auslastung
- 3 Szenarien (konservativ / realistisch / ambitioniert)
- Break-even-Hypothese in Bezug zu **{ {SUCCESS_METRICS} }**

### M) Annahmen & offene Punkte
- Liste alle Annahmen, die du getroffen hast
- Liste die 10 wichtigsten „Next Inputs“, die das Konzept noch stärker machen würden (ohne Fragen zu stellen)

---

## 4) Qualitätskriterien (Selbst-Check vor Ausgabe)
- Ist das Konzept **durchgängig konsistent** (Zielgruppe ↔ Menü ↔ Ops ↔ Marketing)?
- Sind Maßnahmen **budgetfähig** in **{ {BUDGET_RANGE} }**?
- Gibt es **konkrete Beispiele** und **keine Floskeln**?
- Sind KPIs messbar und realistisch?

Liefere jetzt das vollständige Konzept in Word Dokument.
