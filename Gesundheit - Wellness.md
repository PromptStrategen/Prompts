> **Ziel:** Dieser Prompt erzeugt einen **umsetzungsfertigen Content-Leitfaden** (Strategie + Redaktionssystem + Qualitätsstandards) für Gesundheit & Wellness – in einer Tonalität und Struktur, wie sie eine **Marketing-Agentur** für einen Kunden liefern würde.  
> **Hinweis (Compliance):** Output ersetzt **keine medizinische Beratung**. Keine Diagnosen, keine individuellen Therapiepläne, keine Heilversprechen.

---

## 1) User-Input: Variablenblock (ausfüllen)

Kopiere den Block, fülle ihn aus und setze ihn **oberhalb** des Prompts ein.

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Content-Agentur"
{{CLIENT_BRAND}} = "Beispiel Wellness GmbH"
{{CLIENT_URL}} = "https://example.com"
{{COUNTRY_MARKET}} = "DACH"
{{LANGUAGE}} = "Deutsch"
{{TARGET_AUDIENCE_PRIMARY}} = "Berufstätige 25–45, gesundheitsbewusst, wenig Zeit"
{{TARGET_AUDIENCE_SECONDARY}} = "40+, Prävention & Wohlbefinden"
{{AUDIENCE_PAIN_POINTS}} = "Stress, Schlafprobleme, Energie-Tiefs, unstrukturierte Ernährung"
{{POSITIONING}} = "evidenzorientiert, alltagstauglich, ohne Dogma"
{{BRAND_VOICE}} = "klar, empathisch, seriös, leicht motivierend"
{{EMOJI_LEVEL}} = "none"  # none | low | medium
{{CONTENT_GOALS}} = "Trust aufbauen, Newsletter Leads, organischer Traffic, Produktinteresse"
{{PRIMARY_OFFER}} = "Online-Coaching + Kurse"
{{SECONDARY_OFFERS}} = "E-Book, Newsletter, kostenlose Checklisten"
{{UNIQUE_PROOF}} = "zertifizierte Coaches, wissenschaftliche Quellen, transparente Methoden"
{{COMPETITORS}} = "Marke A, Marke B, Influencer C"
{{DIFFERENTIATION}} = "Wissenschaft + Alltag, keine Quick-Fixes, messbare Routinen"
{{TOPICS_IN_SCOPE}} = "Schlaf, Stress, Ernährung, Bewegung, Mindfulness, Regeneration"
{{TOPICS_OUT_OF_SCOPE}} = "Diagnosen, Medikamente, Therapieanweisungen, Heilversprechen"
{{RISK_TOPICS}} = "Essstörungen, Depression, Angststörungen, Schwangerschaft, chronische Erkrankungen"
{{MEDICAL_DISCLAIMER_STYLE}} = "kurz und klar, am Ende jeder Seite"
{{CHANNELS}} = "Blog, LinkedIn, Instagram, YouTube, Newsletter"
{{CONTENT_FORMATS}} = "How-to, Mythbusting, Checklists, Fallbeispiele, Interviews, Guides"
{{SEO_FOCUS}} = "hoch"  # niedrig | mittel | hoch
{{KEYWORDS_SEED}} = "besser schlafen, stress reduzieren, gesunde routines, achtsamkeit"
{{CONTENT_FREQUENCY}} = "3 Posts/Woche + 1 Newsletter/Woche"
{{TIME_HORIZON_WEEKS}} = 12
{{BUDGET_LEVEL}} = "mittel"  # niedrig | mittel | hoch
{{DATA_AVAILABLE}} = "Website Analytics, Search Console, Newsletter KPIs, Kundenfeedback"
{{SUCCESS_METRICS}} = "CTR, Leads, Newsletter-Opt-ins, Verweildauer, Share-Rate"
{{LEGAL_REQUIREMENTS}} = "DSGVO, Wettbewerbsrecht, keine Heilversprechen"
{{SOURCES_REQUIREMENT}} = "peer-reviewed bevorzugt, Leitlinien/Behörden ok"
{{CITATION_STYLE}} = "Kurzquellen am Ende (Titel, Jahr, Link)"
{{OUTPUT_DEPTH}} = "maximal"
```

---

## 2) Der Prompt (Copy & Paste)

```text
SYSTEM:
Du bist ein Senior-Strategie- und Redaktionsleiter einer Marketing-Agentur mit Fokus auf Health & Wellness, Evidenzkommunikation und Compliance im DACH-Markt. Du arbeitest präzise, detailtief, strukturiert, praxisorientiert. Du vermeidest Heilversprechen, Diagnosen, individuelle Therapieanweisungen und nutzt einen sicheren, verantwortungsvollen Ton. Du kennzeichnest Risiken und verweist bei sensiblen Themen auf professionelle Hilfe.

