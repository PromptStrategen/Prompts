> **Ziel:** Mit diesem Prompt erzeugst du einen **strategischen Leitfaden**, der Teams befähigt, **systematisch neue Denkwege** zu entwickeln (Innovation, Positionierung, Kampagnen- und Produktideen) – **strukturierter Output**, **messbare Hypothesen**, **klare nächste Schritte**.

---

## 1) Copy & Paste Prompt (mit Variablen)

### 1.1 Variablenblock (User-Input – bitte ausfüllen)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_BRAND}} = "Beispiel GmbH"
{{INDUSTRY}} = "B2B SaaS / IT-Services"
{{REGION}} = "DACH"
{{TARGET_AUDIENCE}} = "IT-Leitung, Ops/Support, Entscheider in KMU (50–500 MA)"
{{CORE_OFFER}} = "Marketing & Prozessoptimierung"
{{PRIMARY_OBJECTIVE}} = "Neue Wachstumspfade/Positionierung finden"
{{CURRENT_CHALLENGE}} = "Stagnierende Leads, austauschbare Botschaften, hoher Wettbewerbsdruck"
{{COMPETITOR_SET}} = "Systemhäuser, No-Code-Agenturen, RPA-Beratungen"
{{UNIQUE_PROOF}} = "MVP in 14 Tagen · DSGVO-by-design · Security-first"
{{CURRENT_CHANNELS}} = "LinkedIn, Website/SEO, Outbound, Webinare"
{{BUDGET_RANGE}} = "10–30k/Monat"
{{TIME_HORIZON}} = "90 Tage"
{{CONSTRAINTS}} = "Keine unrealistischen Versprechen; Compliance/DSGVO; Ressourcen: 1 PM, 1 Copy, 1 Designer, 1 Engineer"
{{DATA_AVAILABLE}} = "CRM-Export, Website Analytics, 20 Sales Calls Notes, NPS, Support Tickets"
{{RISK_TOLERANCE}} = "mittel"
{{TONE}} = "Corporate, prägnant, ohne Buzzword-Overkill"
{{LANGUAGE}} = "Deutsch"
```

### 1.2 Prompt (an ein LLM senden)

```text
Du agierst als: Innovationsstratege, Behavioral Economist, Growth Lead und Kommunikationsarchitekt in einer Marketing-Agentur. 
Dein Arbeitsmodus: kritisch, evidenzorientiert, kreativ – aber mit Business-Disziplin. Du vermeidest Floskeln. Du priorisierst Hebel mit Impact.

KONTEXT
- Agentur: {{AGENCY_NAME}}
- Kunde/Brand: {{CLIENT_BRAND}} ({{INDUSTRY}}, {{REGION}})
- Zielgruppe: {{TARGET_AUDIENCE}}
- Kernangebot: {{CORE_OFFER}}
- Primärziel: {{PRIMARY_OBJECTIVE}}
- Problem/Lage: {{CURRENT_CHALLENGE}}
- Wettbewerb: {{COMPETITOR_SET}}
- Proof/Trust: {{UNIQUE_PROOF}}
- Kanäle: {{CURRENT_CHANNELS}}
- Budget: {{BUDGET_RANGE}}
- Zeithorizont: {{TIME_HORIZON}}
- Constraints: {{CONSTRAINTS}}
- Datenlage: {{DATA_AVAILABLE}}
- Risikotoleranz: {{RISK_TOLERANCE}}
- Tonalität/Sprache: {{TONE}} / {{LANGUAGE}}

AUFGABE
Erstelle einen Leitfaden "Neue Wege denken" als umsetzbares Arbeitsdokument für ein Agentur-Team. 
Der Leitfaden soll neue Denkpfade nicht nur brainstormen, sondern **systematisch erzwingen** (Reframing, Gegenannahmen, Hypothesen, Experimente).

ARBEITSPROZESS (zwingend, explizit abarbeiten)
1) Problempräzisierung:
   - Formuliere das Kernproblem in 3 Varianten: (a) operativ, (b) psychologisch (Jobs-to-be-done), (c) systemisch (Marktmechanik).
   - Liste 10 Annahmen, die im aktuellen Denken "stillschweigend" drinstecken.
2) Reframing-Matrix:
   - Erzeuge 12 Reframes, jeweils mit: neuer Blickwinkel, wofür es gut ist, was es riskant macht.
   - Nutze mindestens diese Linsen: "Umkehrung", "Extremfall", "Constraint als Feature", "Second-order effects", "Nicht-Kunde", "Antiwettbewerb", "Pre-Mortem".
3) Opportunity-Raum:
   - Baue eine Opportunity Map mit 3 Achsen: (a) Kundennutzen (hoch/niedrig), (b) Differenzierung (hoch/niedrig), (c) Umsetzbarkeit in {{TIME_HORIZON}} (hoch/niedrig).
   - Platziere mindestens 15 konkrete Opportunities (kurze Titel + 1 Satz).
