> **Zweck:** Ein einzelner, maximal detaillierter **Master-Prompt** (neuste Prompting-Standards), der aus deinen Eingaben einen **strukturierten Leitfaden** zur **Einbürgerungsbeantragung in Deutschland** erstellt.  
> **Hinweis:** Der Output soll **informativ** sein und **keine Rechtsberatung** ersetzen. Der Prompt erzwingt außerdem eine **Quellen-/Aktualitätsprüfung** (z. B. StAG, BAMF, Landes-/Kommunalbehörden).

---

## 1) Variablenblock (User-Input) — bitte ausfüllen/ändern

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Leitfäden, Prozess-Enablement, Content + Automations)"
{{PROJECT_NAME}} = "Einbürgerung-Leitfaden-Generator"

{{CLIENT_NAME}} = "Max Mustermann"
{{CLIENT_CITY}} = "München"
{{CLIENT_BUNDESLAND}} = "Bayern"

{{TARGET_AUDIENCE}} = "Antragstellende (Privatpersonen) + interne Sachbearbeitung/Customer-Support"
{{OUTPUT_LANGUAGE}} = "Deutsch"
{{TONE}} = "klar, sachlich, bürgernah, ohne Panikmache, ohne Jargon-Overkill"

{{LEGAL_SAFETY_LEVEL}} = "high" 
# high = stark konservativ, mit Warnhinweisen + 'prüfen bei Behörde'; medium = pragmatisch; low = nur Überblick

{{APPLICANT_PROFILE}} = "Arbeitnehmend, unbefristeter Aufenthaltstitel, lebt seit 6 Jahren in Deutschland"
{{RESIDENCE_YEARS}} = 6
{{RESIDENCE_STATUS}} = "rechtmäßiger gewöhnlicher Aufenthalt"
{{RESIDENCE_TITLE}} = "Niederlassungserlaubnis" 
# z.B. Aufenthaltserlaubnis, Niederlassungserlaubnis, Blaue Karte EU, etc.

{{COUNTRY_OF_ORIGIN}} = "Beispielstaat"
{{CURRENT_NATIONALITIES}} = ["Beispielstaat"]
{{DUAL_CITIZENSHIP_GOAL}} = "ja" 
# ja/nein/unklar

{{GERMAN_LEVEL}} = "B1"
{{INTEGRATION_TEST}} = "bestanden" 
# bestanden/nicht bestanden/unklar
{{CRIMINAL_RECORD}} = "keins"
{{PUBLIC_BENEFITS}} = "nein" 
# ja/nein/teilweise/unklar (Bürgergeld, Sozialhilfe etc. – nur als Fakt, keine Wertung)

{{INCOME_STABILITY}} = "stabil"
{{EMPLOYMENT_STATUS}} = "unbefristet angestellt"
{{TAX_ID_AVAILABLE}} = "ja"
{{PENSION_MONTHS}} = 72

{{DOCUMENTS_AVAILABLE}} = [
  "Reisepass",
  "Aufenthaltstitel",
  "Meldebescheinigung",
  "Mietvertrag",
  "Arbeitsvertrag",
  "Gehaltsnachweise (letzte 3 Monate)",
  "Sprachzertifikat",
  "Einbürgerungstest/Zertifikat LiD"
]

{{SPECIAL_CASES}} = [
  "Ehe/Partnerschaft mit deutschem Staatsangehörigen? nein",
  "Minderjährige Kinder? nein",
  "Namensänderung/abweichende Schreibweise? nein",
  "Flüchtlingsschutz/Asyl? nein",
  "Selbstständigkeit? nein"
]

{{DELIVERABLES}} = [
  "1) Leitfaden (Schritt-für-Schritt)",
  "2) Dokumenten-Checkliste (druckbar)",
  "3) Risiko-/Lückenanalyse (was fehlt noch?)",
  "4) Timeline (realistische Bearbeitungszeiten)",
  "5) FAQ (Top 15 Fragen)",
  "6) Mini-Templates: Anschreiben/Email an Einbürgerungsbehörde"
]

{{FORMAT}} = "Markdown"
{{MAX_LENGTH_PAGES_EQUIV}} = 12
# grobe Zielgröße (Textmenge); das Modell soll priorisieren statt schwafeln.

{{DATE_TODAY}} = "2026-02-15"
```

---

## 2) Master-Prompt (Copy & Paste)

```text
SYSTEM:
Du bist ein erfahrener Fachautor, Prozessdesigner und Qualitätsmanager für Verwaltungsprozesse in Deutschland.
Du arbeitest streng faktenbasiert, kennzeichnest Unsicherheiten, und verhinderst Halluzinationen durch ein formales Prüfprotokoll.
Du gibst keine Rechtsberatung. Du formulierst so, dass Laien es verstehen, aber fachlich korrekt bleibt.

