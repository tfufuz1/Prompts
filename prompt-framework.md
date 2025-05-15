# Framework für strukturierte ChatGPT-Anweisungen

## 1. Basis-Struktur

### 1.1 Kontext-Block
```
KONTEXT:
- Rolle: [Gewünschte Expertise/Perspektive]
- Zielgruppe: [Für wen ist das Ergebnis bestimmt]
- Vorwissen: [Relevante Vorkenntnisse/Annahmen]
- Rahmenbedingungen: [Zeitliche/technische/rechtliche Einschränkungen]
```

### 1.2 Aufgaben-Block
```
AUFGABE:
- Hauptziel: [Primäres Ziel der Interaktion]
- Teilaufgaben: [Durchzuführende Schritte]
- Gewünschtes Format: [Struktur/Layout der Antwort]
- Ausschlusskriterien: [Was soll vermieden werden]
```

### 1.3 Qualitäts-Block
```
QUALITÄTSKRITERIEN:
- Erfolgskriterien: [Woran wird Erfolg gemessen]
- Mindestanforderungen: [Must-have Elemente]
- Optimierungsziele: [Nice-to-have Elemente]
- Prüfpunkte: [Worauf soll besonders geachtet werden]
```

## 2. Erweiterungen für mehrstufige Interaktionen

### 2.1 Iterations-Marker
```
ITERATION:
- Phase: [Aktuelle Phase im Gesamtprozess]
- Status: [Fortschritt/offene Punkte]
- Änderungen: [Anpassungen zur vorherigen Version]
- Nächste Schritte: [Geplante Folgeschritte]
```

### 2.2 Feedback-Schleife
```
FEEDBACK:
- Bewertung letzte Version: [Was war gut/schlecht]
- Konkrete Änderungswünsche: [Was soll angepasst werden]
- Offene Fragen: [Was muss geklärt werden]
- Neue Anforderungen: [Was kam hinzu]
```

## 3. Implementierungsrichtlinien

### 3.1 Grundprinzipien
- Explizite über implizite Anweisungen
- Atomare, eindeutige Anforderungen
- Konsistente Begrifflichkeiten
- Messbare Qualitätskriterien
- Nachvollziehbare Struktur

### 3.2 Best Practices
- Nummerierung für Referenzierbarkeit
- Priorisierung der Anforderungen
- Beispiele für gewünschtes Format
- Grenzen und Einschränkungen definieren
- Iterationsschritte dokumentieren

### 3.3 Anpassungsmöglichkeiten
- Skalierung der Detailtiefe
- Modulare Erweiterbarkeit
- Branchen-spezifische Anpassungen
- Format-Variationen

## 4. Beispielanwendung

### 4.1 Initial-Prompt
```
KONTEXT:
- Rolle: Senior Software Architekt
- Zielgruppe: Entwicklungsteam
- Vorwissen: Grundlegendes Verständnis von Microservices
- Rahmenbedingungen: Cloud-native Umgebung

AUFGABE:
- Hauptziel: Microservice-Architektur für E-Commerce System
- Teilaufgaben:
  1. Komponenten identifizieren
  2. Schnittstellen definieren
  3. Datenmodell erstellen
- Format: Architektur-Dokumentation mit Diagrammen
- Ausschluss: Legacy-Systeme

QUALITÄTSKRITERIEN:
- Erfolgskriterien: Skalierbarkeit, Wartbarkeit
- Mindestanforderungen: REST-APIs, Event-Driven
- Optimierungsziele: Cloud-native Patterns
- Prüfpunkte: Security, Performance
```

### 4.2 Iterations-Prompt
```
ITERATION:
- Phase: Design-Review
- Status: Komponenten definiert, Schnittstellen offen
- Änderungen: Neue Security-Anforderungen
- Nächste Schritte: API-Design finalisieren

FEEDBACK:
- Bewertung: Komponenten gut strukturiert
- Änderungswünsche: Mehr Details zu Security
- Offene Fragen: Authentifizierung
- Neue Anforderungen: GDPR-Compliance
```

## 5. Erfolgskontrolle

### 5.1 Qualitätsindikatoren
- Vollständigkeit der Anforderungen
- Eindeutigkeit der Anweisungen
- Konsistenz über Iterationen
- Nachvollziehbarkeit der Änderungen
- Erreichung der Qualitätsziele

### 5.2 Anpassungsbedarf erkennen
- Regelmäßige Evaluation
- Feedback-Analyse
- Iteration-Metriken
- Verbesserungsvorschläge

### 5.3 Dokumentation
- Versionierung der Prompts
- Änderungshistorie
- Lessons Learned
- Best Practices Sammlung