USER:
Kontext:
{{AGENCY_NAME}} agiert als {{AGENCY_ROLE}} für {{CLIENT_BRAND}} ({{CLIENT_URL}}) im Markt {{COUNTRY_MARKET}}. Sprache: {{LANGUAGE}}.
Zielgruppen:
- Primär: {{TARGET_AUDIENCE_PRIMARY}}
- Sekundär: {{TARGET_AUDIENCE_SECONDARY}}
Pain Points: {{AUDIENCE_PAIN_POINTS}}
Positionierung: {{POSITIONING}}
Brand Voice: {{BRAND_VOICE}} | Emoji-Level: {{EMOJI_LEVEL}}
Ziele: {{CONTENT_GOALS}}
Offer: {{PRIMARY_OFFER}} | Secondary: {{SECONDARY_OFFERS}}
Proof: {{UNIQUE_PROOF}}
Wettbewerb: {{COMPETITORS}} | Differenzierung: {{DIFFERENTIATION}}

Themen:
- In Scope: {{TOPICS_IN_SCOPE}}
- Out of Scope: {{TOPICS_OUT_OF_SCOPE}}
- Risiko-Themen: {{RISK_TOPICS}}
Recht/Compliance: {{LEGAL_REQUIREMENTS}}
Quellenanforderung: {{SOURCES_REQUIREMENT}} | Zitierstil: {{CITATION_STYLE}}
Kanäle: {{CHANNELS}} | Formate: {{CONTENT_FORMATS}}
SEO-Fokus: {{SEO_FOCUS}} | Keyword-Seeds: {{KEYWORDS_SEED}}
Frequenz: {{CONTENT_FREQUENCY}} | Horizont: {{TIME_HORIZON_WEEKS}} Wochen
Budget: {{BUDGET_LEVEL}} | Daten: {{DATA_AVAILABLE}}
Erfolgsmessung: {{SUCCESS_METRICS}}
Disclaimer-Stil: {{MEDICAL_DISCLAIMER_STYLE}}
Ausgabetiefe: {{OUTPUT_DEPTH}}

Aufgabe:
Erstelle einen vollständigen Leitfaden für Health-&-Wellness-Content, der sofort in der Agenturproduktion genutzt werden kann. Liefere das Ergebnis als strukturiertes Dokument mit folgenden Abschnitten (streng in dieser Reihenfolge) und jeweils maximaler Detailtiefe:

1) Executive Summary (1 Seite): Zielbild, Nutzenversprechen, Risikorahmen.
2) Brand- & Message-Architektur:
   - Kernbotschaften (3–5), Proof Points, Tonalitätsregeln, No-Go-Wording.
   - Value Ladder: Free Content → Lead Magnet → Offer.
   - Narrativ-Frameworks (z. B. Problem→Mechanismus→Mini-Schritte→Erwartungsmanagement).
3) Zielgruppen-Deep-Dive:
   - Segmentierung, Jobs-to-be-Done, Einwände, Trigger, "Aha"-Momente.
   - Empathie-Map + konkrete Formulierungsbeispiele.
4) Themenstrategie & Content-Pillars:
   - 4–6 Pillars mit Subthemen, Suchintentionen, Funnel-Phase.
   - Redaktionsregeln: Fakten vs. Meinungen, Evidenzlevels.
   - "Mythbusting"-Policy: Wie Behauptungen geprüft werden.
5) SEO & Informationsarchitektur ({{SEO_FOCUS}}):
   - Cluster-Map (Hub-&-Spoke), interne Verlinkung, FAQ-Strategie.
   - Keyword-Ansatz aus {{KEYWORDS_SEED}}: Themen, Synonyme, Longtails.
   - Snippet-Optimierung, E-E-A-T-Checkliste (praxisnah).
6) Kanal-Playbooks ({{CHANNELS}}):
   Für jeden Kanal: Ziel, Content-Typen, Hook-Patterns, typische Länge, CTA-Logik,
   Posting-Frequenz, Wiederverwendung (Repurposing), Qualitätskriterien.
7) Editorial System (Operations):
   - Workflow von Idee → Briefing → Draft → Review → Legal/Compliance → Publish → Analyse.
   - Rollen/RACI (Agentur + Kunde), Übergabepunkte, Briefing-Template.
   - Review-Checkliste (Inhalt, Ton, SEO, Claims, Quellen).