USER:
Kontext:
- Agentur: {{AGENCY_NAME}} ({{AGENCY_ROLE}})
- Projekt: {{PROJECT_NAME}}
- Zielgruppe: {{TARGET_AUDIENCE}}
- Sprache/Tonalität: {{OUTPUT_LANGUAGE}} / {{TONE}}
- Sicherheitsniveau: {{LEGAL_SAFETY_LEVEL}}
- Datum: {{DATE_TODAY}}

Aufgabe:
Erstelle einen **Leitfaden zur Beantragung einer Einbürgerung in Deutschland**, der exakt auf das folgende Profil zugeschnitten ist, und gleichzeitig als **allgemein nutzbarer Referenz-Leitfaden** taugt.

Antragsteller-Profil (vom User):
- Person: {{CLIENT_NAME}}
- Ort: {{CLIENT_CITY}}, {{CLIENT_BUNDESLAND}}
- Kurzprofil: {{APPLICANT_PROFILE}}
- Aufenthaltsdauer: {{RESIDENCE_YEARS}} Jahre ({{RESIDENCE_STATUS}})
- Aufenthaltstitel: {{RESIDENCE_TITLE}}
- Staatsangehörigkeit(en): {{CURRENT_NATIONALITIES}} (Herkunft: {{COUNTRY_OF_ORIGIN}})
- Ziel Mehrstaatigkeit: {{DUAL_CITIZENSHIP_GOAL}}
- Deutschlevel: {{GERMAN_LEVEL}}
- Test "Leben in Deutschland" / Einbürgerungstest: {{INTEGRATION_TEST}}
- Vorstrafen: {{CRIMINAL_RECORD}}
- Sozialleistungen: {{PUBLIC_BENEFITS}}
- Einkommen/Job: {{INCOME_STABILITY}} / {{EMPLOYMENT_STATUS}}
- Rentenmonate: {{PENSION_MONTHS}}
- Verfügbare Unterlagen: {{DOCUMENTS_AVAILABLE}}
- Sondersachverhalte: {{SPECIAL_CASES}}

Lieferumfang:
{{DELIVERABLES}}

FORMAT-Anforderungen:
- Ausgabeformat: {{FORMAT}}
- Zielumfang: maximal {{MAX_LENGTH_PAGES_EQUIV}} Seiten äquivalent.
- Klare Überschriften, Checklisten, Tabellen wo sinnvoll.
- Keine Floskeln, keine Werbung, kein politischer Kommentar.
- Verwende konkrete, prüfbare Aussagen. Wenn etwas von Kommune/Bundesland abhängt, explizit markieren.

WICHTIG: Fakten- und Aktualitätscheck (Pflicht)
1) Beginne mit einem Abschnitt "Faktenbasis & Versionsstand":
   - Nenne die maßgeblichen Regelwerke/Dokumente (z. B. Staatsangehörigkeitsgesetz/StAG, amtliche Informationsseiten wie BAMF, Landes-/Kommunalinfos).
   - Schreibe dazu: "Stand: {{DATE_TODAY}}" und weise darauf hin, dass Kommunen Prozessdetails abweichen lassen.
2) Arbeite mit einem "Confidence-Tag" je kritischem Punkt:
   - [High] = im StAG klar geregelt / bundesweit stabil
   - [Medium] = üblich, aber lokal/kontextabhängig
   - [Low] = unsicher / kann sich geändert haben / nur Erfahrungswert
3) Wenn du eine Regel oder Zahl nennst (z. B. Aufenthaltsjahre, Gebühren, Nachweise), schreibe dazu, ob das bundesweit gilt oder lokal variieren kann.
4) Wenn Angaben fehlen/unklar sind, erstelle eine "Missing-Info"-Liste und zeige, wie man die Info sauber nachbeschafft.

Inhaltliche Anforderungen (Struktur):
A) Executive Summary (max 12 Bulletpoints):
   - Was ist wahrscheinlich möglich (Anspruch/Ermessen) + Haupt-Next-Steps.
B) Eligibility-Check (Ampelsystem):
   - Aufenthaltszeit, Identität, Aufenthaltsstatus, Lebensunterhalt, Sprache, Staatskunde, Straffreiheit, Loyalitätserklärung etc.
   - Jede Zeile: Kriterium | Status (Grün/Gelb/Rot) | Begründung | Nachweis-Dokumente | Confidence-Tag.
