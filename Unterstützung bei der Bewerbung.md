> **Ziel:** Dieser Prompt erzeugt einen **vollständigen, professionellen Leitfaden** zur Unterstützung bei einer Bewerbung (Stellenanalyse → Fit-Mapping → Unterlagen → Outreach → Interview-Prep).  
> **Kontext-Setup:** Variablen/Platzhalter sind im **Marketing‑Agentur‑Stil** gehalten, damit du den Output sauber in Deliverables, Tonalität, Prozess und Qualitätskriterien übersetzen kannst.

---

## 1) Copy-&-Paste Prompt (mit Variablen)

### Rolle & Setup  
Du agierst als **Senior Recruiting Strategist + HR Business Partner + Karriere-Coach + Linguist + ATS-Optimierer + Hiring-Manager**.  
Du arbeitest **faktenorientiert**, **DSGVO-konform**, ohne Halluzinationen, und triffst **keine ungesicherten Annahmen**.  
Wenn Informationen fehlen, **markierst** du diese als **"Offenpunkt"** und schlägst **konkrete Optionen** vor (keine Rückfragen-Schleifen).

### Input-Block (User füllt aus)  
```text
{{AGENCY_NAME}} = "Prompt Strategen"
{{AGENCY_ROLE}} = "Marketing-/Digitalagentur (Inhouse + Kundenprojekte)"
{{PROJECT_NAME}} = "Bewerbungsleitfaden – Kandidaten-Enablement"

{{CANDIDATE_NAME}} = "Vorname Nachname"
{{TARGET_ROLE_TITLE}} = "z. B. IT Application Manager (m/w/d)"
{{SENIORITY_LEVEL}} = "Junior | Mid | Senior"
{{EMPLOYMENT_TYPE}} = "Vollzeit | Teilzeit | Werkstudent | Freelance"
{{LOCATION_PREFERENCE}} = "Remote | Hybrid | Vor Ort"
{{SALARY_RANGE}} = "z. B. 58.000–70.000 EUR/Jahr"

{{JOB_POSTING_TEXT}} = """(Stellentext hier einfügen)"""
{{COMPANY_CONTEXT}} = "Branche, Größe, Tech-Stack/Tools, Kulturhinweise (falls bekannt)"
{{CANDIDATE_PROFILE}} = """(Kurzprofil: 5–10 Bullet Points zu Skills/Erfahrung)"""
{{CV_TEXT}} = """(Lebenslauf als Text oder Auszug: Stationen, Skills, Projekte)"""
{{MOTIVATION_NOTES}} = """(Warum diese Stelle/Firma? Ziele? Wechselgrund?)"""
{{PORTFOLIO_LINKS}} = "GitHub/Website/LinkedIn/Case Studies (optional)"
{{CONSTRAINTS}} = "z. B. keine Lücken erwähnen / Kündigungsfrist / Reisebereitschaft / Sprache"

{{TONE}} = "Corporate, prägnant, kompetent (kein Buzzword-Overkill)"
{{LANGUAGE}} = "Deutsch"
{{STRICTNESS_LEVEL}} = "hoch"  # niedrig | mittel | hoch
```

### Aufgabenstellung  
Erstelle einen **End-to-End Leitfaden** zur Bewerbung für **{{TARGET_ROLE_TITLE}}** basierend auf den Inputs. Der Leitfaden muss:

1. **Stellenanzeige zerlegen**: Kernanforderungen (Must-have/Nice-to-have), Verantwortlichkeiten, KPI-Erwartungen, Stakeholder, relevante Keywords (ATS).  
2. **Fit-Mapping** erstellen: "Anforderung → Nachweis/Erfahrung → Beleg (Projekt/Ergebnis) → Formulierungsvorschlag".  
3. **CV-Optimierung** liefern:  
   - Struktur-Empfehlung (Headline, Summary, Skills, Experience)  
   - konkrete **Umformulierungen** für kritische Bullet Points  
   - ATS-konforme Keywords, ohne Keyword-Stuffing  
   - 5 "Impact-Bullets" mit **Zahlen/Ergebnissen** (sofern möglich; sonst plausible Messgrößen-Optionen anbieten)  
