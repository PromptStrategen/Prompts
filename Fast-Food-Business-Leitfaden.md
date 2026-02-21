> **Zweck:** Dieser Prompt erzeugt einen **vollständigen, umsetzbaren Leitfaden** für den Aufbau oder die Optimierung eines **Fast-Food-Business** (z. B. Burger, Döner, Pizza, Chicken, Bowls, Foodtruck).  
> **Format:** Agentur-Briefing + variablenbasierte Steuerung + klare Deliverables + Qualitäts-Gates.  
> **Hinweis:** Platzhalter in `{{...}}` bitte ausfüllen. Nicht ausgefüllte Felder werden als Annahmen behandelt und müssen transparent markiert werden.

---

## 1) Variablenblock (User-Input)
Kopieren, ausfüllen, unter den Prompt setzen:

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Strategie + Go-to-Market + Ops-Enablement)"
{{PROJECT_NAME}} = "Fast-Food-Business-Leitfaden 360°"

{{BUSINESS_TYPE}} = "Stationäres Restaurant"  # Stationäres Restaurant | Take-away | Delivery-first | Foodtruck | Franchise | Ghost Kitchen
{{CUISINE_FOCUS}} = "Burger & Fries"          # z.B. Döner, Pizza, Fried Chicken, Asian Bowls, Vegan, Mixed
{{BRAND_NAME}} = "Beispiel: Crunch & Co."
{{LOCATION_CITY}} = "Nürnberg"
{{TARGET_AREA_TYPE}} = "Innenstadt"           # Innenstadt | Wohngebiet | Bahnhofsumfeld | Gewerbegebiet | Campus | Event-Gelände
{{COUNTRY_REGION}} = "Deutschland (DACH)"
{{LANGUAGE}} = "Deutsch"

{{TARGET_CUSTOMERS_PRIMARY}} = "Pendler & Mittagstisch"  # 1–2 Hauptsegmente
{{TARGET_CUSTOMERS_SECONDARY}} = "Abendkunden & Delivery" # optional
{{POSITIONING}} = "Schnell, konsistent, hochwertig – zum fairen Preis"
{{UVP}} = "In 4 Minuten fertig + frische Zutaten + Signature-Sauce"
{{PRICE_TIER}} = "Mid"                         # Budget | Mid | Premium
{{AVERAGE_TICKET_EUR}} = 11.90                 # durchschnittlicher Warenkorb
{{OPENING_HOURS}} = "Mo–Sa 11–22 Uhr"
{{CAPACITY}} = "45 Sitzplätze + Take-away"

{{CHANNELS}} = "Walk-in, Google Maps, Lieferando/Wolt/UberEats, Instagram, TikTok"
{{DELIVERY_STRATEGY}} = "Hybrid"               # none | Plattform | own-delivery | Hybrid
{{MENU_COMPLEXITY}} = "Low"                    # Low | Medium | High
{{MENU_ITEMS_COUNT}} = 12
{{SIGNATURE_ITEMS}} = "Signature Burger, Loaded Fries, Hausgemachte Limo"
{{DIETARY_OPTIONS}} = "Vegan Option + glutenarm" # optional

{{STARTING_BUDGET_EUR}} = 45000
{{MONTHLY_MARKETING_BUDGET_EUR}} = 1200
{{TEAM_SIZE_INITIAL}} = 6
{{SUPPLIERS_STATUS}} = "Noch offen"            # offen | teilweise fix | fix
{{EQUIPMENT_STATUS}} = "Teilweise vorhanden"   # none | teilweise | vorhanden

{{GOALS_90D}} = "Eröffnung + 250 Bestellungen/Woche + 4.6★ Google"
{{GOALS_12M}} = "Stabiler Monatsumsatz 80k€ + zweite Filiale prüfen"
{{CONSTRAINTS}} = "DSGVO, Lebensmittelhygiene, begrenzte Küche (20 m²)"
{{RISKS_KNOWN}} = "Personalfluktuation, Preissensibilität, Lieferzeiten"
{{COMPETITORS_NOTED}} = "Lokale Burgerläden + Ketten im Umkreis"
{{UNIQUE_STORY}} = "Familienrezept & lokale Zutaten"
{{BRAND_TONE}} = "Modern, direkt, humorvoll, zuverlässig"
{{EMOJI_LEVEL}} = "low"                        # none | low | medium
```

---

## 2) Copy-&-Paste Master-Prompt (1 Prompt)

```text
Du bist ein interdisziplinäres Expertenteam, gesteuert durch {{AGENCY_NAME}} ({{AGENCY_ROLE}}):
- Strategieberatung (Business Model, Positionierung, Pricing)
- Gastronomie/Ops (Küche, Prozesse, Service Design, HACCP/Qualität)
- Finance/Controlling (Unit Economics, Break-even, Forecast, KPI-System)
- Growth Marketing (Brand, Acquisition, Retention, Local SEO, Paid Social)
- Produkt/UX (Menu Engineering, Angebotsarchitektur, Bundles, Upsell)
- Legal/Compliance (DACH-Basics: DSGVO, Impressum, Hygiene/Allergen-Kommunikation, Arbeitsrecht-Basics – ohne Rechtsberatung zu behaupten)

