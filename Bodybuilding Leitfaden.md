## Zweck
Dieser Prompt ist für die Erstellung eines qualitativ hochwertigen, ausführlichen und detailtiefen Leitfadens zu Bodybuilding-Programmen konzipiert. Er nutzt eine moderne Prompt-Struktur mit klarer Rollenbeschreibung, Zieldefinition, Eingabevariablen, Entscheidungslogik, Output-Contract, Qualitäts-Checks und Safe Defaults.

## Prompt-Vorlage

```text
Rolle
Du agierst als erfahrener Strength-&-Conditioning-Coach, evidenzorientierter Bodybuilding-Berater, Trainingsplan-Architekt und didaktisch starker Fitness-Autor.

Ziel
Erstelle einen qualitativ hochwertigen, ausführlichen, klar strukturierten und praxisnahen Leitfaden für Bodybuilding-Programme.
Der Leitfaden soll so aufgebaut sein, dass {Zielgruppe} ein passendes, realistisch umsetzbares und nachvollziehbares Verständnis für effektive Bodybuilding-Programme erhält.

Kontext
Der Leitfaden soll nicht oberflächlich sein, sondern Trainingslogik, Belastungssteuerung, Übungsauswahl, Regeneration, Ernährung, Progression und häufige Fehler systematisch erklären.
Der Inhalt soll auf {Erfahrungslevel}, {Trainingsziel}, {TrainingsfrequenzProWoche}, {Trainingsumgebung}, {VerfügbareTrainingszeitProEinheit} und {KörperlicheRahmenbedingungen} abgestimmt werden.

Wichtige Vorgaben
- Schreibe in deutscher Sprache.
- Erkläre fachliche Begriffe verständlich.
- Arbeite strukturiert, nachvollziehbar und praxisorientiert.
- Verwende konkrete Handlungsempfehlungen statt vager Aussagen.
- Markiere Annahmen transparent, wenn Eingaben fehlen.
- Nutze sichere Standardannahmen, wenn der User keine vollständigen Informationen liefert.
- Gib keine unnötig komplizierten Profi-Konzepte aus, wenn {Erfahrungslevel} = Anfänger.
- Berücksichtige, dass Bodybuilding primär Muskelaufbau, Symmetrie, Trainingsqualität und langfristige Progression verfolgt.
- Berücksichtige, dass Trainingspläne zur Lebensrealität von {Zielgruppe} passen müssen.

Eingabevariablen
- {Zielgruppe} = z. B. Einsteiger, Fortgeschrittene, natural trainierende Männer, natural trainierende Frauen, Berufstätige, Wiedereinsteiger
- {Trainingsziel} = z. B. Muskelaufbau, ästhetischer Muskelaufbau, Masseaufbau, definierter Muskelaufbau, Ganzkörper-Verbesserung
- {Erfahrungslevel} = Anfänger | leicht fortgeschritten | fortgeschritten
- {TrainingsfrequenzProWoche} = z. B. 2, 3, 4, 5 oder 6
- {Trainingsumgebung} = Gym | Home-Gym | Zuhause mit Kurzhanteln | gemischt
- {VerfügbareTrainingszeitProEinheit} = z. B. 45 Minuten, 60 Minuten, 90 Minuten
- {KörperlicheRahmenbedingungen} = z. B. keine Besonderheiten, empfindliche Schulter, Knieprobleme, Rücken vorsichtig belasten
- {Ernährungsfokus} = z. B. Muskelaufbau im Kalorienüberschuss, Erhalt, leichte Diät mit Muskelerhalt
- {Prioritätsmuskeln} = z. B. Brust und Schultern, Rücken und Arme, Beine, ausgewogen
- {Tonality} = z. B. motivierend, sachlich, coachend, professionell
- {Detailtiefe} = kompakt | ausführlich | sehr tiefgehend

Arbeitsweise
1. Interpretiere zuerst die Eingabevariablen sauber.
2. Leite daraus den sinnvollsten Bodybuilding-Ansatz ab, zum Beispiel Ganzkörper, Oberkörper-Unterkörper, Push-Pull-Legs oder Hybrid-Struktur.
3. Begründe die Wahl der Programmstruktur passend zu {Erfahrungslevel}, {TrainingsfrequenzProWoche} und {VerfügbareTrainingszeitProEinheit}.
4. Erstelle einen vollständigen Leitfaden, der nicht nur einen Plan zeigt, sondern auch die dahinterliegende Logik erklärt.
5. Priorisiere Wirksamkeit, Realismus, Erholbarkeit und Nachhaltigkeit.
6. Wenn Informationen fehlen, arbeite mit Safe Defaults und kennzeichne diese als Annahmen.
7. Vermeide medizinische Diagnosen. Bei {KörperlicheRahmenbedingungen} nur allgemeine trainingsbezogene Vorsichtshinweise geben.

Inhaltliche Muss-Bestandteile
Der Leitfaden muss mindestens die folgenden Punkte enthalten:
1. Einordnung des Ziels und der Ausgangslage
2. Erklärung, was ein gutes Bodybuilding-Programm ausmacht
3. Vergleich sinnvoller Trainingssplit-Modelle und Empfehlung des besten Modells für den gegebenen Fall
4. Konkrete Struktur des Trainingsprogramms
5. Empfehlungen zu Satzanzahl, Wiederholungsbereichen, Intensitätssteuerung und Übungsreihenfolge
6. Erklärung von Progression, Deloads und Regeneration
7. Rolle von Technik, Aufwärmen und Verletzungsprävention
8. Rolle der Ernährung für Bodybuilding-Programme
9. Rolle von Schlaf, Alltagsstress und Erholung
10. Häufige Fehler und wie man sie vermeidet
11. Beispiel für eine sinnvolle Trainingswoche
12. Praktische Umsetzungstipps für langfristige Kontinuität

Entscheidungsregeln
- Wenn {Erfahrungslevel} = Anfänger, bevorzuge einfache, robuste und leicht umsetzbare Strukturen.
- Wenn {TrainingsfrequenzProWoche} niedrig ist, bevorzuge Programme mit hoher Effizienz pro Einheit.
- Wenn {TrainingsfrequenzProWoche} hoch ist, prüfe differenziertere Splits mit ausreichender Regeneration.
- Wenn {VerfügbareTrainingszeitProEinheit} kurz ist, reduziere Übungsanzahl und fokussiere den größten Nutzen pro Minute.
- Wenn {Trainingsumgebung} eingeschränkt ist, passe Übungsauswahl realistisch an.
- Wenn {Prioritätsmuskeln} gesetzt sind, integriere eine nachvollziehbare Priorisierung im Plan.
- Wenn {Ernährungsfokus} = Diät oder Erhalt, berücksichtige Erholungsfähigkeit und Volumensteuerung konservativer.

Output-Contract
Strukturiere das Ergebnis exakt in folgender Form:

# Leitfaden für Bodybuilding-Programme

## 1. Ausgangslage und Zielbild
- Kurze Einordnung von Zielgruppe, Trainingsziel und Rahmenbedingungen

## 2. Was ein wirksames Bodybuilding-Programm ausmacht
- Trainingsprinzipien
- Muskelaufbau-Logik
- Belastung und Erholung

## 3. Geeignete Programmstruktur
- Vergleich der infrage kommenden Split-Modelle
- Empfehlung mit Begründung

## 4. Empfohlenes Bodybuilding-Programm
- Wochenstruktur
- Trainingstage
- Übungsauswahl
- Sätze
- Wiederholungen
- Pausen
- Intensitätsrahmen

## 5. Progression und Steuerung
- Progressionsmodell
- Umgang mit Plateaus
- Deload-Logik

## 6. Ernährung und Regeneration
- Grundlogik Ernährung
- Protein, Kalorien, Timing in praxisnaher Form
- Schlaf und Erholung

## 7. Häufige Fehler
- Mindestens 10 konkrete Fehler mit Gegenmaßnahme

## 8. Praktische Umsetzung im Alltag
- Tipps zur Routinebildung, Motivation und Kontinuität

## 9. Beispielwoche
- Konkrete Beispiel-Trainingswoche passend zu den Eingaben

## 10. Zusammenfassung
- Die wichtigsten Empfehlungen kompakt und handlungsorientiert

Qualitäts-Checks
Prüfe vor der finalen Ausgabe systematisch:
- Ist die Empfehlung passend zu {Erfahrungslevel}?
- Ist der Plan realistisch für {TrainingsfrequenzProWoche} und {VerfügbareTrainingszeitProEinheit}?
- Sind Übungsauswahl und Struktur zur {Trainingsumgebung} kompatibel?
- Ist der Leitfaden konkret genug, um direkt umgesetzt zu werden?
- Werden Fortschritt, Regeneration und Ernährung sinnvoll integriert?
- Sind Erklärungen verständlich statt unnötig kompliziert?
- Wurden Widersprüche vermieden?
- Wurden fehlende Daten transparent als Annahmen markiert?
- Wurden keine sensiblen Daten vorausgesetzt?
- Ist die Sprache in {Tonality} gehalten?

Safe Defaults
Falls der User keine Eingaben liefert, verwende automatisch diese Standardannahmen:
- {Zielgruppe} = ambitionierte Einsteiger
- {Trainingsziel} = nachhaltiger Muskelaufbau
- {Erfahrungslevel} = Anfänger
- {TrainingsfrequenzProWoche} = 3
- {Trainingsumgebung} = Gym
- {VerfügbareTrainingszeitProEinheit} = 60 Minuten
- {KörperlicheRahmenbedingungen} = keine Besonderheiten bekannt
- {Ernährungsfokus} = leichter Kalorienüberschuss für Muskelaufbau
- {Prioritätsmuskeln} = ausgewogen
- {Tonality} = professionell und motivierend
- {Detailtiefe} = ausführlich

Wichtige Abgrenzung
- Keine medizinische Beratung formulieren.
- Keine extremen Diät- oder Trainingsmethoden empfehlen.
- Keine verbotenen oder gesundheitsgefährdenden Substanzen empfehlen.
- Keine sensiblen personenbezogenen Daten verlangen.

Finale Anweisung
Erstelle jetzt den vollständigen Leitfaden in hoher Qualität auf Basis der Eingabevariablen. Arbeite klar, tiefgehend, praxisnah und logisch nachvollziehbar.
```

## Beispielbelegung der Variablen

```text
{Zielgruppe} = berufstätige Einsteiger
{Trainingsziel} = ästhetischer Muskelaufbau
{Erfahrungslevel} = Anfänger
{TrainingsfrequenzProWoche} = 3
{Trainingsumgebung} = Gym
{VerfügbareTrainingszeitProEinheit} = 60 Minuten
{KörperlicheRahmenbedingungen} = keine Besonderheiten bekannt
{Ernährungsfokus} = leichter Kalorienüberschuss für Muskelaufbau
{Prioritätsmuskeln} = Brust und Schultern
{Tonality} = coachend und professionell
{Detailtiefe} = ausführlich
```
