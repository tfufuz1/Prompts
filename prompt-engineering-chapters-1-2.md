# 1. Strukturelemente professioneller Prompts

## 1.1 Kernkomponenten eines High-Performance-Prompts

### Basisstruktur
```markdown
## SYSTEM-KONTEXT
- Definiert grundlegende Parameter
- Setzt Rahmenbedingungen
- Etabliert Constraints

## ROLLEN-DEFINITION
- Expertise und Fähigkeiten
- Verantwortungsbereiche
- Verhaltensmuster

## AUFGABEN-SPEZIFIKATION
- Hauptziele
- Teilaufgaben
- Erwartete Ergebnisse

## OUTPUT-FORMATIERUNG
- Strukturvorgaben
- Formatierungsregeln
- Präsentationsmuster

## QUALITÄTSKRITERIEN
- Erfolgsmetriken
- Prüfmechanismen
- Feedback-Loops
```

### Praktische Implementierung
```markdown
# 🤖 [Rollenbezeichnung] - v[Version]
## ROLLENDEFINITION:
- Hauptaufgabe: [Präzise Hauptfunktion]
- Kernkompetenzen: [Liste der Fähigkeiten]
- Arbeitsweise: [Methodische Ansätze]

## KERNFUNKTIONEN:
1. [Funktion 1]
   - [Unterpunkt]
   - [Unterpunkt]
2. [Funktion 2]
   - [Unterpunkt]
   - [Unterpunkt]

## PROZESSSTEUERUNG:
1. [Prozessschritt 1]
2. [Prozessschritt 2]
3. [Prozessschritt 3]

## AUSGABEFORMAT:
[Strukturierte Vorgaben für Output]
```

## 1.2 Modularer Aufbau von Instruktionssets

### Basis-Module
1. **Kontext-Modul**
   ```markdown
   KONTEXT:
   - Anwendungsbereich: [Spezifikation]
   - Zielgruppe: [Definition]
   - Rahmenbedingungen: [Parameter]
   ```

2. **Kompetenz-Modul**
   ```markdown
   KOMPETENZEN:
   - Primär: [Hauptfähigkeiten]
   - Sekundär: [Unterstützende Fähigkeiten]
   - Grenzen: [Limitierungen]
   ```

3. **Prozess-Modul**
   ```markdown
   PROZESS:
   1. Input-Verarbeitung
   2. Analyse-Phase
   3. Synthese-Phase
   4. Output-Generierung
   ```

4. **Output-Modul**
   ```markdown
   OUTPUT:
   Format: [Strukturvorgabe]
   Elemente:
   - [Element 1]
   - [Element 2]
   Validierung:
   - [Prüfkriterium 1]
   - [Prüfkriterium 2]
   ```

# 2. Methodiken der Prompt-Konstruktion

## 2.1 Chain-of-Thought Methode

### Grundstruktur
```markdown
DENKPROZESS:
1. Initial-Analyse
   - Gegebene Informationen
   - Fehlende Informationen
   - Annahmen

2. Zwischenschritte
   - Schritt A → Ergebnis
   - Schritt B → Ergebnis
   - Schritt C → Ergebnis

3. Synthese
   - Kombination der Ergebnisse
   - Validierung
   - Schlussfolgerung
```

### Praktisches Beispiel
```markdown
AUFGABE: Textanalyse durchführen

DENKPROZESS:
1. Textstruktur erfassen
   - Länge: 500 Wörter
   - Format: Argumentativ
   - Stil: Akademisch

2. Analyse-Ebenen
   - Sprachliche Mittel → Identifiziert
   - Argumentation → Geprüft
   - Kohärenz → Bewertet

3. Gesamtbewertung
   - Stärken zusammengefasst
   - Schwächen identifiziert
   - Verbesserungsvorschläge formuliert
```

## 2.2 Zero-Shot vs. Few-Shot Prompting

### Zero-Shot Template
```markdown
AUFGABE: [Präzise Beschreibung]
KONTEXT: [Notwendige Informationen]
ERWARTUNG: [Gewünschtes Ergebnis]
FORMAT: [Ausgabestruktur]
```

### Few-Shot Template
```markdown
AUFGABE: [Beschreibung]
BEISPIELE:
1. Input: [Beispiel 1]
   Output: [Erwartetes Ergebnis 1]
2. Input: [Beispiel 2]
   Output: [Erwartetes Ergebnis 2]

AKTUELLE AUFGABE:
Input: [Aktueller Fall]
Output: [Zu generieren]
```

## 2.3 Role Prompting und Persona-Design

### Persona-Template
```markdown
# PERSONA-DEFINITION
## KERNATTRIBUTE:
- Expertise: [Fachgebiet]
- Erfahrung: [Jahre/Niveau]
- Perspektive: [Sichtweise]

## KOMMUNIKATIONSSTIL:
- Tonalität: [Formell/Informell]
- Komplexität: [Einfach/Komplex]
- Interaktionsmuster: [Direktiv/Kollaborativ]

## VERHALTENSMUSTER:
- Primärverhalten: [Hauptmuster]
- Sekundärverhalten: [Nebenmuster]
- Grenzen: [Limitierungen]
```

## 2.4 Task Decomposition

### Dekompositions-Framework
```markdown
HAUPTAUFGABE: [Beschreibung]

TEILAUFGABEN:
1. [Teilaufgabe 1]
   - Eingaben: [...]
   - Prozess: [...]
   - Ausgaben: [...]

2. [Teilaufgabe 2]
   - Eingaben: [...]
   - Prozess: [...]
   - Ausgaben: [...]

INTEGRATION:
- Sequenz: [Reihenfolge]
- Abhängigkeiten: [Beziehungen]
- Validierung: [Prüfungen]
```
