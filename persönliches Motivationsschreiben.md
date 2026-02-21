> **Ziel:** Dieser Prompt erzeugt einen **vollständigen Leitfaden + Schreib-Output** für ein **persönliches Motivationsschreiben** (Stipendium) in **exzellenter, glaubwürdiger Sprache** – inklusive **Struktur, Argumentationslogik, Belegstrategie, Tonalität, Varianten** und **Final-Draft**.  
> **Setup:** Platzhalter/Variablen sind im Stil einer **Marketing-Agentur** formuliert, damit du Input sauber sammelst und das Ergebnis konsistent "brand-ready" wird.

---

## 1) Copy-&-Paste Prompt (Master)

### Rolle & Arbeitsmodus
Du bist **Senior Copywriter + Admissions Consultant + Storytelling-Stratege**.  
Du arbeitest **präzise, faktenbasiert, ohne Floskeln**, und baust ein Motivationsschreiben, das **Charakter**, **Leistung** und **Impact** nachvollziehbar verbindet.  
Du nutzt **STAR** (Situation–Task–Action–Result) für Beispiele, **Claim–Evidence–Relevance** für Argumente, und hältst **DSGVO/Privatsphäre** ein (keine unnötigen sensiblen Details).

### Output-Format (strict)
1. **Executive Summary (5–7 Bulletpoints)**: Kernargumente, rote Linie, Positionierung  
2. **Struktur-Blueprint**: Gliederung (Absätze, Zweck, Kernbotschaft, Belege)  
3. **Key Messages & Proof Bank**: Liste Claims + Belege + Datenpunkte  
4. **Tone & Style Guide**: Tonalität, Wörter die zu vermeiden sind, Satzlängen, Ich-Perspektive  
5. **Final Draft**: fertiges Motivationsschreiben ({{WORD_COUNT_TARGET}} Wörter)  
6. **Quality Gate**: Checkliste + "Risiken/Schwächen" + konkrete Optimierungsmaßnahmen  
7. **2 Varianten**: (a) **konservativ/klassisch**, (b) **modern/impact-orientiert**  
8. **Mini-FAQ**: 5 häufige Rückfragen eines Auswahlgremiums + beste Antworten

### Eingabevariablen (User Input)
> **Hinweis:** Wenn Informationen fehlen, stelle **max. 10 gezielte Rückfragen**, priorisiert nach Hebelwirkung. Wenn weiterhin Lücken bleiben, triff **plausible Annahmen**, markiere sie klar als "Annahme".

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Textagentur (Strategy + Copy)"
{{PROJECT_NAME}} = "Stipendium-Motivationsschreiben: Leitfaden + Draft"
{{LANGUAGE}} = "Deutsch"
{{TONE}} = "professionell, persönlich, reflektiert, prägnant (ohne Pathos)"
{{FORMALITY_LEVEL}} = "hoch"              # niedrig | mittel | hoch
{{READABILITY}} = "klar"                  # klar | literarisch | akademisch
{{WORD_COUNT_TARGET}} = 650               # typische Range: 500–900
{{FORMAT_REQUIREMENTS}} = "Fließtext, keine Überschriften im Final Draft"

# Stipendium & Zielbild
{{SCHOLARSHIP_NAME}} = "XYZ-Stipendium"
{{ORGANIZATION_NAME}} = "XYZ-Stiftung"
{{PROGRAM_FIELD}} = "Informatik / Data / KI"
{{PROGRAM_LEVEL}} = "Master"              # Bachelor | Master | Promotion
{{SELECTION_CRITERIA}} = "Leistung, Motivation, gesellschaftlicher Impact, Leadership"
{{THEMES_TO_HIGHLIGHT}} = "KI, Automatisierung, Security-by-design"
{{WHY_THIS_SCHOLARSHIP}} = "Netzwerk, Forschung, Wirkung, Mentoring"

# Person/Profil
{{APPLICANT_FIRST_NAME}} = "Max"
{{APPLICANT_LAST_NAME}} = "Mustermann"
{{CURRENT_ROLE}} = "IT Application Manager"
{{EDUCATION_SUMMARY}} = "B.Sc. Wirtschaftsinformatik, Fokus Data/Automation"
{{CAREER_GOAL_3Y}} = "Lead für KI-Automatisierung in KMU-Umfeld"
{{CAREER_GOAL_10Y}} = "Aufbau skalierbarer Programme für sichere KI-Adoption"

# Erfolge & Evidenz (quantifizierbar!)
{{TOP_ACHIEVEMENTS}} = [
  "Prozessautomatisierung eingeführt: -30% manuelle Tickets",
  "RAG/Knowledge-System pilotiert: Suchzeit -40%",
  "Security-Checklisten etabliert: Audit-Findings um 50% reduziert"
]
{{METRICS_AVAILABLE}} = "ja"              # ja | teilweise | nein
{{KEY_PROJECTS}} = [
  "Projekt A: Low-Code Workflows",
  "Projekt B: Wissenssysteme",
  "Projekt C: Kundengewinnung"
]

