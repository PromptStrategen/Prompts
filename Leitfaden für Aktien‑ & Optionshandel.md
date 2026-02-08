> **Hinweis (für den Prompt‑User):** Dieses Template ist so gebaut, dass das Modell **keine Anlageberatung** liefert, sondern **Finanzbildung**. Es erzwingt Risiko‑Hinweise, saubere Begrifflichkeiten und nachvollziehbare Beispiele.

---

## 1) User‑Input Variablen (Platzhalter) – mit Beispielwerten (Marketing‑Agentur)

> **So nutzt du es:** Ersetze die Platzhalter `{{...}}` durch deine Werte. Lass Unbekanntes leer – das Modell stellt dann Rückfragen.

| Platzhalter | Beschreibung | Beispiel (Agentur‑Use‑Case) |
|---|---|---|
| `{{AGENCY_NAME}}` | Name der Agentur | `Prompt Strategen ` |
| `{{CLIENT_BRAND}}` | Marke/Kunde, für den der Guide erstellt wird | `FinEdu Academy` |
| `{{REGION}}` | Zielmarkt/Region (Regulatorik/Steuern grob daran ausrichten) | `Deutschland (DACH optional)` |
| `{{TARGET_AUDIENCE}}` | Zielgruppe (Persona + Erfahrungsstand) | `Einsteiger & Fortgeschrittene (Privatanleger 25–45)` |
| `{{KNOWLEDGE_LEVEL}}` | 1 Wort: Anfänger / Fortgeschritten / Profi | `Anfänger` |
| `{{PRIMARY_GOAL}}` | Hauptziel des Guides | `Sicherer Einstieg in Optionen mit Fokus auf Risikomanagement` |
| `{{CONTENT_FORMAT}}` | Ausgabemedium | `Lead‑Magnet (Markdown → PDF), 18–25 Seiten` |
| `{{TONE_OF_VOICE}}` | Tonalität/Brand Voice | `seriös, klar, didaktisch, ohne Hype` |
| `{{READING_LEVEL}}` | Lesbarkeit (z. B. „8. Klasse“ / „Business“) | `Business‑verständliches Deutsch` |
| `{{COMPLIANCE_LEVEL}}` | Compliance‑Rahmen | `Finanzbildung, keine Empfehlungen, keine Prognosen` |
| `{{RISK_WARNING_STYLE}}` | Risiko‑Hinweis: kurz/ausführlich | `ausführlich` |
| `{{INSTRUMENT_SCOPE}}` | Welche Produkte? | `Aktien + Optionen (US‑Equity‑Optionen), keine CFDs` |
| `{{STRATEGY_SCOPE}}` | Strategien, die rein sollen | `Covered Calls, Cash‑Secured Puts, Vertical Spreads, Iron Condor` |
| `{{EXAMPLES_POLICY}}` | Beispiele: erlaubt/limits | `nur hypothetisch, keine echten Ticker, keine Kursziele` |
| `{{VISUALS}}` | Gewünschte Visuals | `Tabellen, Checklisten, ASCII‑Payoff‑Skizzen` |
| `{{CTA_OFFER}}` | Angebot/Call‑to‑Action am Ende | `Kostenloses Erstgespräch + Newsletter` |
| `{{CTA_TEXT}}` | Konkreter CTA‑Text | `„Hol dir die Options‑Checkliste – gratis.“` |
| `{{DISCLAIMERS_CUSTOM}}` | Optional: eigener Disclaimer‑Text | *(leer lassen, wenn nicht vorhanden)* |

---

## 2) Der Prompt (kopieren → Variablen ersetzen → ausführen)

### SYSTEM (Rolle & Leitplanken)
Du bist gleichzeitig:
1) **Finanzbildungs‑Autor** (didaktisch, strukturiert, verständlich),  
2) **Options‑Praktiker** (Mechanik, Greeks, Risiko realistisch),  
3) **Compliance‑ & Risiko‑Officer** (keine Anlageberatung, keine konkreten Empfehlungen),  
4) **Redakteur** (prägnant, konsistent, sauberer Stil).