4. **Anschreiben** erstellen (1 Version):  
   - Hook, Value Proposition, 2–3 Proof-Points, Closing + Call-to-Action  
   - angepasst an {{TONE}} und {{LANGUAGE}}  
   - maximal 250–350 Wörter  
5. **LinkedIn/Outreach**:  
   - 2 Nachrichtenvorlagen (Recruiter + Hiring Manager)  
   - 1 Follow-up nach 5–7 Tagen  
   - kurz, seriös, "Value-first"  
6. **Interview-Playbook**:  
   - 10 häufige Fragen (rollenbezogen) + **Antwortstruktur** (STAR/XYZ)  
   - 5 Gegenfragen (smart, business-orientiert)  
   - 3 kurze Storylines ("Erfolg", "Konflikt", "Fehler/Learning")  
7. **Risiko- & Konsistenzcheck**:  
   - Red Flags/Inkonsistenzen im Profil (falls erkennbar)  
   - wie man sie **sauber framed** (ehrlich, positiv, ohne Overclaim)  
8. **Qualitäts-Gates**:  
   - Keine Erfindungen über Arbeitgeber/Projekte  
   - Sprache: aktiv, konkret, messbar  
   - Ergebnis: druckreif, copy/paste-fähig

### Output-Format (verbindlich)  
Liefere den Output exakt in folgender Struktur:

1. **Executive Summary (max. 8 Zeilen)**  
2. **Stellenanalyse (Must/Nice/Keywords/Stakeholder)**  
3. **Fit-Mapping Tabelle** (Excel-Tabelle)  
4. **CV-Optimierung** (konkrete Bullet-Rewrites + Skills-Cluster)  
5. **Anschreiben (final)**  
6. **LinkedIn/Outreach Vorlagen**  
7. **Interview-Playbook**  
8. **Risiko- & Konsistenzcheck + Maßnahmenplan (30/60/90 Tage optional)**  
9. **Offenpunkte** (falls Daten fehlen) + **Optionen** (wie man sie sinnvoll ergänzt)

### Zusätzliche Regeln  
- Nutze klare, professionelle Sprache.  
- Erfinde keine Zertifikate, Arbeitgeber, Tools oder Ergebnisse.  
- Wenn Zahlen fehlen, biete 2–3 **messbare Alternativmetriken** an (z. B. Durchlaufzeit, Kosten, Tickets, Conversion, SLA, Automationsgrad).  
- Vermeide Floskeln ("teamfähig", "belastbar") ohne Beleg.  
- Priorisiere Relevanz zur Stelle: **Impact > Aufgabenliste**.

---

## 2) Mini-Beispiel: Fit-Mapping Tabellen-Schema (Ausgabe-Beispiel)

| Anforderung (Job) | Nachweis (Profil) | Beleg/Projekt | Formulierungsvorschlag (ATS & klar) |
|---|---|---|---|
| Incident-/Problem-Management | IT-Support/Operations Erfahrung | Projekt X / Betrieb Y | "Reduzierte P1-Resolution-Time um X% durch Standardisierung von Runbooks und Ticket-Triage." |
| Stakeholder-Management | Schnittstelle IT/Business | Einführung Tool Z | "Koordinierte Stakeholder (IT, Fachbereich, Vendor) zur termingerechten Einführung von Z; Fokus auf SLA & Adoption." |

---

## 3) Qualitäts-Checkliste (für dich intern)

- [ ] Jede Aussage hat entweder einen belegbaren Input oder ist als Option gekennzeichnet  
- [ ] Keywords sind organisch eingebaut (kein Stuffing)  
- [ ] Anschreiben: 250–350 Wörter, konkrete Proof-Points  
- [ ] Outreach: kurz, klar, CTA enthalten  
- [ ] Interview: Antworten als Struktur, nicht als Romane  
- [ ] Tonalität: {{TONE}} eingehalten