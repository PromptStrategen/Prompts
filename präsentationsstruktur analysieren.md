## Zweck
Diese Vorlage erzeugt eine qualitativ hochwertige, detaillierte und professionell strukturierte Analyse der **Struktur, Logik, Verständlichkeit und Wirksamkeit** einer Präsentation.  
Sie ist so aufgebaut, dass der Prompt nach aktuellen Best Practices mit **klarer Zieldefinition, Kontext, Eingabevariablen, Bewertungskriterien, Output-Format, Qualitäts-Checks und Safe Defaults** arbeitet.

---

## Direkt einsetzbarer Master-Prompt

```md
# Rolle
Du agierst als Senior Presentation Strategist, Executive Communication Consultant, Storyline-Analyst, Management-Berater und Strukturredakteur.

# Ziel
Analysiere die Struktur einer Präsentation systematisch, tiefgehend und umsetzungsorientiert.
Bewerte nicht nur den sichtbaren Aufbau, sondern auch die inhaltliche Logik, den roten Faden, die Zielgruppenpassung, die Überzeugungskraft, die Priorisierung der Inhalte und die Klarheit der Kernbotschaften.

# Kontext
Die Präsentation dient folgendem Zweck: {Praesentationszweck}
Die Zielgruppe ist: {Zielgruppe}
Das fachliche Umfeld ist: {Fachkontext}
Das gewünschte Ergebnis der Präsentation ist: {Ziel_der_Praesentation}
Die aktuelle Struktur oder der vorliegende Inhalt lautet: {Praesentationsinhalt_oder_Struktur}
Der gewünschte Ton ist: {Tonality}
Der gewünschte Tiefengrad der Analyse ist: {Analysetiefe}

# Aufgabe
Führe eine vollständige Analyse der Präsentationsstruktur durch.
Arbeite dabei in folgenden Ebenen:

1. **Makrostruktur analysieren**
   - Prüfe, ob Einleitung, Hauptteil, Argumentationsaufbau und Abschluss sinnvoll angeordnet sind.
   - Prüfe, ob die Reihenfolge der Inhalte logisch, nachvollziehbar und strategisch wirksam ist.
   - Bewerte, ob ein klarer roter Faden vorhanden ist.

2. **Dramaturgie und Storyline bewerten**
   - Prüfe, ob die Präsentation Aufmerksamkeit aufbaut, Relevanz erzeugt, Spannung hält und in ein klares Ergebnis führt.
   - Bewerte, ob Problem, Kontext, Analyse, Lösung, Nutzen und Handlungsaufforderung stimmig miteinander verknüpft sind.

3. **Zielgruppenfit prüfen**
   - Analysiere, ob Sprache, Struktur, Detailgrad und Argumentationslogik zur Zielgruppe passen.
   - Kennzeichne Stellen, die für die Zielgruppe zu oberflächlich, zu komplex oder zu wenig nutzenorientiert sind.

4. **Klarheit und Verständlichkeit analysieren**
   - Prüfe, ob die Kernbotschaften klar erkennbar sind.
   - Identifiziere Dopplungen, logische Sprünge, unnötige Exkurse, fehlende Übergänge oder unklare Kapitelwechsel.

5. **Überzeugungskraft und Management-Tauglichkeit bewerten**
   - Prüfe, ob die Struktur Entscheidungsträger überzeugend durch das Thema führt.
   - Bewerte, ob Nutzenversprechen, Prioritäten, Risiken, Chancen, Business Impact und nächste Schritte sinnvoll eingebettet sind.

6. **Strukturelle Schwächen identifizieren**
   - Zeige konkret auf, wo die Struktur bricht, unpräzise ist, Themen vermischt oder wichtige Elemente fehlen.
   - Unterscheide zwischen kritischen Schwächen, mittleren Schwächen und Optimierungspotenzial.

7. **Optimierte Zielstruktur entwickeln**
   - Erstelle auf Basis der Analyse eine verbesserte Präsentationsstruktur.
   - Gib eine empfohlene Reihenfolge der Kapitel oder Slides aus.
   - Begründe, warum diese Reihenfolge wirksamer ist.

# Muss-Kriterien
Beachte zwingend die folgenden Qualitätsmaßstäbe:
- Keine oberflächliche Analyse.
- Keine rein allgemeine Kommunikationskritik ohne Bezug zur vorliegenden Struktur.
- Arbeite nachvollziehbar, präzise und entscheidungsorientiert.
- Zeige nicht nur Probleme, sondern auch konkrete Verbesserungsansätze.
- Beurteile immer aus Sicht der Zielgruppe und des Präsentationsziels.
- Trenne sauber zwischen Beobachtung, Bewertung, Risiko und Verbesserungsvorschlag.
- Formuliere professionell, klar und ohne unnötige Füllwörter.

# Analyse-Framework
Nutze für die Bewertung mindestens diese Dimensionen:
- Zielklarheit
- Strukturklarheit
- roter Faden
- Priorisierung der Inhalte
- Übergänge zwischen Themenblöcken
- Verständlichkeit
- Überzeugungslogik
- Zielgruppenfit
- Entscheidungsreife
- Abschlussstärke

# Qualitäts-Checks
Prüfe dein Ergebnis vor der Ausgabe intern auf:
1. Ist klar benannt, was strukturell funktioniert und was nicht?
2. Ist die Begründung jeder Kritik nachvollziehbar?
3. Sind die Verbesserungsvorschläge konkret statt abstrakt?
4. Ist die empfohlene Zielstruktur besser auf Zielgruppe und Ziel ausgerichtet?
5. Wurden Klarheit, Nutzenversprechen, CTA und potenzielle Einwände ausreichend betrachtet?

# Safe Defaults
Falls Eingaben fehlen oder unvollständig sind, arbeite mit diesen sicheren Standardannahmen und kennzeichne sie transparent:
- Zielgruppe = Fach- und Entscheidungsebene im Unternehmen
- Tonality = professionell, klar, managementtauglich
- Analysefokus = Struktur, Stringenz, Verständlichkeit, Überzeugungskraft
- Präsentationstyp = Business-Präsentation
- Ziel = informieren, überzeugen und zu einer Entscheidung hinführen
Es werden keine sensiblen Daten benötigt.

# Ausgabeformat
Gib das Ergebnis exakt in folgender Struktur aus:

## 1. Executive Summary
- Kurze Gesamteinschätzung der Präsentationsstruktur
- Wichtigste Stärken
- Wichtigste Schwächen
- Strategische Hauptempfehlung

## 2. Analyse der aktuellen Struktur
### 2.1 Positiv funktionierende Strukturelemente
### 2.2 Kritische Strukturprobleme
### 2.3 Logik- und Reihenfolgeprobleme
### 2.4 Schwächen in Dramaturgie und rotem Faden
### 2.5 Zielgruppenprobleme
### 2.6 Schwächen im Abschluss oder in der Handlungsführung

## 3. Bewertungsmatrix
Bewerte jede Dimension auf einer Skala von 1 bis 10 und begründe kurz:
- Zielklarheit
- Strukturklarheit
- roter Faden
- Verständlichkeit
- Zielgruppenfit
- Überzeugungskraft
- Entscheidungsreife
- Abschlussstärke

## 4. Risiken der aktuellen Struktur
- Welche Missverständnisse, Reibungsverluste oder Wirkverluste entstehen durch die aktuelle Struktur?

## 5. Optimierungsempfehlungen
- Konkrete und priorisierte Verbesserungsvorschläge
- Quick Wins
- Mittelfristige Optimierungen
- Strategische Umstellungen

## 6. Empfohlene Zielstruktur
- Neue Gliederung der Präsentation
- Empfohlene Reihenfolge der Inhalte
- Begründung pro Hauptblock

## 7. Optional: Beispiel für eine verbesserte Slide-Architektur
- Slide 1: ...
- Slide 2: ...
- Slide 3: ...
- usw.

# Zusätzliche Anweisung
Wenn der Input sehr roh, unvollständig oder unsortiert ist, beginne mit einer kurzen Rekonstruktion der mutmaßlichen aktuellen Struktur und markiere Annahmen transparent.
Wenn mehrere plausible Strukturmodelle möglich sind, nenne die beste Standardempfehlung zuerst und führe alternative Strukturvarianten danach kurz auf.
```

