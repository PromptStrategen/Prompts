## Ziel des Prompts
Dieser Prompt erzeugt einen qualitativ hochwertigen, ausführlichen, strategisch belastbaren und operativ umsetzbaren **Jahresstrategieplan für eine Ausbildung**.  
Er ist nach modernen Prompting-Prinzipien aufgebaut: **klare Zieldefinition, definierte Rolle, expliziter Kontext, strukturierte Eingaben, konkrete Deliverables, Qualitäts-Checks, Safe Defaults und ein eindeutiger Output-Contract**.

---

## Empfohlene Nutzung
Diesen Prompt nutzt du, wenn du für eine Ausbildung einen vollständigen Jahresplan entwickeln willst, zum Beispiel für:
- Fachinformatiker/in Systemintegration
- Fachinformatiker/in Anwendungsentwicklung
- Kaufmännische Ausbildung
- Technische Ausbildung
- Interne Onboarding- und Entwicklungsprogramme

---

## Platzhalter-System für Userinput
Nutze die folgenden Variablen als Eingabeparameter. Nicht bekannte Werte können durch die vorgeschlagenen Beispielwerte oder durch `unbekannt` ersetzt werden.

### Kernvariablen
- `{Ausbildungsberuf}` – Beispiel: Fachinformatiker/in für Systemintegration
- `{Ausbildungsjahr}` – Beispiel: 1. Ausbildungsjahr
- `{Zeitraum}` – Beispiel: 01.08.2026 bis 31.07.2027
- `{Unternehmenstyp}` – Beispiel: mittelständisches IT-Dienstleistungsunternehmen
- `{Abteilung}` – Beispiel: Beispiel Abteilung
- `{Vorkenntnisse}` – Beispiel: Grundlagen in Windows, Hardware und einfache Netzwerkkonzepte
- `{Lernniveau}` – Beispiel: Anfänger mit erster Praxiserfahrung
- `{Zielkompetenzen}` – Beispiel: Kundenkommunikation, Ticketbearbeitung, Hardwarediagnose, Netzwerkanalyse, Dokumentation
- `{Prüfungsbezug}` – Beispiel: IHK-Zwischenprüfung und betriebliche Praxisanforderungen
- `{Unternehmensziele}` – Beispiel: schnellere operative Einsatzfähigkeit, saubere Dokumentation, höhere Selbstständigkeit
- `{Praxisaufgaben}` – Beispiel: Supportfälle begleiten, Geräte vorbereiten, Peripherie anbinden, Checklisten pflegen
- `{ToolsSysteme}` – Beispiel: Ticketsystem, Active Directory, Windows 11, Netzwerkanalyse-Tools
- `{LernzeitProWoche}` – Beispiel: 4 Stunden strukturierte Lernzeit pro Woche
- `{Betreuungsintensität}` – Beispiel: eng begleitet im ersten Quartal, danach schrittweise mehr Eigenverantwortung
- `{Stärken}` – Beispiel: hohe Lernbereitschaft, höfliche Kommunikation, technisches Interesse
- `{Entwicklungsfelder}` – Beispiel: Priorisierung, saubere Fehleranalyse, Dokumentationsqualität
- `{Rahmenbedingungen}` – Beispiel: regulärer Arbeitsalltag, begrenzte Lernfenster, reale Supportfälle haben Priorität
- `{Tonality}` – Beispiel: professionell, klar, motivierend, praxisnah

### Optionale Zusatzvariablen
- `{Standort}` – Beispiel: Berlin
- `{Berufsschulrhythmus}` – Beispiel: Blockunterricht oder 1–2 Berufsschultage pro Woche
- `{Stakeholder}` – Beispiel: Ausbilder, Teamleitung, Berufsschule, Fachbereiche
- `{Erfolgskriterien}` – Beispiel: messbare Kompetenzzuwächse pro Quartal, steigende Selbstständigkeit, weniger Rückfragen bei Standardaufgaben
- `{Risiken}` – Beispiel: Überforderung, fehlende Lernroutine, zu wenig Praxisreflexion
- `{BesondereSchwerpunkte}` – Beispiel: Kundenkontakt, Fehlerdiagnose, Systemverständnis, Prüfungsrelevanz

---

