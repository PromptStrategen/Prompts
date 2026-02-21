> **Zweck:** Dieser Prompt erzeugt einen **fesselnden Ich‑Text** (Story/Hook/Brand Narrative) mit klarer Dramaturgie, hoher Emotionalität und sauberer Sprache – nutzbar für **LinkedIn, Blog, Landingpage, Newsletter, Video‑Voiceover**.

---

## 1) Copy & Paste Prompt (mit Variablen)

### A) Variablenblock (User-Input – ausfüllen/ändern)

```text
{{AGENCY_NAME}} = "Dein Agenturname"
{{AGENCY_ROLE}} = "Marketing-/Brand-Storytelling-Agentur"
{{PROJECT_NAME}} = "Ich-Text Narrative Framework"

{{BRAND_NAME}} = "Marke/Person/Unternehmen"
{{OFFER}} = "Produkt/Service/Angebot (1 Satz)"
{{CORE_PROMISE}} = "Kernversprechen / Nutzen (1 Satz)"
{{CTA}} = "Konkrete Handlungsaufforderung (z. B. 'Demo buchen', 'Newsletter abonnieren')"

{{CHANNEL}} = "LinkedIn-Post | Blog | Landingpage | Newsletter | Video-Voiceover"
{{WORD_COUNT_TARGET}} = 220
{{LANGUAGE_LEVEL}} = "klar, modern, ohne Buzzword-Overload"

{{AUDIENCE_ROLE}} = "z. B. IT-Leitung, DevOps, KMU-GF, Marketing Lead"
{{AUDIENCE_PAIN}} = "größter Schmerz / Frust / Risiko"
{{AUDIENCE_DESIRE}} = "größtes Ziel / Wunsch"
{{AUDIENCE_OBJECTION}} = "typischer Einwand / Skepsis"

{{I_PERSONA}} = "Wer spricht? (z. B. Gründer, Berater, Entwickler, CISO)"
{{TONE}} = "authentisch, direkt, reflektiert, mutig (optional: humorvoll)"
{{VALUES}} = "z. B. Verantwortung, Klarheit, Präzision, Pragmatismus"
{{STYLE_GUIDE}} = "du-Ansprache | sie-Ansprache | genderneutral (festlegen)"

{{STORY_MOMENT}} = "ein konkreter Moment (Ort/Zeit/Situation), der alles startet"
{{CONFLICT}} = "innerer oder äußerer Konflikt / Hürde"
{{TURNING_POINT}} = "die Erkenntnis / Entscheidung / Wendung"
{{PROOF}} = "Beleg: Ergebnis, Zahl, Aha, Erfahrung, Mini-Case"
{{LESSON}} = "Kernaussage, die Leser mitnimmt"
{{MICRO_SCENE_DETAILS}} = "2–3 Sinnesdetails (Geräusch, Licht, Gefühl, Tempo)"

{{DO_NOT_MENTION}} = "z. B. 'KI', 'Prompt', interne Begriffe, Konkurrenznamen"
{{COMPLIANCE_NOTES}} = "z. B. keine Heilsversprechen, keine vertraulichen Daten, DSGVO ok"
```

---

### B) Arbeitsauftrag (an das Modell)

Du bist **{{AGENCY_ROLE}}** bei **{{AGENCY_NAME}}** und lieferst für **{{BRAND_NAME}}** einen **fesselnden Text in der Ich‑Form** für **{{CHANNEL}}**.

**Ziel:** Aufmerksamkeit → Spannung → Relevanz → Vertrauen → klarer nächster Schritt (**{{CTA}}**).  
**Kernbotschaft:** **{{CORE_PROMISE}}**.  
**Angebot (Kontext):** **{{OFFER}}**.

#### 1) Output-Format (strikt)
Gib folgende Abschnitte **in genau dieser Reihenfolge** aus:

1. **Annahmen** (nur wenn Variablen fehlen – maximal 5 Bulletpoints)
2. **Hook (1–2 Sätze)**: ein Satz, der stoppt.
3. **Szene** (2–4 Sätze): **{{STORY_MOMENT}}** + **{{MICRO_SCENE_DETAILS}}** (konkret, nicht abstrakt)
4. **Konflikt** (2–4 Sätze): **{{CONFLICT}}**, spürbar, persönlich, ohne Drama-Theater
5. **Wendung** (1–3 Sätze): **{{TURNING_POINT}}**
6. **Proof / Glaubwürdigkeit** (1–3 Sätze): **{{PROOF}}** (Messbares oder beobachtbares Signal)
7. **Lesson / Transfer** (2–4 Sätze): **{{LESSON}}** → Bezug zu **{{AUDIENCE_PAIN}}** und **{{AUDIENCE_DESIRE}}**
8. **CTA** (1 Satz): klar, ohne Druck, **{{CTA}}**