AUFGABE:
Erstelle einen **Fast-Food-Business-Leitfaden 360°** für {{BRAND_NAME}} im Format eines **operativen Handbuchs** plus **Marketing-Playbook**.
Der Leitfaden muss **konkret, umsetzbar, zahlenorientiert** sein und an {{BUSINESS_TYPE}} / {{CUISINE_FOCUS}} / {{LOCATION_CITY}} angepasst werden.
Arbeite in {{LANGUAGE}}. Tonalität: {{BRAND_TONE}}. Emoji-Level: {{EMOJI_LEVEL}}.

WICHTIG:
1) Wenn Informationen fehlen, triff **realistische Annahmen** und markiere sie klar als **[ANNAHME]**. Stelle keine Rückfragen.
2) Liefere **Checklisten, Vorlagen, SOPs (Standard Operating Procedures)** und **Quality Gates** (Messpunkte).
3) Baue einen **90-Tage-Plan** und einen **12-Monats-Roadmap** mit KPIs.
4) Berücksichtige typische DACH-Rahmenbedingungen (z. B. Allergene, Kassen-/Belegpflicht-Realität allgemein, DSGVO bei Newsletter/Tracking, Hygieneprozesse).
5) Fokus auf **Profitabilität** und **Geschwindigkeit**: kurze Wege, klare Rollen, wenige aber starke Menu-Items, stabile Qualität.
6) Keine leeren Buzzwords. Jede Empfehlung braucht: (a) Warum, (b) Umsetzungsschritte, (c) KPI/Erfolgskriterium, (d) Risiko & Mitigation.

EINGABEN (Variablen):
- Business: {{BUSINESS_TYPE}}, {{CUISINE_FOCUS}}, {{POSITIONING}}, {{UVP}}, {{PRICE_TIER}}, {{AVERAGE_TICKET_EUR}}
- Markt/Ort: {{LOCATION_CITY}}, {{TARGET_AREA_TYPE}}, {{COUNTRY_REGION}}, {{COMPETITORS_NOTED}}
- Zielgruppen: {{TARGET_CUSTOMERS_PRIMARY}}, {{TARGET_CUSTOMERS_SECONDARY}}
- Angebot: {{MENU_COMPLEXITY}}, {{MENU_ITEMS_COUNT}}, {{SIGNATURE_ITEMS}}, {{DIETARY_OPTIONS}}
- Kanäle: {{CHANNELS}}, {{DELIVERY_STRATEGY}}
- Ressourcen: {{STARTING_BUDGET_EUR}}, {{MONTHLY_MARKETING_BUDGET_EUR}}, {{TEAM_SIZE_INITIAL}}
- Betrieb: {{OPENING_HOURS}}, {{CAPACITY}}, {{SUPPLIERS_STATUS}}, {{EQUIPMENT_STATUS}}
- Ziele: {{GOALS_90D}}, {{GOALS_12M}}
- Constraints/Risiken: {{CONSTRAINTS}}, {{RISKS_KNOWN}}, {{UNIQUE_STORY}}

AUSGABEFORMAT (streng einhalten, mit Überschriften in Word):

# {{PROJECT_NAME}} – Leitfaden für {{BRAND_NAME}} ({{LOCATION_CITY}})
## Executive Summary (max. 12 Bullet Points)
- 3 wichtigste Hebel (Profit, Speed, Quality)
- 3 größte Risiken + Gegenmaßnahmen
- 3 Top-KPIs, die täglich/wöchentlich getrackt werden

## 1) Business Model & Positionierung
### 1.1 Zielgruppen & Jobs-to-be-done
- Primär/Sekundär-Segmente, Bedürfnisse, Kauftrigger, Preissensibilität
### 1.2 Wettbewerb & Differenzierung
- Konkurrenten-Typen, Lücken, klare Differenzierung
### 1.3 Angebotsarchitektur (Bundles, Upsell, Cross-Sell)
- 5–8 Bundle-Ideen + Upsell-Mechaniken (z. B. Upgrade, Add-ons, Dessert)
### 1.4 Pricing-Logik
- Preisspannen, psychologische Preisanker, Promo-Grenzen (kein "Race to the bottom")

## 2) Menu Engineering & Produktstandard
### 2.1 Menüprinzipien (Schnelligkeit + Konsistenz)
- Regeln für Item-Anzahl, Zutaten-Wiederverwendung, Stationen-Design
### 2.2 Kernmenü ({{MENU_ITEMS_COUNT}} Items) – Vorschlag
- Tabelle: Item | Preis | COGS-Schätzung | Marge | Prep-Time | Upsell-Potenzial
### 2.3 Rezept-/Portionierungsstandard
- Portionierung, Grammaturen, Foto-Standard, Allergen-Hinweise (DACH)
### 2.4 Qualitätsmanagement (HACCP-Logik auf Pragmatik)
- Kritische Kontrollpunkte, Temperatur-Checks, Reinigungsplan

