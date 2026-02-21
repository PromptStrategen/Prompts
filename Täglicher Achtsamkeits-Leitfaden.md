> **Ziel:** Dieses Prompt erzeugt einen **hochwertigen, praxisnahen und detailtiefen Achtsamkeits-Leitfaden** für den Alltag – inklusive **Morgen-, Mittags-, Abend-Routinen**, Mikro-Übungen, Reflexion, Progress-Tracking und Varianten (z. B. Stress, Fokus, Schlaf).  
> **Output:** Ein **druck- und app-tauglicher** Leitfaden in sauberer Struktur (Word Dokument), ohne esoterische Floskeln, mit konkreten Zeitfenstern und klaren Anweisungen.

---

## 1) User-Input: Variablenblock (ausfüllen/ändern)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_BRAND}} = "Beispiel GmbH"
{{TARGET_AUDIENCE}} = "Wissensarbeiter (25–55), hoher Stress, wenig Zeit"
{{GOAL_PRIMARY}} = "Stress reduzieren + Fokus erhöhen"
{{GOAL_SECONDARY}} = "Schlaf verbessern"
{{TONE}} = "professionell, ruhig, motivierend, ohne Kitsch"
{{LANGUAGE}} = "Deutsch"
{{FORMAT_PREFERENCE}} = "Word Dokument"
{{DAILY_TIME_BUDGET_MIN}} = 12
{{TIME_WINDOWS}} = "Morgen (3–5 min), Mittag (2–4 min), Abend (4–6 min)"
{{EXPERIENCE_LEVEL}} = "Einsteiger"
{{CONSTRAINTS}} = "keine religiösen Begriffe, keine Heilsversprechen, alltagstauglich"
{{CONTEXT}} = "Viel Bildschirmzeit, viele Meetings, hoher E-Mail-Load"
{{TRIGGERS}} = "Anspannung vor Calls, Grübeln abends, Prokrastination"
{{PREFERRED_TECHNIQUES}} = "Atemübungen, Body Scan, kurze Journaling-Prompts, Micro-Pausen"
{{AVOID_TECHNIQUES}} = "lange Meditationen > 10 min, esoterische Sprache"
{{ACCESSIBILITY_NEEDS}} = "inkl. Alternativen für laute Umgebung und für unterwegs"
{{TRACKING_STYLE}} = "Checkliste + 1–10 Skala + Wochenreview"
{{LEGAL_SAFETY_NOTE}} = "Kein Ersatz für medizinische/psychotherapeutische Behandlung"
```

---

## 2) Copy-&-Paste Prompt (Master Prompt)

**Rolle / Setup**  
Du agierst als **Evidence-based Mindfulness Coach** (achtsamkeitsbasierte Stressreduktion, habit building, Verhaltenspsychologie), als **UX-Redakteur** (klare Microcopy) und als **Marketing-Agentur-Stratege** (Zielgruppenorientierung, messbare Outcomes).  
Du arbeitest **nüchtern, alltagstauglich und strukturiert**. Keine Heilsversprechen, keine Diagnosen, kein pseudo-wissenschaftlicher Jargon.

**Aufgabe**  
Erstelle für **{{CLIENT_BRAND}}** einen **Täglichen Achtsamkeits-Leitfaden** für **{{TARGET_AUDIENCE}}**. Ziel ist **{{GOAL_PRIMARY}}** (sekundär: **{{GOAL_SECONDARY}}**) bei einem täglichen Zeitbudget von **{{DAILY_TIME_BUDGET_MIN}} Minuten** und Zeitfenstern **{{TIME_WINDOWS}}**.  
Berücksichtige Kontext **{{CONTEXT}}**, typische Trigger **{{TRIGGERS}}**, bevorzugte Techniken **{{PREFERRED_TECHNIQUES}}** und Ausschlüsse **{{AVOID_TECHNIQUES}}**.  
Halte dich an Constraints: **{{CONSTRAINTS}}**. Sprache: **{{LANGUAGE}}**, Format: **{{FORMAT_PREFERENCE}}**, Tonalität: **{{TONE}}**.

**Output-Anforderungen (streng)**  
Gib das Ergebnis **als Word Dokument** aus mit folgenden Abschnitten und Formaten:

### A) Executive Summary (max. 120 Wörter)
- Problem / Zielbild / Nutzen in 3 bullets (messbar formuliert)

### B) Leitprinzipien (5–7 Punkte)
- Kurz, klar, "so wendest du es an" (keine Theorie-Wüsten)

### C) Tagesroutine (Kernstück)
Erstelle eine Tagesroutine mit:
1. **Morgen-Routine** (3–5 Min)  
2. **Mittags-Reset** (2–4 Min)  
3. **Abend-Routine** (4–6 Min)  
Für jede Routine:
- **Ziel** (1 Satz)
- **Schritt-für-Schritt** (nummeriert, mit Sekunden/Minutenangaben)
- **Mentale Check-in Frage** (1 Frage)
- **Fallback-Variante** (wenn "keine Zeit" / "laut" / "unterwegs")
- **Typische Fehler + Fix** (2–3 Paare)

### D) Mikro-Interventionen (Achtsamkeit in Meetings & Bildschirmalltag)
- 10 Micro-Übungen (30–90 Sekunden)  
- Jede Übung: **Trigger → Aktion → Nutzen → 1 Satz Ankerphrase**
- Speziell: "vor Call", "nach Stress-Mail", "bei Prokrastination", "zwischen Meetings"

### E) Journaling-Module (ultrakurz)
- 7 Tages-Prompts (max. 2 Sätze pro Prompt)
- 3 Varianten: "Fokus", "Stress", "Dankbarkeit" (je 3 Prompts)

### F) Wochenreview (10 Minuten, einmal pro Woche)
- 5 Leitfragen (konkret)
- Mini-Auswertung: Was funktioniert? Was raus? Was rein?
- 1 Anpassungsregel ("Wenn X, dann Y")

### G) Tracking & Scorecard
- **Tägliche Checkliste** (Checkboxen)
- **Skalen** (Stress 1–10, Fokus 1–10, Schlafqualität 1–10)
- **KPI-Definitionen** (z. B. "3/7 Tage vollständig")
- **Progression** über 4 Wochen (Level 1–4, jeweils kleine Steigerung)

### H) Personalisierungs-Guide
- Wähle 3 Profile (z. B. "High-Stress", "Fokus-Boost", "Schlaf-Fix")  
- Pro Profil: Anpassung der Routinen + 2 Micro-Übungen + 1 Journaling-Set

### I) Safety & Grenzen (Pflicht)
- Kurzer Hinweis: **{{LEGAL_SAFETY_NOTE}}**
- Red Flags: Wann professionelle Hilfe sinnvoll ist (neutral formuliert, keine Diagnosen)

---

## 3) Qualitätskriterien / Prüfliste (vor finaler Ausgabe anwenden)

- **Konkret:** Jede Übung ist "jetzt sofort" ausführbar (kein "sei einfach präsent" ohne Anleitung).  
- **Zeitgenau:** Jede Routine hat klare Minuten-/Sekundenangaben.  
- **Alltagstauglich:** Passt zu {{CONTEXT}} und {{TARGET_AUDIENCE}} (Meetings, Screen-Work, Zeitmangel).  
- **Nicht esoterisch:** Ton entspricht {{TONE}} und {{CONSTRAINTS}}.  
- **Messbar:** Tracking/Scorecard ist nutzbar ohne zusätzliche Tools.  
- **Zugänglich:** Alternativen für unterwegs/laute Umgebung sind enthalten.  
- **Kompakt, aber tief:** Keine Romane – lieber präzise Module mit hoher Dichte.

---

## 4) Optional: Mini-Add-ons (nur wenn sinnvoll)

Wenn es ohne Aufblähen passt, ergänze:
- **"Notfall-Protokoll" (2 Minuten)** für akute Überforderung  
- **"Pre-Sleep Routine" (3 Minuten)** als Alternative zur Abendroutine  
- **"Focus Sprint" (5 Minuten)** vor Deep Work

---

## 5) Output-Formatierung (Styling)

- Nutze klare Überschriften (H2/H3), nummerierte Schritte, Checkboxen.
- Vermeide Emojis (außer ausdrücklich gewünscht).
- Schreibe so, dass der Leitfaden **direkt in Notion/Obsidian/Confluence** funktioniert.

---

**Start jetzt.**  
Erzeuge den kompletten Leitfaden gemäß oben. Keine Meta-Erklärungen über dein Vorgehen, nur das Ergebnis.