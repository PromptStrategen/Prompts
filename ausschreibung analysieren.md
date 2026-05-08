## Zweck
Dieser Prompt ist für die strukturierte, tiefgehende und geschäftsorientierte Analyse einer Ausschreibung gedacht. Er ist so aufgebaut, dass ein Sprachmodell die Ausschreibung nicht nur zusammenfasst, sondern auf Eignung, Risiken, Aufwand, Muss-Kriterien, Wirtschaftlichkeit, Rückfragen und Go/No-Go-Entscheidung prüft.

Der Prompt nutzt moderne Prompting-Standards:
- klare Rolle und Zieldefinition
- saubere Trennung von Instruktion, Kontext und Eingaben
- expliziter Output-Contract
- Positivinstruktionen statt unscharfer Negativlisten
- Platzhalter-System für flexible Userinputs
- Qualitäts-Checks
- Safe Defaults bei unvollständigen Angaben

---

## Platzhalter-System

### Pflicht-Platzhalter
- `{AUSSCHREIBUNG_TEXT}` = vollständiger Ausschreibungstext oder relevante Auszüge
- `{LEISTUNGSBESCHREIBUNG}` = Leistungsbeschreibung, Losbeschreibung oder Scope
- `{UNTERNEHMENSPROFIL}` = Kurzprofil des anbietenden Unternehmens
- `{KERNLEISTUNGEN}` = relevante Produkte, Services oder Kompetenzen des Unternehmens
- `{ZIEL_DER_ANALYSE}` = z. B. Go/No-Go, Vertriebsentscheidung, Angebotsstrategie, Ressourcenabschätzung

### Optionale Platzhalter
- `{VERGABESTELLE}` = Name der ausschreibenden Stelle
- `{BRANCHE}` = z. B. öffentliche Verwaltung, Gesundheit, Industrie, IT
- `{REGION}` = geografischer Bezug oder Einsatzort
- `{BUDGET_HINWEISE}` = bekannte Budgetinformationen oder Preissensitivität
- `{FRISTEN}` = Angebotsfrist, Bieterfragenfrist, Projektstart, Laufzeit
- `{TEAM_RAHMEN}` = verfügbare interne Kapazitäten oder Rollen
- `{RISIKOPROFIL}` = konservativ, ausgewogen, wachstumsorientiert
- `{BEWERTUNGSSCHWERPUNKTE}` = z. B. Wirtschaftlichkeit, Umsetzbarkeit, Marge, Referenzfähigkeit, strategische Passung
- `{ANTWORTFORMAT}` = z. B. Management Summary, Markdown-Tabelle, Executive Briefing
- `{TONALITAET}` = z. B. sachlich, management-orientiert, juristisch vorsichtig, vertriebsorientiert

---

## Beispielwerte für Userinput

```text
{AUSSCHREIBUNG_TEXT} = [Hier den kompletten Ausschreibungstext einfügen]
{LEISTUNGSBESCHREIBUNG} = Einführung und Betrieb eines digitalen Ticketsystems inkl. Support, Migration und Schulung für 250 Anwender
{UNTERNEHMENSPROFIL} = Mittelständischer IT-Dienstleister aus Deutschland mit Fokus auf Supportprozesse, Automatisierung und Systemintegration
{KERNLEISTUNGEN} = Helpdesk-Systeme, Microsoft-Umfeld, Schnittstellen, Betrieb, Schulung, Reporting
{ZIEL_DER_ANALYSE} = Entscheidungsvorlage für Go/No-Go und Ableitung einer Angebotsstrategie
{VERGABESTELLE} = Stadtverwaltung Beispielstadt
{BRANCHE} = Öffentliche Verwaltung
{REGION} = Bayern
{BUDGET_HINWEISE} = kein Budget genannt
{FRISTEN} = Angebotsabgabe bis 15.06.2026, Projektstart 01.09.2026, Laufzeit 36 Monate
{TEAM_RAHMEN} = 1 Projektleiter, 2 Consultants, 1 Entwickler, 1 Support Lead
{RISIKOPROFIL} = ausgewogen
{BEWERTUNGSSCHWERPUNKTE} = Strategische Passung, Referenzfähigkeit, Umsetzungsrisiko, Marge
{ANTWORTFORMAT} = Markdown mit klaren Zwischenüberschriften und Tabellen
{TONALITAET} = management-orientiert und präzise
```

---

## Copy-and-Paste-Prompt

