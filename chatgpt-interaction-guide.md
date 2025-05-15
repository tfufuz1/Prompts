# Leitfaden für effiziente ChatGPT-Interaktionen

## 1. Grundlegende Strukturierungsprinzipien

### Rollenbasierte Interaktion
- Definiere eine spezifische Rolle für ChatGPT (z.B. "Agiere als erfahrener Software-Architekt")
- Nutze das Kommando "bleibe in dieser Rolle" für Folgeanfragen
- Beispiel: "Du bist ein erfahrener Python-Entwickler. Bleibe während unserer gesamten Konversation in dieser Rolle."

### Kontextuelle Rahmenbedingungen
- Setze klare Rahmenbedingungen zu Beginn der Konversation
- Referenziere diese in Folgeanfragen durch "unter Berücksichtigung der vorher festgelegten Bedingungen"
- Beispiel: "Folgende Regeln gelten für alle weiteren Antworten: Maximal 3 Absätze, immer mit Beispiel"

## 2. Fortlaufende Kontrolle und Steuerung

### Memorierungstechniken
- Nummeriere wichtige Informationen oder Regeln
- Verwende Schlüsselwörter als Anker ("Bezugnehmend auf Regel #2")
- Erstelle eine Zusammenfassung bisheriger Festlegungen am Ende jeder komplexen Interaktion

### Qualitätssicherung
- Implementiere Überprüfungsroutinen ("Prüfe vor jeder Antwort folgende Kriterien")
- Nutze Checklisten für konsistente Outputs
- Fordere explizite Bestätigung der Einhaltung ("Bestätige, dass alle genannten Kriterien erfüllt sind")

## 3. Strukturierte Ausgabeformate

### Template-Definitionen
- Definiere wiederverwendbare Ausgabeformate
- Beispiel:
  ```
  Format für alle Antworten:
  1. Kurzzusammenfassung
  2. Detailausführung
  3. Praktisches Beispiel
  4. Nächste Schritte
  ```

### Formatierungskonventionen
- Lege Markdown-Formatierung fest
- Bestimme einheitliche Überschriftenhierarchie
- Definiere Listen- und Tabellenformate

## 4. Interaktionsmuster für komplexe Gespräche

### Iterative Verfeinerung
- Beginne mit grober Struktur
- Verfeinere schrittweise durch gezielte Nachfragen
- Nutze Zwischenzusammenfassungen

### Verzweigte Dialoge
- Markiere Entscheidungspunkte klar
- Nutze eindeutige Referenzen auf vorherige Verzweigungen
- Halte Überblick durch Nummerierung oder Bezeichnung von Pfaden

## 5. Fehlerbehandlung und Korrekturmechanismen

### Korrekturanweisungen
- Definiere Standard-Korrekturphrasen
- Beispiel: "Korrigiere unter Beibehaltung aller bisherigen Regeln folgendes:"
- Implementiere Versions-Tags für Überarbeitungen

### Qualitätssicherungsschleifen
- Etabliere regelmäßige Überprüfungspunkte
- Nutze standardisierte Überprüfungsfragen
- Implementiere Feedback-Schleifen

## 6. Best Practices für Langzeit-Interaktionen

### Sessionmanagement
1. Starte jede neue Session mit Zusammenfassung der geltenden Regeln
2. Setze explizite Checkpoints für längere Gespräche
3. Nutze Versionierung für verschiedene Gesprächsstände

### Kontinuitätssicherung
- Verwende eindeutige Identifikatoren für wichtige Konzepte
- Etabliere klare Referenzierungsmechanismen
- Führe regelmäßige Konsistenzprüfungen durch

## Praktische Anwendung

### Initialisierungsbeispiel
```
Neue Konversation:
1. Rolle: Senior Software-Architekt
2. Kontext: Enterprise-Softwareentwicklung
3. Ausgabeformat: Immer mit Problemanalyse, Lösung, Beispielcode
4. Qualitätskriterien: Performance, Skalierbarkeit, Wartbarkeit
5. Bleibe in dieser Konfiguration für alle folgenden Antworten
```

### Kontrollbeispiel
```
Vor jeder Antwort:
- Prüfe Übereinstimmung mit definierter Rolle
- Validiere Ausgabeformat
- Bestätige Einhaltung der Qualitätskriterien
```