## 3) Operations: Prozesse, Rollen, Layout
### 3.1 Rollen & Schichtmodell ({{TEAM_SIZE_INITIAL}} Personen)
- Rollenbeschreibung je Position + Verantwortlichkeiten (RACI light)
### 3.2 SOPs (Standard Operating Procedures) – als Checklisten
- Opening SOP
- Peak-Time SOP (Rush Hour)
- Closing SOP
- Delivery SOP (Plattform & Hybrid)
- Reklamations SOP (inkl. Refund/Replacement-Policy)
### 3.3 Layout- & Stationenlogik (Speed)
- Stationen, Wege, Engpässe, "One-Touch"-Prinzip
### 3.4 Lieferkette & Einkauf
- Supplier-Auswahlkriterien, Mindestlager, FIFO, Notfallplan

## 4) Unit Economics & Finanzmodell (konkret)
### 4.1 Grundformeln (verständlich)
- Umsatz, COGS, Bruttomarge, Personalkostenquote, Deckungsbeitrag, Break-even
### 4.2 Beispielrechnung (mit {{AVERAGE_TICKET_EUR}})
- Szenarien: konservativ / realistisch / aggressiv
- Break-even: Bestellungen/Tag und Umsatz/Monat
### 4.3 KPI-Dashboard (Daily/Weekly/Monthly)
- Tabelle: KPI | Zielwert | Messmethode | Verantwortlich | Frequenz
### 4.4 Cashflow & Budget-Guardrails
- 5 Budget-Regeln (z. B. Promo-Cap, Food-Waste-Cap, Plattformgebühren)

## 5) Marketing & Go-to-Market (Local-first)
### 5.1 Brand Foundation
- Markenstory ({{UNIQUE_STORY}}), Tonalität, Kernbotschaften, Claims (10 Vorschläge)
### 5.2 Local SEO & Google Maps Playbook
- Profil-Setup, Foto-Plan, Review-Engine, Q&A, Posts, NAP-Konsistenz
### 5.3 Social Content Engine ({{CHANNELS}})
- Content-Pillars (5), Hook-Formeln (10), 30 Content-Ideen
- 4 Wochen Redaktionsplan (mit Posting-Frequenz)
### 5.4 Paid & Performance (wenn Budget passt)
- Kanalwahl, Zielgruppen, Creatives, Landing/Tracking-Setup (DSGVO-Basics)
- 3 Kampagnen-Blueprints: Opening, Retargeting, Lunch-Boost
### 5.5 Retention & Wiederkäufe
- Loyalty-Mechaniken, Stempelkarten/QR, Bundles, Newsletter/WhatsApp (DSGVO-Hinweise)

## 6) Compliance & Risiko (DACH-Basics, ohne Rechtsberatung)
- Allergen-/Zusatzstoff-Kommunikation, Hygiene-Doku, DSGVO bei Kundendaten
- Personal: Onboarding, Unterweisung, Schichtdoku (high-level)
- Haftungs-/Risikomatrix: Risiko | Impact | Wahrscheinlichkeit | Mitigation

## 7) 90-Tage-Plan (Sprint-Plan mit Quality Gates)
- Woche 1–2: Setup (Menü, Lieferanten, SOPs, Branding)
- Woche 3–4: Soft-Launch + Feedback-Loops
- Woche 5–8: Skalierung (Speed, Reviews, Ads)
- Woche 9–12: Optimierung (Marge, Waste, Retention)
Für jede Woche: Ziele, Tasks, Owner, KPI, Quality Gate

## 8) 12-Monats-Roadmap (Skalierung & Expansion)
- Quartal 1–4: Schwerpunkt, Meilensteine, KPIs, Investitionspunkte
- "Zweite Filiale/Franchise/Ghost Kitchen"-Entscheidungslogik

## 9) Anhänge (Templates & Copy-Paste)
- SOP-Checklisten (kurz + ausführlich)
- KPI-Sheet (Tabellenformat)
- Beispiel-Speisekarte (Text)
- Review-Reply-Vorlagen (positiv/negativ)
- Reklamations-Skripte (Frontline)
- Stellenanzeigen-Text + Interviewfragen (3 Rollen)
- Einkaufsliste & Wareneingang-Check
- Social Captions (20) + Hashtags (DACH/Local)
- Launch-Plan "Grand Opening" (7 Tage Countdown)

QUALITÄTSKONTROLLE (am Ende):
- Liste "Top 10 Handlungsschritte" (1 Woche umsetzbar)
- Liste "Top 10 Messpunkte" (KPIs) + Zielwerte
- Liste "Was weglassen?" (Scope-Cut) um Speed & Qualität zu sichern
- Kurzer Risiko-Check: Was könnte scheitern, und wie verhindern wir’s?

LIEFERE ALLES ALS Word Dokument, sauber formatiert, mit Tabellen wo sinnvoll.
```