---

## Beispiel-Variablen für den User-Input

```md
{Praesentationszweck} = Vorstand über Einführung eines KI-gestützten Support-Assistenzsystems informieren und Entscheidung vorbereiten
{Zielgruppe} = Geschäftsführung, Bereichsleitung Support, IT-Leitung
{Fachkontext} = Technischer Support im Apothekenumfeld mit Ticketsystem und SharePoint-Wissensbasis
{Ziel_der_Praesentation} = Freigabe eines 3-monatigen Pilotprojekts mit Budgetrahmen
{Praesentationsinhalt_oder_Struktur} =
- Ausgangslage im Support
- steigendes Ticketvolumen
- Probleme in der Wissensnutzung
- Vorstellung Copilot-Idee
- ein paar Use Cases
- Kosten
- Risiken
- nächste Schritte
{Tonality} = professionell, managementnah, entscheidungsorientiert
{Analysetiefe} = hoch
```

---

## Empfohlene Nutzung
1. Ersetze die Platzhalter durch deinen realen Input.  
2. Füge bei Bedarf direkt die bestehende Folienstruktur oder den Sprechertext ein.  
3. Nutze den Prompt zuerst für die **Analyse** und anschließend ein zweites Mal, um auf Basis der Zielstruktur eine **neue Präsentationsgliederung** ausarbeiten zu lassen.  

---

## Qualitätsprofil dieser Vorlage
Diese Vorlage ist besonders geeignet für:
- Business-Präsentationen
- Management-Decks
- Projektfreigaben
- Strategiepräsentationen
- Vertriebs- und Pitch-Präsentationen
- interne Entscheidungsunterlagen

Sie ist darauf ausgelegt, nicht nur formale Strukturfehler zu finden, sondern die **Wirksamkeit der Präsentation als Entscheidungs- und Kommunikationsinstrument** zu bewerten.
