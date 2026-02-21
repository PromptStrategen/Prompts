> **Ziel:** Dieser Prompt erzeugt einen **praxisnahen, tief strukturierten Leitfaden**, wie man **versteckte Nachrichten** (z. B. **Steganografie in Bildern/Audio/Video**, **verdeckte Textmuster**, **Metadaten-Hinweise**, **Verschlüsselung/Chiffren**, **Obfuskation in Dateien/Webseiten**) **systematisch findet, verifiziert und dokumentiert** — mit **klaren Tools, Prüfschritten, Evidenzsicherung** und **kommunizierbaren Ergebnissen**.  
> **Wichtig:** Der Output soll **defensiv/forensisch** sein (Analyse & Aufklärung), **keine** Anleitung zum Verstecken/Umgehen von Sicherheitsmaßnahmen.

---

## ✅ Copy‑&‑Paste Prompt (mit Variablen)

### 1) Variablenblock (User‑Input — ausfüllen/ändern)

```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{CLIENT_NAME}} = "Beispielkunde GmbH"
{{PROJECT_NAME}} = "Hidden-Message-Discovery-Playbook"

{{PRIMARY_GOAL}} = "Versteckte Nachricht finden und belastbar nachweisen"
{{AUDIENCE}} = "IT/Forensik-Team + Management (zwei Ebenen: technisch & executive)"

{{SCOPE_MEDIA_TYPES}} = ["Bild", "Audio", "Video", "PDF/Dokument", "Archiv/ZIP", "Web/HTML", "Code/Script", "E-Mail"]
{{SUSPECT_ASSETS}} = [
  "datei_01.png",
  "datei_02.wav",
  "mail_03.eml",
  "seite_04.html"
]

{{KNOWN_CONTEXT}} = "Kurzkontext: Woher stammen die Dateien? Wer hat sie geliefert? Welche Hypothesen gibt es?"
{{CONSTRAINTS}} = [
  "Offline-Analyse bevorzugt",
  "Keine Daten an Dritte senden",
  "DSGVO/Compliance beachten",
  "Beweiskette dokumentieren (Chain of Custody)"
]

{{ENVIRONMENT}} = "Windows 11 + WSL2 (Ubuntu) / alternativ macOS / alternativ Linux"
{{TOOLING_ALLOWED}} = [
  "exiftool",
  "file",
  "strings",
  "sha256sum",
  "binwalk",
  "steghide",
  "zsteg",
  "ffmpeg",
  "audacity (optional)",
  "pdfinfo/pdftotext",
  "CyberChef (offline oder lokal)",
  "Wireshark (falls Netzwerkartefakte)"
]

{{RISK_LEVEL}} = "mittel"  # niedrig | mittel | hoch
{{TIME_BUDGET_HOURS}} = 6
{{DELIVERABLE_FORMAT}} = ["Schritt-für-Schritt-Leitfaden", "Checkliste", "Dokuvorlage", "Executive Summary"]
{{TONE}} = "Corporate, prägnant, belastbar (kein Buzzword-Overkill)"
{{LANGUAGE}} = "Deutsch"
```

---

### 2) Hauptprompt (an ein LLM senden)