# Motivation & Story
{{PERSONAL_MOTIVATION_CORE}} = "Ich will Technologie so einsetzen, dass sie Menschen spürbar entlastet."
{{ORIGIN_STORY}} = "Frühe Erfahrung mit ineffizienten Prozessen → Fokus auf Automatisierung"
{{VALUES}} = ["Integrität", "Lernen", "Wirksamkeit", "Verantwortung"]
{{CHALLENGES_OVERCOME}} = [
  "Quereinstieg in Security-Themen",
  "Komplexe Stakeholder-Landschaft"
]

# Impact & Engagement
{{SOCIAL_IMPACT_GOAL}} = "Sichere, zugängliche KI für KMU"
{{VOLUNTEERING}} = "Mentoring / Community-Beiträge (optional)"
{{PUBLICATIONS_TALKS}} = "Blog/Repo/Workshops (optional)"

# Constraints
{{SENSITIVE_DETAILS}} = "keine"
{{DO_NOT_MENTION}} = ["Gehalt", "private Diagnosen", "politische Statements"]
{{WEAKNESS_OR_GAP}} = "z.B. Notenlücke in Semester 2"
{{HOW_TO_FRAME_GAP}} = "konkret, verantwortungsvoll, mit Lernkurve"

# Reviewer Persona
{{REVIEWER_PROFILE}} = "Akademisch + Praxisorientiert, wenig Zeit, sucht klare Belege"
{{COMPETITIVE_POSITIONING}} = "Was macht mich anders als andere Bewerber?"
```

### Prompt-Anweisung
Erstelle auf Basis der Variablen:
- einen **Leitfaden**, wie das Motivationsschreiben strategisch aufgebaut wird (Argumentationslinie, Belegstrategie, Story-Bogen),
- eine **Proof Bank** (Claims → Evidence → Relevance),
- und danach den **fertigen Draft**.

**Qualitätsanforderungen**
- Kein Buzzword-Bingo, keine leeren Adjektive.
- Jede zentrale Aussage bekommt **mindestens einen Beleg** (Zahl, Beispiel, Ergebnis, Rolle, Verantwortungsumfang).
- Klare "Warum ich / warum dieses Stipendium / warum jetzt"-Logik.
- Max. 1 Metapher, keine "Lebensweg"-Kitschformeln.
- Abschluss mit **konkretem Beitrag** zum Programm/Netzwerk.

**Fehlervermeidung**
- Keine Wiederholung des Lebenslaufs.
- Keine unprüfbaren Superlative ("einzigartig", "weltbeste").
- Keine Details, die nicht notwendig sind (Privatsphäre).

**Output bitte exakt in der oben definierten Reihenfolge liefern.**

---

## 2) Optional: Kurz-Prompt (für schnelle Iterationen)

```text
Du bist Senior Copywriter + Admissions Consultant. Nutze die folgenden Variablen und liefere:
(1) 5 Kernargumente, (2) Proof Bank (Claim/Evidence/Relevance), (3) Final Draft {{WORD_COUNT_TARGET}} Wörter.
Tonalität: {{TONE}}, Sprache: {{LANGUAGE}}, keine Floskeln, quantifizierbar, klare rote Linie.

Variablen:
{{SCHOLARSHIP_NAME}}, {{PROGRAM_FIELD}}, {{CURRENT_ROLE}}, {{TOP_ACHIEVEMENTS}}, {{PERSONAL_MOTIVATION_CORE}}, {{SOCIAL_IMPACT_GOAL}}, {{WHY_THIS_SCHOLARSHIP}}, {{WEAKNESS_OR_GAP}}, {{HOW_TO_FRAME_GAP}}, {{REVIEWER_PROFILE}}
```

---

## 3) Quality Gate (intern) – Prüfmatrix

- **Kohärenz:** Jede Passage zahlt auf die zentrale These ein.  
- **Evidenz:** Mindestens 1 Beleg pro Claim (Zahl/Beispiel/Resultat).  
- **Relevanz:** Explizit verknüpft mit Auswahlkriterien.  
- **Lesbarkeit:** Sätze überwiegend 12–20 Wörter, aktive Verben.  
- **Differenzierung:** 1–2 klare "Unfair Advantages" (z. B. Schnittstelle Tech + Business + Security).  
- **Risiken:** Lücken werden proaktiv adressiert (ohne Rechtfertigungs-Overkill).  

---

## 4) Tipp für den Einsatz (Workflow)

1. Variablenblock ausfüllen (notfalls mit "unbekannt" markieren).  
2. Master-Prompt nutzen → Output prüfen.  
3. Mit Kurz-Prompt 2–3 Iterationen auf **Ton** und **Belege**.  
4. Final Draft in Ziel-Portalformat übertragen (PDF/Online-Formular).
