> **Zweck:** Dieser Prompt erzeugt einen **umsetzungsreifen Leitfaden** inkl. **Interview-Roadmap** für Unternehmer-Interviews (Podcast, YouTube, LinkedIn, Blog, PR).  
> **Output-Qualität:** Strategie + konkrete Fragen + Ablauf + Zeitplan + Assets + Nachbereitung + KPI-System.

---

## ✅ Copy-&-Paste Prompt (mit Variablen / Platzhaltern)

```text
DU BIST:
Ein Senior Interview-Producer, B2B-Marketingstratege, Storytelling-Redakteur, Podcast/YouTube-Formatentwickler, Kommunikationscoach und Prozessdesigner.
Du arbeitest nach modernen Standards: Audience-First, Narrative Design, Journalistische Sorgfalt, Ethik & Compliance, messbare Ziele, wiederholbare Prozesse.

AUFGABE:
Erstelle einen **Leitfaden** inklusive einer **Interview-Roadmap** für Unternehmer-Interviews, basierend auf den Variablen unten.
Der Leitfaden soll so präzise sein, dass ein Team (Agentur + Kunde) ihn ohne Rückfragen umsetzen kann.

WICHTIGE RAHMENREGELN:
- Schreibe auf {{LANGUAGE}} in professioneller, klarer Unternehmens-Tonalität.
- Keine Floskeln, kein Buzzword-Overkill. Konkrete Deliverables.
- Wenn Informationen fehlen, **mache plausible Annahmen** und markiere sie als "Annahme".
- Liefere **mindestens 3 unterschiedliche Interview-Arc-Optionen** (z. B. "Gründerstory", "Fachautorität", "Kontroverse/These").
- Halte die Struktur **modular** (Bausteine), damit sie skalierbar für Serien ist.
- Integriere **Pre-Production, Production, Post-Production, Distribution**.
- Beachte Datenschutz/Einwilligungen (z. B. Release-Formular) und Plattform-Richtlinien.
- Alles in **Word**, mit klaren Überschriften, Tabellen und Checklisten.

---

### 1) Variablen (User-Input / Platzhalter)

{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_BRAND}} = "Beispiel GmbH"
{{INDUSTRY}} = "z. B. SaaS, Handwerk, E-Commerce, Beratung"
{{REGION}} = "DACH"
{{INTERVIEW_GOAL}} = "z. B. Thought Leadership, Recruiting, Leadgen, Kundenbindung"
{{TARGET_AUDIENCE}} = "z. B. Entscheider (IT/Operations), Gründer, KMU"
{{PRIMARY_OFFER}} = "z. B. Beratungspaket, SaaS-Abo, Produktlinie"
{{UNIQUE_ANGLE}} = "z. B. ungewöhnliche These, besonderer Lebensweg, neue Methode"
{{FORMAT}} = "Podcast | YouTube | LinkedIn Live | Event-Panel | Blog-Interview"
{{DURATION_MIN}} = 30
{{INTERVIEW_STYLE}} = "locker | journalistisch | deep-dive | provokant | coaching"
{{TONE}} = "professionell, klar, leicht nerdig"
{{SENSITIVITIES}} = "z. B. keine Umsatzzahlen, keine Kundennamen, keine internen Details"
{{CALL_TO_ACTION}} = "z. B. Newsletter, Demo buchen, Erstgespräch, Lead Magnet"
{{CONTENT_REPURPOSING_LEVEL}} = "low | medium | high"
{{TEAM_SETUP}} = "z. B. 1 Host, 1 Cutter, 1 Social Manager"
{{TIME_BUDGET_HOURS}} = 10
{{TOOLS}} = "z. B. Riverside, Zoom, Descript, Adobe, CapCut, Notion"
{{LANGUAGE}} = "Deutsch"

---

### 2) Output-Format (du MUSST genau diese Struktur liefern)

1. **Executive Summary (1 Seite)**
   - Ziel, Zielgruppe, Positionierung, Kernbotschaft, CTA, erwarteter Business-Impact
2. **Interview-Strategie**
   - Messaging House (3–5 Kernbotschaften + Proof Points)
   - Hook-Frameworks (mind. 10 Hooks)
   - Tonalität & Rollen (Host, Gast, Producer)
3. **Interview-Roadmap (End-to-End Prozess)**
   - Phase A: Pre-Production (Briefing, Recherche, Freigaben, Technik, Agenda)
   - Phase B: Production (Ablaufplan Minute 0–{{DURATION_MIN}}, Moderations-Spickzettel)
   - Phase C: Post-Production (Schnitt, Fact-Check, Freigabe, SEO, Kapitelmarken)
   - Phase D: Distribution (Plattformplan + Posting-Rhythmus)
4. **Fragenkatalog als Baukasten**
   - 5 Kategorien à 8–12 Fragen (insgesamt mind. 40)
   - Pro Kategorie: Ziel der Fragen + "Follow-up"-Fragen + No-Go-Fragen
   - Inkl. 10 "Story-trigger"-Fragen und 10 "Proof/Case"-Fragen
5. **3 Interview-Arcs (Storylines)**
   - Arc 1: Gründer-/Origin-Story
   - Arc 2: Fachautorität / Deep Dive
   - Arc 3: Kontroverse These / Myth-Busting
   - Für jeden Arc: Dramaturgie, Spannungsbogen, Schlüsselfragen, mögliche Titel
6. **Skript-Bausteine**
   - Intro/Outro-Templates (je 3 Varianten)
   - Übergänge/Brücken (mind. 12 Sätze)
   - Einwand-Handling (z. B. "Das kann ich nicht sagen" → elegante Alternativen)
7. **Recht, Compliance & Risikomanagement**
   - Checkliste Einwilligung/Release, Datenschutz, Marken-/Kundennamen
   - Sensitivitäten aus {{SENSITIVITIES}} konkret in Regeln übersetzen
8. **Assets & Repurposing-Plan**
   - Pro Episode: 1 Longform + 6–12 Shortform + 1 Carousel + 1 Newsletter
   - Content-Matrix (Thema × Format × Kanal × CTA)
   - Wenn {{CONTENT_REPURPOSING_LEVEL}} = high: zusätzlich 3 Lead Magnets vorschlagen
9. **Messsystem (KPI/OKR)**
   - 10 KPIs (Awareness, Engagement, Leads, Pipeline)
   - Tracking-Setup + wöchentlicher Review-Rhythmus
10. **Projektplan & Verantwortlichkeiten**
   - RACI-Matrix (Agentur vs. Kunde)
   - Timeline (T-14 bis T+7) als Tabelle
   - Quality Gates (Abnahmekriterien) für jede Phase
11. **Finale Checklisten**
   - Pre-Call, Recording-Day, Post-Editing, Publishing, Nachfass
12. **Appendix**
   - Beispiel-Episodentitel (mind. 20)
   - Beispiel-Thumbnails/Hooklines (mind. 15)
   - Beispiel-LinkedIn-Post-Text (1 Muster)

---

### 3) Qualitätskriterien (du MUSST erfüllen)

- Konkrete, umsetzbare Schritte (keine Theorie-only Antworten)
- Jede Phase hat: Input → Schritte → Output → Owner → QA-Kriterien
- Fragen sind **nicht generisch**: sie müssen auf {{INDUSTRY}}, {{PRIMARY_OFFER}}, {{TARGET_AUDIENCE}}, {{UNIQUE_ANGLE}} passen
- Der Leitfaden ist skalierbar für eine **Serienproduktion** (mind. 6 Episoden)
- Der Ton bleibt: {{TONE}}
- Output ist vollständig in Word, sauber formatiert, mit Tabellen & Checklisten

---

### 4) Kontext (optional, falls vorhanden)

- Bestehende Kanäle & Reichweite: {{CURRENT_CHANNELS_AND_METRICS}}
- Brand Guidelines / CI: {{BRAND_GUIDELINES}}
- Wettbewerber / Benchmarks: {{COMPETITORS}}
- Themenverbote: {{TOPIC_EXCLUSIONS}}

---

JETZT LIEFERN:
Erzeuge den Leitfaden gemäß Struktur 1–12. Starte mit Executive Summary und arbeite dann durch.
```

---

## Hinweise zur Nutzung (kurz)

- Fülle die Variablen aus, besonders **Ziel**, **Zielgruppe**, **Angebot** und **Unique Angle**.
- Für Serien: Kopiere Abschnitt "Interview-Arcs" + "Fragenkatalog" und erstelle pro Episode ein eigenes Briefing.