## Beispiel-Variablenbelegung
```text
{Ausbildungsberuf} = Fachinformatiker/in für Systemintegration
{Ausbildungsjahr} = 1. Ausbildungsjahr
{Zeitraum} = 01.08.2026 bis 31.07.2027
{Unternehmenstyp} = mittelständisches IT-Unternehmen
{Abteilung} = Beispiel Abteilung
{Vorkenntnisse} = erste Grundlagen in Windows, Hardware und Tickets
{Lernniveau} = Anfänger mit leichter Praxiserfahrung
{Zielkompetenzen} = Supportverständnis, technische Diagnose, Dokumentation, Kundenkommunikation, selbstständige Bearbeitung einfacher Fälle
{Prüfungsbezug} = IHK-relevante Grundlagen und betriebliche Einsatzfähigkeit
{Unternehmensziele} = schneller produktiver Einsatz, bessere Servicequalität, sauberere Übergaben
{Praxisaufgaben} = Geräte aufsetzen, Support begleiten, Peripherie prüfen, Checklisten nutzen
{ToolsSysteme} = Ticketsystem, Windows 11, Active Directory, Netzwerktools
{LernzeitProWoche} = 4 Stunden
{Betreuungsintensität} = hoch in Q1, mittel in Q2, reduziert ab Q3
{Stärken} = lernwillig, freundlich, zuverlässig
{Entwicklungsfelder} = Fehleranalyse, Priorisierung, technische Tiefe
{Rahmenbedingungen} = operative Aufgaben haben Vorrang, Lernzeit muss realistisch planbar sein
{Tonality} = professionell, praxisnah, motivierend
```

---

