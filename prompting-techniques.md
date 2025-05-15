
| Technik                       | Beschreibung                                                          | Prompt-Formulierung                                                                                                                                  | Konkretes Beispiel                                                                                                                                                                          |
| ----------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Flippet-Interaction           | Strukturierte Gesprächsoptionen mit nummerierten Auswahlmöglichkeiten | "Präsentiere nach jeder Antwort drei nummerierte Optionen zur Gesprächsfortführung und frage nach meiner Wahl."                                      | "Hier sind deine Optionen für Machine Learning:\n1. Supervised Learning vertiefen\n2. Praktische Übung starten\n3. Anwendungsfälle erkunden\nWelche Option wählst du?"                      |
| Branching Dialog              | Verzweigte Gesprächsführung mit unterschiedlichen Pfaden              | "Erstelle einen Dialog, bei dem jede meiner Entscheidungen zu einem anderen Gesprächszweig führt. Biete mindestens 2-3 Optionen pro Schritt."        | "Du willst eine App entwickeln. Wählst du:\nA) Native App entwickeln\nB) Cross-Platform Framework nutzen\nC) Progressive Web App erstellen\nJede Wahl führt zu spezifischen Folgeoptionen." |
| Goal-Oriented Prompting       | Zielgerichtete Führung mit Meilensteinen                              | "Definiere mein Ziel [X] und führe mich mit konkreten Zwischenzielen und Checkpoints dorthin. Frage nach jedem Milestone nach Feedback."             | "Ziel: REST API entwickeln\nMeilenstein 1: Endpoints definieren\nMeilenstein 2: Datenmodell erstellen\nWo stehst du? Was brauchst du für den nächsten Schritt?"                             |
| Explorative Interaktion       | Offene Erkundung mit gelenkter Führung                                | "Lass uns [Thema] erkunden. Stelle mir offene Fragen und biete verschiedene Richtungen zur Vertiefung an. Reagiere auf meine Interessen."            | "Du interessierst dich für Cybersecurity. Was fasziniert dich mehr:\n- Technische Aspekte?\n- Menschliche Faktoren?\n- Rechtliche Rahmenbedingungen?"                                       |
| Iterative Vertiefung          | Schrittweise Vertiefung mit Feedback-Schleifen                        | "Beginne mit einer Übersicht zu [Thema]. Vertiefen wir nach jedem Abschnitt die Aspekte, die mich interessieren. Prüfe regelmäßig mein Verständnis." | "Grundlagen der Algorithmen verstanden?\n1. Tiefer in Komplexitätsanalyse\n2. Praktische Implementierung\n3. Optimierungstechniken\nWas interessiert dich?"                                 |
| Szenario-basierte Interaktion | Realistische Szenarien mit Entscheidungspunkten                       | "Erstelle ein realistisches Szenario zu [Thema]. Lass mich Entscheidungen treffen und zeige die Konsequenzen. Biete alternative Pfade."              | "Szenario: Deine Webapp wurde gehackt.\nOptionen:\n1. Sofort offline nehmen\n2. Schwachstelle lokalisieren\n3. Backup wiederherstellen\nWas tust du?"                                       |
| Fragengeleitete Interaktion   | Systematische Fragesequenzen                                          | "Führe mich durch [Thema] mit einer Reihe aufeinander aufbauender Fragen. Passe die Komplexität an meine Antworten an."                              | "Lass uns dein Datenbankdesign optimieren:\n1. Wie sieht dein Datenmodell aus?\n2. Welche Beziehungen existieren?\n3. Wie oft werden Daten abgerufen?"                                      |
| Konversationspfade            | Strukturierte Gesprächsverläufe mit Verzweigungen                     | "Erstelle verschiedene Gesprächspfade zu [Thema]. Lass mich zwischen verschiedenen Vertiefungsrichtungen wählen."                                    | "Wähle deinen Lernpfad für JavaScript:\nPfad A: Frontend-Entwicklung\nPfad B: Node.js Backend\nPfad C: Full-Stack Development"                                                              |
| Looping Fragen                | Zyklische Vertiefungsfragen                                           | "Stelle nach jeder Antwort eine vertiefende Frage, die auf meiner Antwort aufbaut. Biete auch Möglichkeiten zur Richtungsänderung."                  | "Du erwähnst Microservices. Möchtest du mehr über:\n- Service Discovery?\n- Load Balancing?\n- API Gateway?\nOder eine andere Richtung einschlagen?"                                        |
| Explorative Optionen          | Offene Erkundungsmöglichkeiten mit Struktur                           | "Präsentiere bei jedem Schritt neue Erkundungsoptionen, die auf meinen bisherigen Interessen basieren. Behalte den roten Faden bei."                 | "Da du dich für KI-Ethik interessierst:\n1. Bias in Algorithmen\n2. Transparenz von KI-Entscheidungen\n3. Gesellschaftliche Auswirkungen\nWelchen Aspekt erkunden wir?"                     |
| Entscheidungsbaumstrategie    | Strukturierte Entscheidungsfindung                                    | "Entwickle einen Entscheidungsbaum für [Problem]. Führe mich Schritt für Schritt durch die Optionen und zeige Konsequenzen."                         | "Entscheidungsbaum: Cloud-Provider wählen\n↳ Hauptfokus: Kosten, Skalierbarkeit, Services?\n  ↳ Spezifische Anforderungen je nach Wahl"                                                     |
| Interaktive Challenges        | Praktische Übungen mit Feedback                                       | "Erstelle eine Reihe von Übungen zu [Thema], die progressiv schwieriger werden. Gib sofortiges Feedback und Hilfestellung."                          | "Challenge 1: Schreibe eine einfache API-Route\nFeedback nach Implementierung\nNächste Challenge basierend auf Performance"                                                                 |
| Rückkopplungsschleifen        | Kontinuierliches Feedback mit Anpassung                               | "Gib mir nach jeder Interaktion Feedback und passe die nächsten Schritte entsprechend an. Frage regelmäßig nach meinen Bedürfnissen."                | "Dein Code-Review zeigt gute Strukturierung.\nMöchtest du:\n1. Performance optimieren\n2. Sicherheit verbessern\n3. Tests hinzufügen?"                                                      |
| Adaptive Lernpfade            | Personalisierte Lernwege                                              | "Erstelle einen adaptiven Lernpfad, der sich an meine Vorkenntnisse und Lerngeschwindigkeit anpasst. Biete regelmäßige Assessments."                 | "Basierend auf deinem Fortschritt in Python:\n1. Fortgeschrittene Konzepte\n2. Praktische Projekte\n3. Spezialgebiete\nWas passt zu dir?"                                                   |

### Beispiele für kombinierte Techniken:

1. **Explorative Szenario-Challenges:**
```
"Lass uns durch ein realitätsnahes Projekt gehen. Du bist Tech Lead eines Startups.
Situation 1: Massive Performanceprobleme in der Produktion
A) Team zusammenrufen für Analyse
B) Monitoring-Daten auswerten
C) Notfall-Rollback durchführen
Wähle eine Option und ich zeige dir die Konsequenzen und nächsten Herausforderungen."
```

2. **Goal-Oriented Branching Tutorial:**
```
"Dein Ziel: Entwicklung einer sicheren Web-Applikation
Schritt 1: Architekturentscheidung
- Option A: Monolithische Architektur
- Option B: Microservices
- Option C: Serverless
Jede Wahl führt zu spezifischen Sicherheitsanforderungen und nächsten Schritten.
Wo möchtest du beginnen?"
```

3. **Iterative Challenge-Loops:**
```
"Lass uns deine Coding-Skills verbessern:
1. Erste Challenge: Implementiere eine einfache Funktion
2. Feedback und Optimierungsvorschläge
3. Nächste Challenge basierend auf deiner Lösung
4. Wiederhole mit steigender Komplexität
Bereit für die erste Challenge?"
```