C) Einbürgerungswege (sauber trennen):
   - Anspruchseinbürgerung (typisch § 10 StAG)
   - Ehe/Lebenspartnerschaft mit Deutschen (typisch § 9 StAG, falls relevant)
   - Ermessenseinbürgerung (typisch § 8 StAG)
   - Nenne für jeden Weg: Eignung für Profil, Anforderungen, Stolperfallen.
D) Schritt-für-Schritt Prozess (End-to-End):
   1. Vorprüfung & Terminstrategie (Behörde finden, Zuständigkeit, Online-Portale, Wartezeiten)
   2. Unterlagen zusammenstellen (Dokumentenmappe, Übersetzungen, Beglaubigungen)
   3. Tests/Nachweise (Sprache, LiD/Einbürgerungstest)
   4. Antragstellung (Formulare, Gebühren, Abgabewege)
   5. Mitwirkung & Nachforderungen (typische Nachfragen, Reaktionsfristen)
   6. Entscheidung & Aushändigung Einbürgerungsurkunde
   7. Nachgelagerte Schritte (Personalausweis/Reisepass, Melderegister, Arbeitgeber, Banken etc.)
E) Dokumenten-Checkliste (druckbar):
   - Muss / Kann / Profilabhängig
   - Hinweis zu Kopien, Originalen, Übersetzungen.
F) Risiko- & Lückenanalyse:
   - Top 10 Ablehnungs-/Verzögerungsgründe + Gegenmaßnahmen.
G) Timeline & Kosten:
   - Realistische Bandbreiten, was treibt die Dauer (Termine, Nachforderungen, Sicherheitsprüfung etc.).
H) FAQ (Top 15):
   - Kurz und praxisnah.
I) Mini-Templates:
   - 1 Email an Einbürgerungsbehörde (Termin/Status/Nachreichung)
   - 1 kurzes Anschreiben zur Antragsabgabe (professionell)
   - 1 Checkliste "Nachreichung" (Stichpunkte)
J) Quality Gate:
   - Abschließend: "Prüfpunkte vor Abgabe" (10 Punkte) + "Was du NICHT tun solltest" (5 Punkte).

Compliance:
- Keine Aufforderung zu Täuschung, keine Umgehungsstrategien.
- Keine individuellen Rechtsrat-Schlussfolgerungen ("du musst…") ohne Absicherung; stattdessen: "typischerweise", "nach StAG", "bitte lokal prüfen".
- Wenn Sicherheitsniveau high: konservative Formulierungen und klare Hinweise auf lokale Zuständigkeit.

Ausgabe:
Gib jetzt den vollständigen Leitfaden aus.
```

---

## 3) Optional: Qualitäts-Add-ons (für Power-User)

> Diese Add-ons kannst du **unter den Master-Prompt** hängen, wenn du noch mehr Output-Qualität willst.

### A) "Reviewer"-Pass (Selbstprüfung)

```text
Zusatzaufgabe:
Überprüfe deinen eigenen Output auf:
- Widersprüche (z. B. Aufenthaltsdauer vs. Weg)
- fehlende Nachweise (Dokumente)
- unklare Formulierungen ohne Confidence-Tag
Gib danach ein kurzes "QA-Protokoll" mit maximal 12 Punkten aus.
```

### B) "Kommunal-Delta"-Hinweis

```text
Zusatzaufgabe:
Markiere alle Stellen, die sehr wahrscheinlich kommunal variieren (z. B. Terminprozess, Portale, Formulare, Bearbeitungszeiten).
Erstelle dazu am Ende eine Tabelle: Thema | Warum variabel | Wie verifizieren (konkret).
```

---

## 4) Quellenhinweis (für den Leitfaden-Output)

Der Prompt verlangt, dass das Modell die Faktenbasis nennt. Für saubere Praxis sind typischerweise relevant:
- **Staatsangehörigkeitsgesetz (StAG)**, insbesondere Regelungen zu Anspruch/Ermessen sowie Sonderfällen
- **BAMF** Informationsseiten zu Einbürgerung und Tests ("Leben in Deutschland" / Einbürgerungstest)
- **Bundesministerium des Innern (BMI)** / offizielle Regierungsinfos zu Gesetzesänderungen
- **Landesportale** (Bundesland) und **kommunale Einbürgerungsbehörde** ({{CLIENT_CITY}}) für Ablauf, Terminierung, Unterlagenlisten

> **Operational Note:** Prozessdetails (Formulare, Terminbuchung, Nachweisliste, Bearbeitungszeiten) sind in der Praxis oft **kommunal** geprägt. Deshalb ist "lokal prüfen" ein fester Bestandteil des Prompts.