8) Content-Templates (Copy & Paste):
   - 6 Vorlagen: Guide, Checklist, Mythbusting, Interview, Case Example, Newsletter.
   - Jede Vorlage mit: Struktur, Beispiel-Headlines, Beispiel-CTA, Evidenz-Hinweisen, Disclaimer-Platz.
9) 12-Wochen Redaktionsplan ({{TIME_HORIZON_WEEKS}}):
   - Wöchentlich: 3 Inhalte + 1 Newsletter (gemäß {{CONTENT_FREQUENCY}}).
   - Pro Inhalt: Titel, Kanal, Format, Ziel (Funnel), Kern-CTA, Kurz-Outline, SEO-Keyword.
   - Baue thematische Progression und saisonale Anlässe ein (DACH).
10) Messkonzept & Reporting:
   - KPI-Definitionen, Messpunkte, Dashboard-Logik, Experiment-Backlog (A/B-Ideen).
   - Frühindikatoren vs. Spätindikatoren.
11) Risiko- & Compliance-Modul:
   - Umgang mit {{RISK_TOPICS}}: Safe-Guardrails, Formulierungen, Eskalationslogik.
   - "No medical advice"-Regeln + Beispiele für zulässige vs. unzulässige Aussagen.
   - Werberecht: keine Heilversprechen, keine Vorher/Nachher-Übertreibungen.
12) Quellenpaket (kuratiert):
   - Liste von 12–20 hochwertigen Quellentypen (Leitlinien, Behörden, Journals),
     inkl. Auswahlkriterien und wie sie zitiert werden ({{CITATION_STYLE}}).

Qualitätsanforderungen:
- Schreibe in {{LANGUAGE}} und konsequent in {{BRAND_VOICE}}.
- Keine Diagnosen, keine individuellen Therapiepläne, keine Heilversprechen.
- Bei sensiblen Themen: sichere Formulierungen + Hinweis auf professionelle Hilfe.
- Nutze klare Überschriften, Tabellen wo sinnvoll, und sofort umsetzbare Bulletpoints.
- Liefere am Ende eine "Final QA"-Checkliste (10–15 Punkte) für die Agenturabnahme.

Ausgabeformat:
- Word, sauber gegliedert, mit Inhaltsverzeichnis.
- Tabellen als Excel-Tabellen.
- Keine Emojis, außer {{EMOJI_LEVEL}} ist nicht "none".
```

---

## 3) Beispiel (ausgefüllter Variablenblock – Kurz)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_BRAND}} = "Beispiel Wellness GmbH"
{{COUNTRY_MARKET}} = "DACH"
{{TARGET_AUDIENCE_PRIMARY}} = "Berufstätige 25–45, Stresslevel hoch, wenig Zeit"
{{POSITIONING}} = "evidenzorientiert & alltagstauglich"
{{BRAND_VOICE}} = "klar, empathisch, seriös"
{{CONTENT_GOALS}} = "SEO-Traffic + Newsletter Leads"
{{PRIMARY_OFFER}} = "Online-Coaching + Kurse"
{{TOPICS_IN_SCOPE}} = "Schlaf, Stress, Ernährung, Bewegung, Regeneration"
{{RISK_TOPICS}} = "Essstörungen, Depression, Schwangerschaft"
{{CHANNELS}} = "Blog, LinkedIn, Instagram, Newsletter"
{{SEO_FOCUS}} = "hoch"
{{KEYWORDS_SEED}} = "besser schlafen, stress reduzieren, gesunde routines"
{{CONTENT_FREQUENCY}} = "3 Posts/Woche + 1 Newsletter/Woche"
{{TIME_HORIZON_WEEKS}} = 12
```

---

## 4) Implementierungs-Quickstart (Agentur-ready)

1. **Variablenblock** vollständig ausfüllen (insb. Risiken, No-Go, Angebote).  
2. Prompt 1:1 in ein LLM einsetzen.  
3. Ergebnis intern mit der **Final QA** abnehmen lassen.  
4. Aus Leitfaden: **Briefing-Template** + **Redaktionsplan** direkt in Tooling übernehmen (Notion/Jira/Asana).  
5. Nach 2 Wochen: KPI-Review, Themen nach Suchdaten & Engagement nachschärfen.

---

## 5) Optional: Prompt-Tuning (bei Bedarf)

- **Mehr wissenschaftlich:** Brand Voice um "nüchtern, evidenzstark" ergänzen.  
- **Mehr Conversion:** Content Goals um "Produktdemo/Call" erweitern + CTA-Mechanik pro Kanal strenger definieren.  
- **Mehr Safety:** Risiko-Themen erweitern + Eskalationslogik verschärfen.
