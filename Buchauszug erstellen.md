> **Zweck:** Dieser Prompt erzeugt einen **professionellen Leitfaden** (Guideline), wie aus einem bestehenden Buch ein **zielgerichteter Auszug** erstellt wird – inkl. Struktur, Stilregeln, Qualitätskriterien, Compliance-Hinweisen und konkreten Arbeitsschritten.  
> **Einsatzkontext:** Marketing-/Content-Agentur (Strategie + Redaktion + Publishing).

---

## 1) Copy-&-Paste Prompt (mit Variablen)

### A) Variablenblock (User-Input)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Content-Agentur (Strategie, Redaktion, Publishing)"
{{PROJECT_NAME}} = "Buchauszug-erstellen"
{{BOOK_TITLE}} = "<<<BUCHTITEL>>>"
{{BOOK_GENRE}} = "Sachbuch | Ratgeber | Business | Roman | ..."

{{AUTHOR_VOICE}} = "nüchtern & kompetent | erzählerisch & bildhaft | humorvoll | wissenschaftlich | ..."
{{TARGET_AUDIENCE}} = "<<<ZIELGRUPPE>>>"
{{AUDIENCE_KNOWLEDGE_LEVEL}} = "Einsteiger | Fortgeschritten | Experten"
{{CORE_PROMISE}} = "<<<KERNNUTZEN / TRANSFORMATION>>>"
{{PRIMARY_GOAL}} = "Lead-Magnet | PR/Media | Buchverkauf | Newsletter-Onboarding | Webinar-Teaser | ..."

{{EXCERPT_TYPE}} = "Kapitel-Auszug | thematischer Auszug | Best-of-Kernaussagen | Fallstudie | Prolog | ..."

{{EXCERPT_LENGTH_WORDS}} = 1200
{{LANGUAGE}} = "Deutsch"
{{TONE}} = "Corporate, klar, keine Buzzword-Orgie, vertrauenswürdig"
{{READABILITY}} = "leicht | mittel | anspruchsvoll"
{{FORMALITY}} = "Sie | Du"

{{KEY_CONCEPTS}} = ["<<<Begriff 1>>>", "<<<Begriff 2>>>", "<<<Begriff 3>>>"]
{{MUST_INCLUDE_SECTIONS}} = ["Hook", "Kontext", "Kernidee", "Beispiel/Case", "Takeaways", "CTA"]
{{MUST_AVOID}} = ["Füllwörter", "abgedroschene Phrasen", "Übertreibungen", "unbelegte Behauptungen"]

{{BRAND_TERMS}} = ["<<<Markenbegriff/Produkt>>>", "<<<Slogan>>>"]
{{CTA_TEXT}} = "<<<CALL-TO-ACTION>>>"
{{CTA_URL}} = "<<<LINK>>>"

{{LEGAL_COMPLIANCE}} = [
  "Keine medizinischen/finanziellen/rechtlichen Versprechen ohne Disclaimer",
  "Keine personenbezogenen Daten",
  "Keine diffamierenden Aussagen",
  "Urheberrecht beachten: Auszug muss aus freigegebenem Material stammen"
]

{{SOURCE_INPUT}} = "<<<HIER BUCHTEXT ODER KAPITEL EINFÜGEN (oder Zusammenfassung + Kapitelstruktur)>>>"
{{OPTIONAL_CONTEXT}} = "<<<Markt-/Wettbewerbskontext, Positionierung, Kampagnenziel, Kanal, Deadline>>>"
```

---

### B) Master-Prompt (an das Modell)

```text
Du agierst als Senior Editorial Director + Content Strategist in {{AGENCY_NAME}} ({{AGENCY_ROLE}}).
Dein Auftrag: Erstelle einen detaillierten, hochwertigen Buchauszug zu {{BOOK_TITLE}}, der {{PRIMARY_GOAL}} optimal unterstützt.

WICHTIG:
- Arbeite strikt mit den Variablen. Wenn Informationen fehlen, markiere sie als [OFFEN] und liefere Annahmen nur als "Hypothese".
- Halte die Tonalität: {{TONE}}. Sprache: {{LANGUAGE}}. Anrede: {{FORMALITY}}.
- Keine Halluzinationen: Keine Zitate/Quellen/Behauptungen erfinden. Wenn etwas nicht belegt ist, kennzeichne es.
- Urheberrecht & Compliance: Berücksichtige {{LEGAL_COMPLIANCE}}. Ergänze notwendige Disclaimer.
- Ergebnis muss als "Guideline" nutzbar sein: konkret, checklistenfähig, mit Qualitätsgates.

INPUT (Buchmaterial / Kontext):
{{SOURCE_INPUT}}
Zusatzkontext:
{{OPTIONAL_CONTEXT}}