## Der Prompt
```text
Rolle
Du agierst als erfahrener Ausbildungsstratege, Lernarchitekt, Fachdozent, Teamleiter, betrieblicher Ausbilder und Organisationsentwickler. Du kombinierst didaktische Qualität, betriebliche Umsetzbarkeit, Kompetenzaufbau, Prüfungsorientierung und strategische Personalentwicklung.

Ziel
Erstelle einen qualitativ höchstmöglichen, ausführlichen, detailtiefen und operativ umsetzbaren jährlichen Strategieplan für die Ausbildung im Kontext von {Ausbildungsberuf} im {Ausbildungsjahr} für den Zeitraum {Zeitraum}.

Kontext
Die Ausbildung findet in folgendem Umfeld statt:
- Unternehmenstyp: {Unternehmenstyp}
- Abteilung/Bereich: {Abteilung}
- Lernniveau: {Lernniveau}
- Vorkenntnisse: {Vorkenntnisse}
- Zielkompetenzen: {Zielkompetenzen}
- Prüfungsbezug: {Prüfungsbezug}
- Unternehmensziele: {Unternehmensziele}
- Praxisaufgaben: {Praxisaufgaben}
- Tools und Systeme: {ToolsSysteme}
- Lernzeit pro Woche: {LernzeitProWoche}
- Betreuungsintensität: {Betreuungsintensität}
- Stärken: {Stärken}
- Entwicklungsfelder: {Entwicklungsfelder}
- Rahmenbedingungen: {Rahmenbedingungen}
- Optionale Stakeholder: {Stakeholder}
- Optionale Risiken: {Risiken}
- Optionale besondere Schwerpunkte: {BesondereSchwerpunkte}
- Gewünschte Tonalität: {Tonality}

Arbeitsprinzipien
1. Arbeite ergebnisorientiert, konkret und praxisnah.
2. Triff nur dann Annahmen, wenn Informationen fehlen. Kennzeichne Annahmen transparent.
3. Nutze sinnvolle Safe Defaults, wenn Angaben fehlen.
4. Richte den Plan auf reale Ausbildungswirksamkeit, Alltagstauglichkeit und Kompetenzzuwachs aus.
5. Verbinde operative Praxis, Lernziele, Reflexion und Prüfungsrelevanz.
6. Formuliere so, dass der Plan direkt von Ausbildern, Teamleitungen oder Ausbildungsbeauftragten eingesetzt werden kann.
7. Vermeide unnötige Allgemeinplätze. Liefere stattdessen belastbare, klare und priorisierte Inhalte.

Aufgabe
Erstelle einen vollständigen Jahresstrategieplan für die Ausbildung und decke dabei mindestens die folgenden Elemente ab:

1. Ausgangsanalyse
- Bewerte die Ausgangslage der Ausbildung.
- Leite Chancen, Risiken, Engpässe und Erfolgshebel ab.
- Zeige, welche Faktoren den Ausbildungserfolg im gegebenen Umfeld am stärksten beeinflussen.

2. Strategische Leitziele für das Ausbildungsjahr
- Formuliere 5 bis 8 klare Jahresziele.
- Ordne jedes Ziel einem Nutzen für den Azubi und einem Nutzen für das Unternehmen zu.
- Kennzeichne Prioritäten.

3. Kompetenzmodell
- Strukturiere die Entwicklung in Fachkompetenz, Methodenkompetenz, Sozialkompetenz und Selbstkompetenz.
- Definiere je Kompetenzfeld die Soll-Entwicklung für das Jahr.
- Leite konkrete Lern- und Praxisfelder ab.

4. Quartalsstrategie
- Teile das Jahr in vier Quartale auf.
- Definiere pro Quartal Fokus, Ziele, Lerninhalte, Praxisanteile, Verantwortungsgrad und gewünschte Ergebnisse.
- Beschreibe die logische Lernprogression von enger Begleitung hin zu mehr Selbstständigkeit.

5. Monats- oder Phasenplan
- Breche die Quartalsstrategie in greifbare Monats- oder Phasenblöcke herunter.
- Benenne pro Phase konkrete Themen, Aufgaben, Lernziele, Übungen, Reflexionspunkte und erwartete Deliverables.

6. Praxisintegration
- Zeige, wie reale Aufgaben aus dem Arbeitsalltag systematisch als Lernfeld genutzt werden können.
- Verknüpfe Theorie, Praxis, Dokumentation und Feedback.
- Gib Beispiele für geeignete Praxisaufgaben mit wachsendem Schwierigkeitsgrad.

7. Betreuungs- und Feedbacksystem
- Lege fest, wie häufig Feedback stattfinden sollte.
- Definiere Formate für Tagesfeedback, Wochenreflexion, Monatsreview und Quartalsgespräch.
- Zeige, wie Lob, Korrektur, Zielschärfung und Eigenverantwortung sinnvoll kombiniert werden.

8. Lernmethodik
- Empfiehl geeignete Lernmethoden für das genannte Lernniveau.
- Berücksichtige Wiederholung, praktische Anwendung, Mini-Projekte, Shadowing, Checklisten, Selbsttests und Transferaufgaben.

9. Prüfungs- und Leistungsbezug
- Zeige, wie betriebliche Lernziele mit dem Prüfungsbezug verbunden werden.
- Markiere, welche Inhalte eher betriebspraktisch und welche eher prüfungsrelevant sind.
- Empfiehl einen realistischen Vorbereitungsrhythmus.

10. KPI- und Fortschrittslogik
- Definiere messbare Indikatoren für Lernfortschritt und Einsatzfähigkeit.
- Nutze qualitative und quantitative KPIs.
- Beispiele: Bearbeitungsqualität, Dokumentationsniveau, Selbstständigkeit, Rückfragequote, Fehlerquote, Kommunikationsqualität.

11. Risiko- und Gegenmaßnahmenplan
- Identifiziere typische Risiken im Jahresverlauf.
- Leite zu jedem Risiko konkrete Gegenmaßnahmen ab.
- Priorisiere nach Eintrittswahrscheinlichkeit und Auswirkung.

12. Maßnahmenplan für Ausbilder und Team
- Zeige, was Ausbilder, Teamleitung und Fachkollegen konkret beitragen sollten.
- Leite Unterstützungsmaßnahmen, Review-Routinen und Enablement-Aufgaben ab.

13. Abschlussbewertung
- Fasse zusammen, wie der Plan den Azubi fachlich, methodisch und organisatorisch voranbringt.
- Gib eine klare Management-Einschätzung zur Umsetzbarkeit.
- Nenne die 5 wichtigsten Hebel für den Erfolg.

Ausgabeformat
Gib das Ergebnis in der folgenden Struktur aus:

# Jährlicher Strategieplan für die Ausbildung
## 1. Management Summary
## 2. Ausgangsanalyse
## 3. Strategische Jahresziele
## 4. Kompetenzmodell
## 5. Quartalsstrategie
## 6. Monats- bzw. Phasenplanung
## 7. Praxisintegration
## 8. Betreuungs- und Feedbacksystem
## 9. Lernmethodik
## 10. Prüfungsbezug
## 11. KPI-System
## 12. Risiken und Gegenmaßnahmen
## 13. Maßnahmen für Ausbilder und Team
## 14. Fazit und Prioritäten

Zusätzliche Qualitätsanforderungen
- Schreibe in sauberem, professionellem Deutsch.
- Liefere keine oberflächliche Übersicht, sondern eine belastbare Endfassung.
- Arbeite mit klaren Zwischenüberschriften, Tabellen und priorisierten Listen, wo sinnvoll.
- Zeige nachvollziehbare Begründungen für Prioritäten und Maßnahmen.
- Achte auf hohe Praxisnähe und Umsetzbarkeit im Betriebsalltag.
- Markiere Annahmen eindeutig.
- Nenne bei jeder größeren Empfehlung den erwarteten Nutzen.

Qualitäts-Checks vor der finalen Ausgabe
Prüfe die Antwort intern vor der Ausgabe auf folgende Punkte:
1. Klarheit: Sind alle Aussagen eindeutig, verständlich und nicht zu allgemein?
2. Vollständigkeit: Sind Strategie, Operative, Betreuung, KPIs und Risiken vollständig abgedeckt?
3. Nutzenversprechen: Wird klar, warum der Plan dem Azubi und dem Unternehmen hilft?
4. Realismus: Ist die Planung mit dem Betriebsalltag vereinbar?
5. Priorisierung: Sind die wichtigsten Maßnahmen klar hervorgehoben?
6. Prüfungs- und Praxisbezug: Sind beide Perspektiven sinnvoll integriert?
7. Handlungsorientierung: Kann der Plan direkt verwendet werden?
8. Einwände: Wurden mögliche Hürden wie Zeitmangel, Überforderung oder fehlende Routine mitgedacht?

Safe Defaults
Falls einzelne Eingaben fehlen, nutze folgende Standardannahmen und kennzeichne sie als Annahme:
- Lernniveau = Einsteiger mit begrenzter Praxiserfahrung
- Betreuungsintensität = hoch im ersten Quartal, danach schrittweise reduziert
- Lernzeit pro Woche = 3 bis 4 Stunden strukturierte Lernzeit
- Ziel = Steigerung von Selbstständigkeit, Fachverständnis und sauberer Arbeitsweise
- Prüfungsbezug = allgemeine Ausbildungs- und IHK-Orientierung, sofern relevant
- Rahmenbedingungen = Ausbildung findet parallel zum Tagesgeschäft statt

Wichtige Arbeitsanweisung
Falls Informationen fehlen, stelle nicht unnötig viele Rückfragen, sondern arbeite mit den Safe Defaults, mache die Annahmen transparent und liefere trotzdem eine hochwertige, vollständige und umsetzbare Endfassung.
```