4) Hypothesen & Experimente (Growth-Loop):
   - Für die Top-7 Opportunities: Formuliere je 1 klare Hypothese im Format:
     "Wenn wir [Intervention], dann [messbarer Effekt], weil [Mechanismus]."
   - Entwirf je 1 Experiment in 14 Tagen: Ziel, Setup, Assets, Kanal, Erfolgskriterium (Metrik + Schwellenwert), Risiken, Stop/Go-Regel.
5) Messaging & Narrative:
   - Leite aus den Top-3 Reframes eine Positionierungs-Story ab:
     Problem → Spannung → neuer Rahmen → Lösung → Beweis → CTA.
   - Liefere je 3 Hook-Varianten (LinkedIn), 2 Value-Proposition-Sätze (Website), 1 Elevator Pitch (20 Sek).
6) Betriebsmodell & Priorisierung:
   - Erstelle eine Priorisierung nach ICE (Impact, Confidence, Ease) mit 1–10 Skala.
   - Gib eine 90-Tage-Roadmap: Woche 1–2, 3–6, 7–12 mit Deliverables, Owner-Rollen, Dependencies.
7) Quality Gates:
   - Validitätscheck: Welche Annahmen sind unbewiesen? Welche Daten fehlen? Welche Tests sind "billig" und welche "teuer"?
   - Compliance-Check: Welche Aussagen sind riskant (z. B. Datenschutz/Heilsversprechen)? Formuliere sichere Alternativen.

OUTPUT-ANFORDERUNGEN (Format strikt einhalten)
A) Executive Summary (max. 10 Bulletpoints)
B) Problem- und Annahmen-Register (Tabelle)
C) Reframing-Matrix (Tabelle, 12 Zeilen)
D) Opportunity Map (Matrix + Liste der 15 Opportunities)
E) Top-7 Hypothesen + 14-Tage-Experimente (jeweils strukturiert)
F) Messaging-Toolkit (Hooks, Value Props, Pitch)
G) ICE-Priorisierung (Tabelle) + 90-Tage-Roadmap
H) Risiken, Pre-Mortem, Datenbedarf, Compliance

QUALITÄTSSTANDARD
- Keine generischen Ratschläge. Jede Empfehlung muss auf den Kontext oben referenzieren.
- Jede Experimentidee muss messbar sein und ein klares Stop/Go-Kriterium enthalten.
- Verwende präzise, agenturtaugliche Sprache ({{TONE}}), keine Buzzword-Kaskaden.
- Liefere konkrete Beispiele/Asset-Ideen (z. B. Landingpage-Abschnitte, Ads-Angles, Webinar-Agenda).
- Wo Informationen fehlen: schreibe "Fehlt: …" und nenne 1–3 minimal-invasive Wege, das zu beschaffen.

STARTE JETZT. Gib den Leitfaden vollständig aus.
```

---

## 2) Beispiel (kurz) – ausgefüllter Variablenblock

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_BRAND}} = "Ich-möchte-KI-verstehen GmbH"
{{INDUSTRY}} = "B2B SaaS / IT-Services"
{{REGION}} = "Deutschland"
{{TARGET_AUDIENCE}} = "IT-Leitung, Operations, Support-Leads in KMU"
{{CORE_OFFER}} = "Prompt-Optimierung + RAG-Wissenssysteme"
{{PRIMARY_OBJECTIVE}} = "Pipeline-Wachstum über Differenzierung"
{{CURRENT_CHALLENGE}} = "Viele Erstgespräche, aber niedrige Close-Rate; Angebot wirkt austauschbar"
{{COMPETITOR_SET}} = "No-Code-Agenturen, Systemhäuser, RPA-Consultants"
{{UNIQUE_PROOF}} = "MVP in 14 Tagen · DSGVO-by-design · Security-first"
{{CURRENT_CHANNELS}} = "LinkedIn, Blog/SEO, Outreach"
{{BUDGET_RANGE}} = "5–15k/Monat"
{{TIME_HORIZON}} = "90 Tage"
{{CONSTRAINTS}} = "Kleines Team; keine Paid-Ads im ersten Monat"
{{DATA_AVAILABLE}} = "Sales Call Notes, Website Analytics, Kundenfeedback"
{{RISK_TOLERANCE}} = "mittel"
{{TONE}} = "klar, professionell, leicht nerdig"
{{LANGUAGE}} = "Deutsch"
```

---

## 3) Betriebshinweise (für Team-Nutzung)

- **Input-Disziplin:** Je besser der Variablenblock, desto weniger "Ideen-Rauschen".
- **Arbeitsweise:** Erst Output erzeugen, dann in einem 30–45-Min Review **1) streichen**, **2) schärfen**, **3) testen**.
- **Governance:** Jede Hypothese bekommt einen Owner, ein Datum, eine Metrik. Keine Experimente ohne Messpunkt.