AUFGABENPAKET:
1) Zieldefinition & Positionierung
   - Definiere Zielgruppe ({{TARGET_AUDIENCE}}) inkl. Wissensstand ({{AUDIENCE_KNOWLEDGE_LEVEL}}) und Job-to-be-done.
   - Formuliere das Nutzenversprechen ({{CORE_PROMISE}}) und das Kommunikationsziel ({{PRIMARY_GOAL}}).
   - Definiere Erfolgskriterien (KPIs) passend zum Ziel (z. B. Conversion, Newsletter-Signups, Verweildauer).

2) Auszug-Strategie
   - Empfiehl eine Auszugslogik passend zu {{EXCERPT_TYPE}} und {{EXCERPT_LENGTH_WORDS}} Wörtern.
   - Lege ein "Redaktions-Briefing" fest: Fokus, Kernbotschaften, No-Go’s ({{MUST_AVOID}}), Pflichtsektionen ({{MUST_INCLUDE_SECTIONS}}).
   - Definiere die Informationshierarchie: Was MUSS in den Auszug, was ist optional, was raus.

3) Struktur & Outline (lieferbar als Blueprint)
   - Erstelle eine klare Outline mit Überschriften (H2/H3) und geschätzter Wortverteilung.
   - Baue {{KEY_CONCEPTS}} sinnvoll ein und nutze {{BRAND_TERMS}} nur dort, wo es organisch passt.
   - Definiere Übergänge und "Retention-Hooks" (Micro-Teaser), ohne Clickbait.

4) Stil- und Sprachregeln (Style Guide)
   - Stimme den Stil auf {{AUTHOR_VOICE}}, {{READABILITY}}, {{FORMALITY}} ab.
   - Gib klare Regeln: Satzlänge, Fachbegriffe erklären, aktive Verben, Beispiele, Metaphern (falls passend), Konsistenzregeln.
   - Lege ein Glossar-Muster an (Begriff → Kurzdefinition → ggf. Beispiel).

5) Redaktioneller Workflow (Operating Model)
   - Beschreibe den Schritt-für-Schritt Prozess: Auswahl → Kürzung → Verdichtung → Rewriting → Fact-Check → Lektorat → Final QA.
   - Definiere Rollen & Verantwortlichkeiten (z. B. Strateg:in, Redakteur:in, Lektor:in, Legal/Compliance).
   - Definiere Quality Gates: Was muss nach jedem Schritt erfüllt sein (inkl. Checkliste).

6) Qualitätssicherung & Risiko-Management
   - Erstelle eine Prüfliste: Logik, Lesefluss, Mehrwert, Konsistenz, Tonalität, rechtliche Risiken, unbewiesene Aussagen.
   - Ergänze "Red Flags" (typische Fehler) und konkrete Korrekturmaßnahmen.
   - Füge notwendige Disclaimer-Vorlagen hinzu (z. B. keine Rechtsberatung).

7) Output-Templates (sofort nutzbar)
   - Liefere: (a) Redaktionsbriefing-Template, (b) Outline-Template, (c) QA-Checklist, (d) CTA-Block.
   - Der CTA muss {{CTA_TEXT}} und {{CTA_URL}} enthalten, in {{TONE}} formuliert.

AUSGABEFORMAT (strikt einhalten):
- Titel: "Buchauszug für {{BOOK_TITLE}}"
- Abschnitt 1–7 gemäß oben (mit klaren Überschriften)
- Jede Checkliste als Excel-Checkbox-Liste
- Am Ende: "Kurzversion (1 Seite)": eine komprimierte Executive Summary des Leitfadens.
```

---

## 2) Best Practices (für maximale Output-Qualität)

- **Input-Qualität skaliert Output-Qualität:** Liefere idealerweise Kapitelstruktur + Ziel + 1–2 Beispielpassagen (Ton & Stil).
- **Wortbudget erzwingt Priorisierung:** Wenn {{EXCERPT_LENGTH_WORDS}} klein ist, Fokus auf **eine** Kernidee statt "Alles drin".
- **Compliance als Quality Gate:** Behauptungen, die nach "Garantie" klingen, konsequent entschärfen oder mit Disclaimer versehen.
- **Lesefluss = Conversion:** Klarer roter Faden + erkennbare Takeaways + CTA, der logisch aus dem Text folgt.

---

## 3) Optional: Mini-Add-on Prompt (wenn du direkt den Auszug generieren willst)

> Nutze diesen Add-on Prompt **nachdem** der Leitfaden steht, um den eigentlichen Auszug zu schreiben.

```text
Erstelle auf Basis des Leitfadens den finalen Buchauszug ({{EXCERPT_LENGTH_WORDS}} Wörter) zu {{BOOK_TITLE}}.
Halte {{AUTHOR_VOICE}}, {{TONE}}, {{FORMALITY}}, {{READABILITY}} ein.
Nutze die Outline und erfülle alle Quality Gates.
Am Ende: Takeaways (3–5 Bulletpoints) + CTA mit {{CTA_TEXT}} und {{CTA_URL}}.
Inputmaterial:
{{SOURCE_INPUT}}
```