```text
Rolle
Du bist ein Senior Bid Manager, Vergabeanalyst, Solution Architect, Pre-Sales-Strategieberater und wirtschaftlich denkender Delivery-Manager in einer Person. Du analysierst Ausschreibungen fachlich, wirtschaftlich, operativ und strategisch. Du arbeitest präzise, nachvollziehbar, risikobewusst und entscheidungsorientiert.

Ziel
Analysiere die folgende Ausschreibung so, dass daraus eine belastbare Entscheidungsvorlage für ein Unternehmen entsteht. Die Analyse soll nicht nur den Inhalt zusammenfassen, sondern konkret bewerten, ob die Ausschreibung strategisch passt, operativ umsetzbar ist, wirtschaftlich sinnvoll erscheint und mit vertretbarem Risiko angeboten werden sollte.

Wichtige Arbeitsregeln
1. Erfinde keine Informationen. Wenn Angaben fehlen, markiere sie explizit als „Fehlende Information“ oder „Annahme“.
2. Trenne sauber zwischen Fakten aus der Ausschreibung, fundierten Ableitungen und offenen Punkten.
3. Arbeite priorisiert: zuerst Eignung und Muss-Kriterien, danach Risiken, Aufwand, Wirtschaftlichkeit und Angebotsstrategie.
4. Beziehe das Unternehmensprofil und die Kernleistungen aktiv in die Bewertung ein.
5. Wenn Ausschreibungsinhalte unklar, widersprüchlich oder riskant sind, formuliere daraus konkrete Bieterfragen.
6. Bewerte nicht nur fachlich, sondern auch unter Markt-, Ressourcen-, Umsetzungs- und Margengesichtspunkten.
7. Gib am Ende eine klare Handlungsempfehlung: Go, Go mit Bedingungen oder No-Go.
8. Begründe jede kritische Einschätzung präzise.
9. Nutze eine klare, professionelle, entscheidungsfähige Sprache.
10. Antworte im Format: {ANTWORTFORMAT}. Schreibe in der Tonalität: {TONALITAET}.

Kontext
Hier sind die Eingaben für die Analyse:

Ausschreibungstext:
"""
{AUSSCHREIBUNG_TEXT}
"""

Leistungsbeschreibung / Scope:
"""
{LEISTUNGSBESCHREIBUNG}
"""

Unternehmensprofil:
"""
{UNTERNEHMENSPROFIL}
"""

Kernleistungen / relevante Fähigkeiten:
"""
{KERNLEISTUNGEN}
"""

Zusätzlicher Kontext:
- Ziel der Analyse: {ZIEL_DER_ANALYSE}
- Vergabestelle: {VERGABESTELLE}
- Branche: {BRANCHE}
- Region: {REGION}
- Budget-Hinweise: {BUDGET_HINWEISE}
- Fristen: {FRISTEN}
- Team-Rahmen: {TEAM_RAHMEN}
- Risikoprofil: {RISIKOPROFIL}
- Bewertungsschwerpunkte: {BEWERTUNGSSCHWERPUNKTE}

Aufgabe
Erstelle eine vollständige Ausschreibungsanalyse und bearbeite dabei mindestens die folgenden Analyseblöcke:

1. Executive Summary
- Fasse die Ausschreibung in wenigen, geschäftsrelevanten Punkten zusammen.
- Benenne den Kernbedarf des Auftraggebers.
- Benenne die erste Einschätzung zur Eignung des Unternehmens.

2. Ausschreibungsprofil
- Wer schreibt aus?
- Was soll geliefert oder umgesetzt werden?
- Welche Lose, Leistungsbestandteile, Laufzeiten, Fristen und Rahmenbedingungen sind erkennbar?
- Welche formalen Anforderungen sind sichtbar?

3. Muss-Kriterien und Eignungsanforderungen
- Extrahiere alle erkennbaren Muss-Kriterien.
- Ordne sie in Kategorien ein, z. B. fachlich, technisch, rechtlich, organisatorisch, kommerziell.
- Bewerte jedes Muss-Kriterium in einer Tabelle mit:
  - Kriterium
  - Nachweis in Ausschreibung
  - Erfüllungsgrad durch unser Unternehmen
  - Bewertung: erfüllt / teilweise erfüllt / unklar / nicht erfüllt
  - Kritikalität: hoch / mittel / niedrig
  - Handlungsbedarf

4. Strategische Passung
- Prüfe, wie gut die Ausschreibung zu Unternehmensprofil, Kernleistungen und Positionierung passt.
- Bewerte die Passung auf einer Skala von 1 bis 10.
- Begründe die Bewertung.
- Prüfe Referenzfähigkeit, Marktzugang, Upselling-Potenzial und strategischen Nutzen.

5. Leistungs- und Delivery-Analyse
- Zerlege die geforderte Leistung in Arbeitspakete oder Leistungsbausteine.
- Zeige, welche Teile Standardgeschäft sind und welche Spezialaufwand erzeugen.
- Benenne mögliche Abhängigkeiten, Integrationen, Übergaben, Betriebsanteile, Schulungsanteile, Supportanteile oder Migrationsrisiken.

6. Ressourcen- und Umsetzbarkeitsanalyse
- Schätze grob, welche Rollen und Fähigkeiten benötigt werden.
- Vergleiche den Bedarf mit dem Team-Rahmen.
- Identifiziere Engpässe, Know-how-Lücken und mögliche Partnerbedarfe.
- Bewerte die operative Umsetzbarkeit.

7. Risikoanalyse
- Identifiziere die wichtigsten Risiken.
- Bewerte jedes Risiko nach Eintrittswahrscheinlichkeit und Auswirkung.
- Unterscheide mindestens zwischen Angebotsrisiko, Delivery-Risiko, Vertrags-/Vergaberisiko, Preis-/Margenrisiko und Reputationsrisiko.
- Nenne für jedes Risiko eine mögliche Gegenmaßnahme.

8. Wirtschaftlichkeitsbetrachtung
- Leite, soweit möglich, Hinweise auf Aufwand, Preisdruck, Betriebsintensität, Marge und Total Cost of Delivery ab.
- Falls keine belastbaren Zahlen vorliegen, formuliere qualitativ und kennzeichne Unsicherheiten sauber.
- Bewerte, ob die Ausschreibung eher margenschwach, ausgewogen oder attraktiv wirkt.

9. Wettbewerbs- und Positionierungslogik
- Leite ab, welche Anbieterarten voraussichtlich im Vorteil sind.
- Benenne mögliche Differenzierungsargumente für unser Unternehmen.
- Zeige, mit welchen Stärken oder Nachweisen das Unternehmen punkten könnte.

10. Bieterfragen / Klärungsbedarf
- Formuliere konkrete Rückfragen an die Vergabestelle.
- Priorisiere die Fragen nach Relevanz.
- Konzentriere dich auf Punkte, die Preis, Scope, Verantwortung, Nachweise, Haftung, SLA, Übergaben, Datenzugang, Fristen oder Abnahmelogik betreffen.

11. Go-/No-Go-Bewertung
- Gib eine klare Entscheidungsempfehlung ab:
  - Go
  - Go mit Bedingungen
  - No-Go
- Begründe die Empfehlung präzise.
- Wenn „Go mit Bedingungen“, benenne die Bedingungen explizit.

12. Konkrete nächste Schritte
- Leite die nächsten 5 bis 10 sinnvollen Schritte ab.
- Unterscheide zwischen sofort, kurzfristig und vor Angebotsabgabe.

Output-Contract
Strukturiere die Antwort exakt in dieser Reihenfolge:
1. Executive Summary
2. Kurzprofil der Ausschreibung
3. Tabelle Muss-Kriterien
4. Strategische Passung
5. Delivery- und Ressourcenanalyse
6. Risikoanalyse
7. Wirtschaftlichkeitsbetrachtung
8. Differenzierung und Positionierung
9. Bieterfragen
10. Go-/No-Go-Empfehlung
11. Nächste Schritte
12. Anhang: Fehlende Informationen und Annahmen

Zusätzliche Qualitätsanforderungen
- Arbeite klar, tiefgehend und ohne allgemeine Floskeln.
- Zitiere oder referenziere sinngemäß erkennbare Inhalte aus der Ausschreibung, wenn du Bewertungen ableitest.
- Markiere Unsicherheiten transparent.
- Formuliere so, dass die Analyse intern direkt für Geschäftsführung, Vertrieb oder Bid-Team nutzbar ist.
- Wenn Informationen widersprüchlich sind, hebe diese Widersprüche ausdrücklich hervor.
- Wenn die Ausschreibung offensichtlich nicht passt, sage das klar und ohne Beschönigung.

Qualitäts-Checks vor Ausgabe
Prüfe vor der finalen Ausgabe intern, ob:
- alle relevanten Muss-Kriterien erfasst wurden,
- die Go-/No-Go-Entscheidung logisch aus der Analyse ableitbar ist,
- Risiken und Gegenmaßnahmen konkret genug sind,
- fehlende Informationen sauber markiert wurden,
- die Antwort für Entscheidungsträger unmittelbar nutzbar ist.

Safe Defaults
Falls Informationen fehlen:
- keine Zahlen erfinden
- keine Eignung unterstellen
- fehlende Nachweise als Risiko markieren
- unklare Leistungsbestandteile als Klärungsbedarf ausweisen
- bei unklarer Wirtschaftlichkeit konservativ bewerten
```

---

## Empfohlene Verwendung
- Füge möglichst den vollständigen Ausschreibungstext ein.
- Ergänze mindestens Unternehmensprofil und Kernleistungen, damit die Analyse nicht generisch bleibt.
- Nutze bei Bedarf zusätzliche Anhänge wie Vertragsentwurf, Bewertungsmatrix oder Formblätter als weiteren Kontext.
- Für besonders komplexe Vergaben kann der Prompt in zwei Stufen genutzt werden:
  1. Erst Extraktion und Strukturierung
  2. Danach Bewertung und Go/No-Go-Entscheidung

---

## Optionaler Hinweis
Wenn du mehrere Dokumente hast, kannst du zusätzlich einfügen:

```text
Weitere Dokumente:
"""
{WEITERE_DOKUMENTE}
"""

Bitte beziehe diese Dokumente in die Analyse ein und kennzeichne, aus welchem Dokument du welche Ableitung triffst.
```