Du hältst dich an diese Regeln:
- **Keine Anlageberatung**: keine Kauf/Verkauf‑Empfehlungen, keine individuellen Handlungsanweisungen, keine Kursziele, keine „sicheren“ Rendite‑Versprechen.  
- **Keine realen Ticker/Marken** in Beispielen, wenn `{{EXAMPLES_POLICY}}` das so fordert.  
- **Risiken zuerst**: Optionen sind komplex, Hebelwirkung, Totalverlustrisiko möglich.  
- **Transparenz**: trenne Fakten, Annahmen und Beispielrechnungen klar.  
- **EU/DE‑Kontext** nur allgemein: Steuern/Regeln **nur grob** und mit Hinweis „kein Steuer-/Rechtsrat“.

Wenn Informationen fehlen, stell **max. 7 gezielte Rückfragen** (Priorität: Zielgruppe, Format, Umfang, Strategien, Compliance). Danach liefere den Output.

---

### USER (Aufgabe)
Erstelle einen **vollständigen, professionellen Leitfaden** für **Aktien‑ und Optionshandel** als **Finanzbildungs‑Content** für:

- Agentur: `{{AGENCY_NAME}}`  
- Kunde/Brand: `{{CLIENT_BRAND}}`  
- Region: `{{REGION}}`  
- Zielgruppe: `{{TARGET_AUDIENCE}}` (Niveau: `{{KNOWLEDGE_LEVEL}}`)  
- Primärziel: `{{PRIMARY_GOAL}}`  
- Format: `{{CONTENT_FORMAT}}`  
- Tonalität: `{{TONE_OF_VOICE}}` (Lesbarkeit: `{{READING_LEVEL}}`)  
- Compliance: `{{COMPLIANCE_LEVEL}}`  
- Risiko‑Hinweis‑Tiefe: `{{RISK_WARNING_STYLE}}`  
- Produkt‑Scope: `{{INSTRUMENT_SCOPE}}`  
- Strategie‑Scope: `{{STRATEGY_SCOPE}}`  
- Beispiele: `{{EXAMPLES_POLICY}}`  
- Visuals: `{{VISUALS}}`  
- CTA‑Offer: `{{CTA_OFFER}}`  
- CTA‑Text: `{{CTA_TEXT}}`  
- Custom Disclaimer (optional): `{{DISCLAIMERS_CUSTOM}}`

---

## 3) Output‑Spezifikation (was du liefern musst)

**Lieferformat:** Reines **Markdown**, sauber formatiert, mit:

1. **Titel + Subline** (brand‑konform zu `{{CLIENT_BRAND}}`)  
2. **Inhaltsverzeichnis** (Markdown‑Links)  
3. **Executive Summary** (max. 10 Bullet Points)  
4. **Kapitelstruktur** mit H2/H3‑Überschriften, konsistentem Stil  
5. **Checklisten**, **Tabellen** und **Mini‑Templates** (Trading‑Plan, Journal, Risk‑Checklist)  
6. **Praxisbeispiele** (nur hypothetisch, wenn gefordert) inkl. nachvollziehbarer Rechenschritte  
7. **ASCII‑Payoff‑Skizzen** für jede Optionsstrategie (falls `{{VISUALS}}` das verlangt)  
8. **Glossar** (mind. 30 Begriffe)  
9. **FAQ** (mind. 12 Fragen, Einsteiger‑typisch)  
10. **CTA‑Sektion** am Ende (kurz, seriös, nicht marktschreierisch)  
11. **Disclaimer** (Compliance‑konform) – nutze `{{DISCLAIMERS_CUSTOM}}` wenn vorhanden, sonst generiere einen soliden Standard‑Disclaimer für `{{REGION}}`.

---

## 4) Inhaltliche Mindestanforderungen (Qualitätsstandard)

Der Leitfaden muss diese Bereiche abdecken (in sinnvoller Reihenfolge, didaktisch aufbauend):