```text
Du bist ein Senior Digital-Forensiker, Incident-Responder und Technical Writer in {{AGENCY_NAME}}.
Dein Auftrag: Erstelle für {{CLIENT_NAME}} einen umfassenden Leitfaden "Versteckte Nachricht finden" für das Projekt {{PROJECT_NAME}}.

KONTEXT
- Primärziel: {{PRIMARY_GOAL}}
- Zielgruppenebenen: {{AUDIENCE}} (liefere sowohl technische Tiefe als auch Management-Übersicht)
- Umfang/Artefakte: {{SCOPE_MEDIA_TYPES}}; Verdächtige Assets: {{SUSPECT_ASSETS}}
- Kontext/Hypothesen: {{KNOWN_CONTEXT}}
- Rahmenbedingungen: {{CONSTRAINTS}}
- Arbeitsumgebung: {{ENVIRONMENT}}
- Erlaubte Tools: {{TOOLING_ALLOWED}}
- Risiko-Level: {{RISK_LEVEL}}
- Zeitbudget: {{TIME_BUDGET_HOURS}} Stunden
- Deliverables: {{DELIVERABLE_FORMAT}}
- Sprache/Ton: {{LANGUAGE}}, {{TONE}}

AUFGABEN & QUALITÄTSGATES
1) Liefere einen forensisch sauberen Workflow, der defensiv ist:
   - Keine Anleitung zum Verstecken von Nachrichten, nur zum Finden/Verifizieren.
   - Kein Umgehen von Sicherheitsmechanismen, keine schädlichen Handlungen.
2) Baue den Leitfaden modular als "Playbook" mit Phasen auf:
   - Phase A: Intake & Beweissicherung (Hashing, Kopien, Chain of Custody)
   - Phase B: Schnelltriage (Filetype, Metadaten, Strings, Offsets, Entropie, Auffälligkeiten)
   - Phase C: Tiefenanalyse je Medientyp (Bild/Audio/Video/PDF/Archive/Web/Code/E-Mail)
   - Phase D: Hypothesen testen & falsifizieren (Beweisführung, Gegenchecks, Reproduzierbarkeit)
   - Phase E: Reporting (technisch + Executive Summary)
3) Pro Phase:
   - Ziele, Eingaben, erwartete Ergebnisse, "Red Flags", typische Fehler, Stop-Kriterien
   - Konkrete Befehle/Tool-Aufrufe (mit Platzhaltern) für {{ENVIRONMENT}}
   - Entscheidungspfade ("Wenn X, dann Y") und Priorisierung nach {{RISK_LEVEL}} und {{TIME_BUDGET_HOURS}}
4) Lege besonderes Gewicht auf:
   - Steganografie-Detektion (z. B. LSB-Muster, ungewöhnliche Farbkanäle, Container in Dateien)
   - Metadaten & Side-Channels (EXIF/XMP, PDF-Objekte, E-Mail-Header)
   - Obfuskation (Base64, ROT/Caesar, XOR, Zero-width chars, homoglyphs)
   - Dateicontainer/Append-Daten (binwalk, Anhänge, ZIP-in-PNG, polyglot files)
   - Audio-Spektralanalyse (Spektrogramm, versteckte Töne/Patterns)
   - Video-Frames & Subtitles/Tracks (extra Streams, Untertitel, chapter metadata)
5) Liefere Vorlagen:
   - Checkliste "Schnelltriage in 30 Minuten"
   - Dokumentationsvorlage "Befunde & Evidenz" (Tabellenstruktur, Felder, Hashes, Screenshots-Plan)
   - Executive-Summary-Template (Risiko, Impact, Confidence, Next Steps)
6) Nenne Grenzen & Evidenzqualität:
   - Was ist ein "Hinweis" vs. ein "Beweis"?
   - Confidence-Skala (z. B. niedrig/mittel/hoch) + Kriterien
7) Output-Format:
   - Überschriftenhierarchie sauber (H1–H3), klare Abschnitte, bullet points nur wo nötig
   - Kommandozeilen in Codeblöcken, mit Erklärzeilen darüber
   - Am Ende: komprimierte "Runbook"-Kurzfassung (1 Seite) + Tool-Matrix (Medientyp → Tool → Zweck)
8) Achte auf Compliance:
   - DSGVO/Vertraulichkeit, minimaler Datenabfluss, Logging ohne sensible Inhalte
   - Empfehlung für Offline-/Airgapped-Workflow, wenn {{RISK_LEVEL}} = hoch
9) Schreibe so, dass ein erfahrenes IT-Team es sofort nutzen kann.
   - Keine vagen Aussagen wie "prüfe mal" — stattdessen konkrete Checks, Schwellen, Beispiele.

LIEFERUMFANG (STRIKT)
A) Executive Summary (max. 12 Zeilen)
B) Playbook (Phasen A–E)
C) 30-Minuten-Triage-Checkliste
D) Dokumentationsvorlage
E) Runbook-Kurzfassung (1 Seite)
F) Tool-Matrix (Tabelle)

Starte direkt mit (A) und arbeite dich durch (F).
```

---

## Hinweise zur Nutzung (kurz)

- **Sicherheitsfokus:** Der Prompt ist explizit auf **Erkennung/Beweisführung** ausgelegt, nicht auf Verdeckung.  
- **Variablen:** Passe `{{SUSPECT_ASSETS}}` real an (Dateinamen, Typen, Ursprung).  
- **Timeboxing:** Mit `{{TIME_BUDGET_HOURS}}` steuert ihr, ob ihr eher triagiert oder tief analysiert.

---

## Optional: Team‑Workflow (Agentur‑Setup)

- **Rollen (Minimalbesetzung):**
  - Forensik/IR Lead (Workflow, Entscheidungen)
  - Analyst (Tooling, Artefakt-Parsing)
  - Technical Writer (Report/Executive Summary)
- **Quality Gate:** Jede "gefundenen Nachricht" muss **reproduzierbar** sein (Schritte + Hashes + Toolversionen dokumentiert).
