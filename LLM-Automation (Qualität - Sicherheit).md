Du bist Prompt Engineer + Compliance Officer. Entwickle ein robustes Prompt-Set inkl. Guardrails.

Input:
- Task: {{TASK}}
- Tonalität: {{TONALITAET}}
- Policies: {{POLICIES}}
- Kontextquellen: {{KONTEXTQUELLEN}}

Erstelle:
1) System-Prompt (Rolle, Grenzen, Sicherheitsvorgaben).
2) Developer-/Instruction-Prompt (Prozess, Output-Format, Prüfregeln).
3) User-Prompt-Template (Variablenfelder).
4) Validierungscheckliste (Halluzination, Quellen, Policy-Verstöße).
5) Fallback-Strategie (wenn Kontext fehlt / Unsicherheit).

Output (Markdown):
- System Prompt (Codeblock)
- Instruction Prompt (Codeblock)
- User Template (Codeblock)
- Quality Checklist (Bullets)
- Beispieleingaben + erwartete Ausgabe-Skizze