---

## Qualitäts-Checks für den Prompt selbst
Dieser Prompt ist so aufgebaut, dass er folgende Qualitätskriterien erfüllt:

- **Klarheit:** Rolle, Ziel, Kontext und Ausgabe sind eindeutig definiert.
- **Nutzenversprechen:** Der Output soll direkt im Ausbildungsalltag einsetzbar sein.
- **CTA/Arbeitsrichtung:** Das Modell wird aktiv zur vollständigen Endfassung und zu umsetzbaren Maßnahmen geführt.
- **Einwandbehandlung:** Typische Hürden wie fehlende Informationen, Zeitmangel oder Überforderung werden abgefedert.
- **Safe Defaults:** Fehlende Daten blockieren die Bearbeitung nicht.
- **Strukturqualität:** Management Summary, Quartalslogik, KPI-System und Risikoplan sind fest eingebaut.

---

## Empfehlung für die praktische Anwendung
Für die höchste Ergebnisqualität:
1. Trage zuerst die Variablen möglichst konkret ein.
2. Nutze echte Praxisaufgaben und reale Rahmenbedingungen.
3. Lass den ersten Entwurf erzeugen.
4. Optimiere im zweiten Durchlauf gezielt einzelne Abschnitte, zum Beispiel nur das KPI-System, nur die Quartalsstrategie oder nur die Feedbacklogik.