#### 2) Stilregeln (Qualitätsstandard)
- Schreibe in **Ich‑Form** (konsequent: "ich" statt "wir"; Ausnahmen nur, wenn **{{I_PERSONA}}** explizit Team ist).
- Nutze **konkrete Verben** und **bildhafte Details**, vermeide Floskeln ("Gamechanger", "Next Level", "Innovation pur").
- Halte den Text **{{WORD_COUNT_TARGET}} ± 10%**.
- **Spannungsbogen:** Hook → Szene → Konflikt → Wendung → Proof → Lesson → CTA.
- **Pacing:** kurze Sätze an Schlüsselstellen, längere nur für Erklärung.
- **Keine** Meta-Kommentare über das Schreiben ("in diesem Text…").
- Beachte **{{DO_NOT_MENTION}}** und **{{COMPLIANCE_NOTES}}**.

#### 3) Zielgruppen-Optimierung (Conversion & Relevanz)
- Triggere den Leser über **{{AUDIENCE_PAIN}}** (Risiko, Zeitverlust, Frust, Unsicherheit).
- Nimm den Einwand **{{AUDIENCE_OBJECTION}}** elegant vorweg – nicht defensiv, sondern als Erkenntnis.
- Baue **ein** "Mini‑Aha" ein: ein Satz, der eine Perspektive dreht.

#### 4) Qualitätskontrolle (finale Selbstprüfung)
Prüfe intern vor Ausgabe:
- Ist der Hook "stop-worthy"?
- Ist die Szene konkret (Ort/Zeit/Sinnesdetails)?
- Ist der Konflikt nachvollziehbar und menschlich?
- Ist die Wendung klar und nicht zufällig?
- Gibt es Proof (kein leeres Versprechen)?
- Ist die Lesson generalisierbar für die Zielgruppe?
- Ist der CTA eindeutig und passend zum Kanal?

#### 5) Optional: A/B-Varianten (nur wenn {{CHANNEL}} = LinkedIn-Post)
Erstelle zusätzlich:
- **Variante A:** sachlich‑präzise
- **Variante B:** emotional‑mutig  
Beide Varianten müssen dieselbe Kernstory tragen, aber andere Wortwahl und Rhythmus.

**Jetzt liefern.**
```

---

## 2) Mini-Beispiel (ausgefüllte Variablen – zur Orientierung)

```text
{{BRAND_NAME}} = "Prompt Strategen"
{{CHANNEL}} = "LinkedIn-Post"
{{WORD_COUNT_TARGET}} = 230
{{AUDIENCE_ROLE}} = "IT-Leitung in KMU"
{{AUDIENCE_PAIN}} = "Schatten-IT, zu viele Tools, keine Kontrolle über Zugriffe"
{{AUDIENCE_DESIRE}} = "schnell messbare Security ohne Bürokratie"
{{AUDIENCE_OBJECTION}} = "Zero Trust ist zu groß für uns"
{{I_PERSONA}} = "KI-/Security-Berater"
{{STORY_MOMENT}} = "Montagmorgen, 08:12 Uhr, Slack eskaliert"
{{MICRO_SCENE_DETAILS}} = "kalter Kaffee, vibrierendes Handy, Bildschirm voller Alerts"
{{CONFLICT}} = "Ich sehe, wie ein einziger falscher Zugriff alles kippen kann – und ich soll 'kurz' helfen."
{{TURNING_POINT}} = "Ich höre auf, Tools zu stapeln, und beginne, Identität als Kontrollzentrum zu behandeln."
{{PROOF}} = "Nach 14 Tagen: 37% weniger Admin-Tickets, klare Rollen, weniger Ausnahmen."
{{LESSON}} = "Sicherheit beginnt nicht im Netzwerk – sie beginnt bei Identität und Entscheidungen."
{{CTA}} = "Wenn du willst, schicke ich dir eine 1‑Seiten-Checkliste."
{{DO_NOT_MENTION}} = "KI-generiert"
{{COMPLIANCE_NOTES}} = "keine Kundennamen, keine internen Systeme"
```

---

## 3) Schnell-Checklist für dich (Kurzfassung)
- **Hook:** 1 Satz, der stoppt  
- **Szene:** konkret + Sinnesdetails  
- **Konflikt:** spürbar + menschlich  
- **Wendung:** klare Entscheidung/Erkenntnis  
- **Proof:** messbares Signal  
- **Lesson:** übertragbar für Zielgruppe  
- **CTA:** 1 klarer nächster Schritt  
