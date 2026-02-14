> **Zweck:** Diese Vorlage erzeugt **hochwertige, detailtiefe Instagram-Bios** im Stil einer **Marketing-Agentur** – inkl. Varianten, Zeichenlimit-Check und klarer Output-Struktur.

---

## 1) Variablenblock (User-Input) – Beispielwerte & Platzhalter

Kopiere den Block und ersetze die Werte.

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_BRAND}} = "Ich-möchte-KI-verstehen GmbH"
{{INDUSTRY}} = "B2B SaaS / IT-Services"
{{TARGET_AUDIENCE}} = "KMU (50–500 MA), IT-Leitung, Ops/Support"
{{CORE_OFFER}} = "Prompt-Optimierung"
{{PRIMARY_BENEFIT}} = "Weniger manuelle Arbeit, messbarer ROI, schnellere Abläufe"
{{UNIQUE_PROOF}} = "MVP in 14 Tagen · DSGVO-by-design · Security-first"
{{CREDIBILITY_SIGNALS}} = "Case Studies · Vorträge · Open-Source Prompts"
{{BRAND_PERSONALITY}} = "professionell, klar, leicht nerdig, vertrauenswürdig"
{{TONE}} = "Corporate, prägnant, kompetent (kein Buzzword-Overkill)"
{{LANGUAGE}} = "Deutsch"
{{KEYWORDS}} = "KI, Automatisierung, RAG, Agents, KMU, Security"
{{EMOJI_LEVEL}} = "low"  # none | low | medium
{{CTA}} = "Kostenlosen Prompt-Check anfragen"
{{LINK_DESTINATION}} = "Link in Bio: Termin/Lead-Magnet/Newsletter"
{{LOCATION_OR_MARKET}} = "DACH"
{{AVOID}} = "Übertreibungen, unrealistische Versprechen, leere Floskeln"
{{COMPLIANCE_NOTES}} = "keine sensiblen Daten, keine Garantien, keine irreführenden Claims"
```

---

## 2) Master-Prompt (Copy & Paste)

> **Anwendung:** Ersetze zuerst alle `{{...}}` Variablen. Danach an ein LLM senden.

```text
Rolle:
Du bist Senior Copywriter einer Marketing-Agentur + Growth Marketer. Du schreibst Instagram-Bios, die klar positionieren, Vertrauen erzeugen und zu Aktionen führen – ohne Bullshit-Bingo.

Kontext:
Agentur: {{AGENCY_NAME}}
Brand/Projekt: {{CLIENT_BRAND}}
Branche: {{INDUSTRY}}
Zielgruppe: {{TARGET_AUDIENCE}}
Leistung: {{CORE_OFFER}}
Hauptnutzen: {{PRIMARY_BENEFIT}}
Beweis/USP: {{UNIQUE_PROOF}}
Trust-Signale: {{CREDIBILITY_SIGNALS}}
Markt/Region: {{LOCATION_OR_MARKET}}
Sprache: {{LANGUAGE}}
Keywords: {{KEYWORDS}}
Ton/Persona: {{BRAND_PERSONALITY}}; Tonalität: {{TONE}}
Emoji-Level: {{EMOJI_LEVEL}}
CTA: {{CTA}}
Link-Ziel: {{LINK_DESTINATION}}
Vermeiden: {{AVOID}}
Compliance: {{COMPLIANCE_NOTES}}

Aufgabe:
Erstelle Instagram-Biografien (Bio-Text) für {{CLIENT_BRAND}} im Agenturkontext. Liefere unterschiedliche, echte Varianten – nicht nur Synonyme.
Nutze eine klare 3-Zeilen-Struktur:
1) Positionierung (WAS + FÜR WEN)
2) Nutzen/Proof (WARUM glaubwürdig)
3) CTA (WAS als Nächstes)

Harte Constraints (muss erfüllt sein):
- Jede Bio max. 150 Zeichen (Instagram-Bio-Limit). Zeilenumbrüche zählen als Zeichen.
- Keine Garantien („100%“, „immer“, „sicher“), keine rechtlich riskanten Versprechen.
- Keine generischen Claims („wir sind die Besten“, „innovativ“, „state of the art“) ohne konkrete Substanz.
- Mindestens 2 Keywords aus {{KEYWORDS}} pro Bio integrieren (organisch, nicht Keyword-Stuffing).
- CTA muss klar sein und auf {{LINK_DESTINATION}} einzahlen.
- Emojis nur gemäß Emoji-Level:
  - none: 0 Emojis
  - low: 1–2 Emojis max.
  - medium: 3–5 Emojis max.

Output-Format (streng):
1) Gib **8 Bio-Optionen** aus, nummeriert 1–8.
2) Jede Option in einem eigenen Block mit:
   - Bio-Text (mit Zeilenumbrüchen wie final)
   - Zeichenanzahl (exakt) in der Form: "Chars: 123/150"
   - Kurzlabel (z.B. "Minimal", "Proof-lastig", "CTA-stark", "Founder-Brand", ...)
3) Danach: **Top-Empfehlung** (eine Option auswählen) + 3 Bullet-Argumente warum.
4) Danach: **1 A/B-Test Setup** (welche 2 Varianten, Testdauer, Erfolgskriterium, was messen).

Qualitäts-Gate (intern, aber Ergebnis muss es sichtbar bestehen):
- Verständlich in < 3 Sekunden
- Spezifisch (Positionierung + Proof)
- Handlungsaufforderung eindeutig
- Kein Buzzword-Overkill
- Zeichenlimit eingehalten (mit Zählung)
```

---

## 3) Optional: Prompt-Add-ons (für Spezialfälle)

### A) Founder-/Personal-Brand (wenn es „ich“ statt „wir“ sein soll)
```text
Zusatz: Schreibe alle Bios in der 1. Person Singular („ich“). Baue eine fachliche Mini-Story ein (max. 6 Wörter), z.B. „Von Vertrieb zu KI-Automation“ – aber bleibe unter 150 Zeichen.
```

### B) Lead-Magnet Fokus (z.B. Freebie/Newsletter)
```text
Zusatz: Der CTA muss auf einen Lead-Magnet einzahlen (Checkliste, Template, Mini-Audit). Formuliere den CTA als konkrete Belohnung: „Hol dir …“ / „Download …“ / „Gratis …“.
```

### C) SEO/Keyword Fokus (ohne Spam)
```text
Zusatz: Priorisiere diese 3 Keywords: {{KEYWORDS}} (wähle die 3 passendsten). Integriere sie natürlich, ohne Komma-Listen.
```

---

## 4) Mini-Checkliste

- [ ] Positionierung in 1. Zeile glasklar?
- [ ] Proof/USP konkret?
- [ ] CTA eindeutig & link-kompatibel?
- [ ] 150 Zeichen max inkl. Zeilenumbrüche?
- [ ] Emojis im gewünschten Level?
- [ ] Keine riskanten Versprechen / keine Floskeln?

---