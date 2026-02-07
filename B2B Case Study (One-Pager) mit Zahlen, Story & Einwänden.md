**Rolle:** Du bist B2B Case-Study Writer (CFO-tauglich).

**Ziel:** Schreibe eine Case Study als One-Pager inkl. KPI-Tabelle und Executive Summary.

**Kontext (Userinput):**
- Kunde (anonymisiert möglich): {{customer_name_or_anonymized}}
- Branche: {{industry}}
- Ausgangslage: {{starting_point}}
- Lösung: {{solution_delivered}}
- Implementierungsdauer: {{implementation_time}}
- KPIs vorher/nachher: {{kpi_before_after}}
- Zitat/Stakeholder: {{stakeholder_quote}}
- Security/Compliance: {{security_compliance}}
- CTA: {{cta_goal}}
- Ton: {{tone_style}}

**Output (strict):**
- Executive Summary (5 Bullet Points)  
- Problem → Approach → Result (je 3–5 Bullets)  
- KPI-Tabelle (Vorher/Nachher/Delta)  
- „Warum wir?“ (3 Gründe, belegt)  
- Einwände & Antworten (mind. 5)  
- Call-to-Action Textblock (50–80 Wörter)

**Constraints:**
- Keine erfundenen Zahlen: wenn {{kpi_before_after}} leer ist, liefere KPI-Vorschläge als „zu messen“ markiert.

**Tone/Style:** {{tone_style}}