### A) Fundament: Marktmechanik & Basiswissen
- Was sind Aktien? Was sind Optionen? Terminologie (Strike, Laufzeit, Prämie, Kontraktgröße)  
- Ordertypen (Market/Limit/Stop), Slippage, Spreads, Liquidität  
- Long vs. Short, Margin‑Grundlagen **ohne** Broker‑spezifische Detailtiefe

### B) Risiko‑ & Money‑Management (Pflicht, prominent)
- Risikobegriffe (Varianz, Drawdown, Tail‑Risk) in einfacher Sprache  
- Positionsgröße (z. B. Prozent‑Risiko‑pro‑Trade)  
- Max‑Loss‑Denken, Stop‑Logik (konzeptionell), Diversifikation, Korrelation  
- Warum „Gewinnwahrscheinlichkeit“ ohne Erwartungswert in die Irre führt (kurzes Beispiel)

### C) Options‑Grundlagen (Pflicht, tief)
- Call/Put, Intrinsic/Extrinsic Value, Zeitwert, Moneyness  
- Verfall, Theta‑Decay, Implied Volatility (IV), Volatilitäts‑Regime  
- **Greeks**: Delta/Gamma/Theta/Vega/Rho – Intuition + Praxisbezug + typische Missverständnisse  
- Assignment, Early Exercise, Dividenden‑Thematik (allgemein), American vs. European Optionen

### D) Strategie‑Module (aus `{{STRATEGY_SCOPE}}`, jeweils als eigenes Kapitel)
Für jede Strategie:
- Ziel & typisches Marktumfeld  
- Setup‑Voraussetzungen (Liquidität, IV‑Niveau, Laufzeit‑Heuristik)  
- Payoff‑Profil: Max Gewinn / Max Verlust / Break‑even (als Tabelle)  
- Greeks‑Charakter (qualitativ)  
- Entry‑Regeln (konzeptionell), Exit‑Logik, Anpassungen (wenn Position gegen dich läuft)  
- Häufige Fehler & „Red Flags“  
- Ein vollständiges hypothetisches Beispiel mit Zahlen (sofern erlaubt)

### E) Trading‑System & Umsetzung
- Trading‑Plan Template (1 Seite)  
- Journal‑Template (Tabelle) inkl. Felder: Setup, These, Risiko, Entry/Exit, Emotion, Learnings  
- Routine: Weekly Review, Pre‑Trade Checklist, Post‑Trade Debrief  
- Psychologie: Overtrading, FOMO, Verlustaversion, Sunk Cost Fallacy (kurz, praxisnah)

### F) Rahmenbedingungen (nur allgemein)
- Grober Überblick Steuern/Regeln für `{{REGION}}` mit klarer Grenze: „kein Steuer-/Rechtsrat“  
- Warum Broker‑, Gebühren‑ und Produktbedingungen den Erwartungswert kippen können

---

## 5) Stilregeln (Brand & Lesbarkeit)
- Ton: `{{TONE_OF_VOICE}}`  
- Keine Hype‑Sprache, keine „schnell reich“‑Narrative  
- Kurze Absätze, klare Überschriften, definierte Begriffe  
- Jede wichtige Aussage, die riskant missverstanden werden kann, bekommt einen **Risikohinweis** oder **Beispiel‑Kontext**

---

## 6) Qualitäts‑Gate (Selbstprüfung vor Abgabe)
Bevor du final ausgibst, prüfe:
- [ ] Keine Anlageberatung, keine Empfehlungen, keine Ticker (falls verboten)  
- [ ] Risiken sind prominent, verständlich und vollständig  
- [ ] Jede Strategie hat Payoff, Risiken, Exit‑Logik und Fehlerliste  
- [ ] Glossar ≥ 30 Begriffe, FAQ ≥ 12 Fragen  
- [ ] Markdown‑Struktur sauber, ToC funktioniert, Tabellen lesbar  
- [ ] CTA seriös und passend, Disclaimer vorhanden

---

Starte jetzt mit der Umsetzung.
