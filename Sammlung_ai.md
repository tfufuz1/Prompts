## Einschränkungen
In einer Sammlung können **Sammlungs-Anweisungen** (~2300 Zeichen) Gespeichert werden.
Ein **Initial-Prompt** ist für die KI wichtiger wie sie Sammlungsanweisung im Fall eines Konfliktes wird der Initial-Prompt bevorzugt.

| Art            |                                                                                                                        |
| -------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Sammlung       | In einer Sammlung können Gespräche mit einer vordefinierten Sammlungs-Anweisung gestartet werden                       |
| Initial-Prompt | Gesprächseinstieg, diese Anweisung wird bevorzugt, bleibt aber nur eine gewisse Zeit im Kontext                        |
| + Prompts      | Die weiteren Prompts sollten direkte Aufgaben und Schritte beinhalten und immer mal wieder an die Richtlinien erinnern |
Das Unterteilen von Prompts in Textschnipsel kann sehr nützlich sein, insbesondere wenn Sie komplexe Aufgaben strukturieren oder verschiedene Domänen abdecken möchten. Hier sind einige Strategien, wie Sie dies effektiv tun können:

### 1. **Nach Funktion oder Aufgabe**

- **Einleitung**: Stellen Sie den Kontext und das Ziel der gesamten Aufgabe vor.
- **Spezifische Anweisung**: Geben Sie eine detaillierte Beschreibung der spezifischen Aufgabe oder Frage.
- **Erwartetes Ergebnis**: Beschreiben Sie, was eine gute Antwort ausmacht.
- **Beispiel**: Fügen Sie ein Beispiel hinzu, um das gewünschte Format oder den Stil zu verdeutlichen.

### 2. **Nach Domäne**

Wenn Ihr Projekt mehrere Fachbereiche abdeckt, können Sie die Prompts nach Domänen unterteilen:

- **Domäne A (z.B. Projektplanung)**:
  - **Kontext**: Hintergrundinformationen zur Domäne.
  - **Aufgabe**: Spezifische Fragen oder Aufgaben innerhalb dieser Domäne.
  - **Erwartungen**: Kriterien für eine gute Antwort in diesem Bereich.

- **Domäne B (z.B. Softwarearchitektur)**:
  - **Kontext**: Relevante Details zur Architektur.
  - **Aufgabe**: Anforderungen und Designfragen.
  - **Erwartungen**: Technische Details und Genauigkeit.

### 3. **Nach Struktur**

- **Einführungsschnipsel**: Allgemeiner Überblick und Zielsetzung.
- **Detailschnipsel**: Detaillierte Anweisungen und spezifische Fragen.
- **Formatierungsschnipsel**: Vorgaben für das Antwortformat.
- **Beispielschnipsel**: Beispiele für Klarheit und Orientierung.

### Beispiel

Hier ist ein Beispiel, wie Sie einen Prompt in Textschnipsel unterteilen könnten:

#### Einleitung
```
Ziel: Entwickle eine umfassende Projektstrategie für eine neue mobile App zur Aufgabenverwaltung.
```

#### Projektplanung
```
Kontext: Die App soll Aufgaben erstellen, bearbeiten und kategorisieren können.
Aufgabe: Erstelle einen Projektplan mit Meilensteinen und Zeitrahmen.
Erwartungen: Der Plan sollte in einer tabellarischen Form dargestellt werden.
```

#### Softwarearchitektur
```
Kontext: Nutze den Projektplan als Grundlage für die Architekturentwicklung.
Aufgabe: Entwirf eine modulare und skalierbare Architektur für die App.
Erwartungen: Beschreibe die Hauptkomponenten und deren Interaktionen in einem Diagramm.
```

Indem Sie Ihre Prompts so strukturieren, können Sie sicherstellen, dass jeder Abschnitt klar und fokussiert bleibt, was zu präziseren und relevanteren Antworten führt.


```
Rolle: Du bist ein erfahrener Projektmanager.
Ziel: Entwickle einen Projektplan, einen Projektstrukturplan und einen Technologie-Stack.

Aufgaben:
1. **Projektplan**: Teile in 5 Abschnitte auf.
2. **Projektstrukturplan**: Teile in 3 Abschnitte auf.
3. **Technologie-Stack**: Teile in 2 Abschnitte auf.

Antwortformat:
- Beginne jede Antwort mit "Teil X von Y".
- Führe die Details des Abschnitts aus.
- Empfehle den nächsten Schritt nach jeder Antwort.
```
Um bei jeder Antwort wichtige Aspekte oder Inhalte pro Aufgabe einzufügen, können Sie den Prompt so gestalten, dass er spezifische Anweisungen für die Details und Schwerpunkte jeder Aufgabe enthält. Hier ist eine detaillierte Struktur, die Sie verwenden können:

### Initialer Prompt

```plaintext
Rolle: Du bist ein erfahrener Projektmanager und Softwarearchitekt.
Ziel: Entwickle einen umfassenden Projektplan, einen Projektstrukturplan und einen Technologie-Stack für eine mobile App.

Aufgabenstruktur:
1. **Projektplan**: Teile den Projektplan in fünf Abschnitte auf und gib jeden Abschnitt in einer separaten Antwort aus.
   - Wichtige Aspekte: Ziele, Zeitrahmen, Meilensteine, Ressourcenbedarf, Risiken.
   
2. **Projektstrukturplan**: Teile den Projektstrukturplan in drei Abschnitte auf und präsentiere jeden Abschnitt einzeln.
   - Wichtige Aspekte: Hauptkomponenten, Verantwortlichkeiten, Abhängigkeiten.

3. **Technologie-Stack**: Teile die Beschreibung des Technologie-Stacks in zwei Abschnitte auf.
   - Wichtige Aspekte: Auswahlkriterien, Vor- und Nachteile der Technologien.

Antwortformat:
- Beginne jede Antwort mit "Teil X von Y" und einer kurzen Zusammenfassung des Inhalts.
- Führe die Details des Abschnitts aus und hebe die wichtigen Aspekte hervor.
- Nach jeder Antwort, empfehle den nächsten logischen Schritt oder Abschnitt.

Erste Aufgabe: Beginne mit dem Projektplan und teile ihn in fünf Antworten auf.
```

### Beispiel für die Aufteilung mit Inhalten

#### Projektplan (Teil 1 von 5)

```plaintext
Teil 1 von 5: Einführung und Projektziele
- Beschreibe das übergeordnete Ziel des Projekts.
- Wichtige Aspekte:
  - Klare Definition der Projektziele.
  - Identifikation der Zielgruppe.
  - Erwartete Ergebnisse und Nutzen der App.
```

#### Projektstrukturplan (Teil 1 von 3)

```plaintext
Teil 1 von 3: Übersichtsdiagramm der Hauptkomponenten
- Erstelle ein Diagramm der Hauptkomponenten des Projekts.
- Wichtige Aspekte:
  - Beschreibung der Funktionalität jeder Komponente.
  - Identifikation von Schlüsselverantwortlichen für jede Komponente.
```

#### Technologie-Stack (Teil 1 von 2)

```plaintext
Teil 1 von 2: Frontend-Technologien
- Liste die Technologien auf, die für das Frontend verwendet werden sollen.
- Wichtige Aspekte:
  - Auswahlkriterien für jede Technologie (z.B. Performance, Skalierbarkeit).
  - Vor- und Nachteile der gewählten Technologien im Kontext des Projekts.
```

Um einen initialen Prompt zu erstellen, der mehrere Aufgaben umfasst und jede Aufgabe in mehrere Antworten unterteilt, sollten Sie eine klare Struktur und spezifische Anweisungen verwenden. Hier ist ein Beispiel, wie Sie dies formulieren können:

### Initialer Prompt

```plaintext
Rolle: Du bist ein erfahrener Projektmanager und Softwarearchitekt.
Ziel: Entwickle einen umfassenden Projektplan, einen Projektstrukturplan und einen Technologie-Stack für eine mobile App.

Aufgabenstruktur:
1. **Projektplan**: Teile den Projektplan in fünf Abschnitte auf und gib jeden Abschnitt in einer separaten Antwort aus.
2. **Projektstrukturplan**: Teile den Projektstrukturplan in drei Abschnitte auf und präsentiere jeden Abschnitt einzeln.
3. **Technologie-Stack**: Teile die Beschreibung des Technologie-Stacks in zwei Abschnitte auf.

Antwortformat:
- Beginne jede Antwort mit "Teil X von Y" und einer kurzen Zusammenfassung des Inhalts.
- Führe die Details des Abschnitts aus.
- Nach jeder Antwort, empfehle den nächsten logischen Schritt oder Abschnitt.

Erste Aufgabe: Beginne mit dem Projektplan und teile ihn in fünf Antworten auf.
```

### Beispiel für die Aufteilung

#### Projektplan (Teil 1 von 5)

```plaintext
Teil 1 von 5: Einführung und Projektziele
- Beschreibe das Projektziel und die erwarteten Ergebnisse.
```

#### Projektstrukturplan (Teil 1 von 3)

```plaintext
Teil 1 von 3: Übersichtsdiagramm der Hauptkomponenten
- Erstelle ein Diagramm, das die Hauptkomponenten des Projekts zeigt.
```

#### Technologie-Stack (Teil 1 von 2)

```plaintext
Teil 1 von 2: Frontend-Technologien
- Liste die Technologien auf, die für das Frontend verwendet werden sollen, und begründe die Auswahl.
```



Um Chained Prompting effektiv in Textschnipsel zu unterteilen, können Sie die Aufgabe in mehrere Schritte aufteilen, wobei jeder Schritt in einem separaten Prompt behandelt wird. Hier ist ein Beispiel, wie Sie dies strukturieren können:

### 1. Initialer Prompt

Starten Sie mit einem umfassenden Prompt, der die Rolle und das Ziel des gesamten Projekts festlegt.

```plaintext
Rolle: Du bist ein Projektmanager für Softwareentwicklung.
Ziel: Entwickle einen detaillierten Projektplan für eine mobile App zur Aufgabenverwaltung.
Nach jeder Antwort: Empfehle den nächsten Schritt im Prozess.
```

### 2. Konzeptentwicklung

In diesem Schritt fokussieren Sie sich auf die Entwicklung des Konzepts.

```plaintext
Aufgabe: Erstelle ein Konzept für die mobile App.
Kontext: Die App soll Aufgaben erstellen, bearbeiten und kategorisieren können.
Erwartete Ausgabe: Eine Liste mit den Hauptfunktionen der App.
```

### 3. Architekturplanung

Dieser Schritt konzentriert sich auf die Entwicklung der Softwarearchitektur.

```plaintext
Aufgabe: Entwickle eine Softwarearchitektur basierend auf dem Konzept.
Kontext: Nutze das zuvor erstellte Konzept als Grundlage.
Erwartete Ausgabe: Ein Diagramm der Hauptkomponenten und ihrer Interaktionen.
```

### 4. Implementierung

Hier geht es um die Umsetzung des Codes für die Komponenten.

```plaintext
Aufgabe: Implementiere die Hauptkomponenten der App mit anwendbarem Code.
Kontext: Verwende die zuvor entwickelte Architektur als Leitfaden.
Erwartete Ausgabe: Funktionierender Code für jede Komponente.
```

### 5. Testen und Validieren

Der letzte Schritt umfasst das Testen und Validieren des Projekts.

```plaintext
Aufgabe: Teste die App und validiere ihre Funktionalität.
Kontext: Stelle sicher, dass alle Funktionen wie geplant arbeiten und keine Fehler auftreten.
Erwartete Ausgabe: Ein Bericht über Testergebnisse und empfohlene Verbesserungen.
```

Durch diese Struktur können Sie sicherstellen, dass ChatGPT in jedem Schritt genau weiß, was erwartet wird, und es ermöglicht Ihnen, den Prozess klar zu gliedern und konsistent voranzutreiben.


Gerne erstelle ich Ihnen ein Template, das Sie für Ihre komplexen Aufgaben mit ChatGPT verwenden können. Dieses Template ist so strukturiert, dass es ChatGPT hilft, alle Schritte korrekt auszuführen und die Aufgaben in mehrere Antworten zu unterteilen.

```plaintext
Rolle: Du bist ein [ROLLE, z.B. erfahrener Projektmanager und Softwarearchitekt].

Gesamtziel: [BESCHREIBUNG DES GESAMTZIELS, z.B. Entwickle einen umfassenden Plan für ein Softwareprojekt]

Aufgabenstruktur:
1. [AUFGABE 1, z.B. Projektplan]: Teile diese Aufgabe in [ANZAHL] Abschnitte auf.
   - Wichtige Aspekte: [LISTE DER WICHTIGEN PUNKTE]
   
2. [AUFGABE 2, z.B. Projektstrukturplan]: Teile diese Aufgabe in [ANZAHL] Abschnitte auf.
   - Wichtige Aspekte: [LISTE DER WICHTIGEN PUNKTE]

3. [AUFGABE 3, z.B. Technologie-Stack]: Teile diese Aufgabe in [ANZAHL] Abschnitte auf.
   - Wichtige Aspekte: [LISTE DER WICHTIGEN PUNKTE]

Antwortformat für jede Aufgabe:
- Beginne jede Antwort mit "Teil X von Y: [KURZE BESCHREIBUNG]"
- Führe die Details des Abschnitts aus und berücksichtige dabei die wichtigen Aspekte.
- Schließe jede Antwort mit einer Empfehlung für den nächsten logischen Schritt ab.

Zusätzliche Anweisungen:
- Halte dich strikt an die vorgegebene Struktur und Anzahl der Abschnitte.
- Stelle sicher, dass alle wichtigen Aspekte in den entsprechenden Abschnitten behandelt werden.
- Wenn du eine Aufgabe abgeschlossen hast, gib eine kurze Zusammenfassung und leite zur nächsten Aufgabe über.

Erste Aufgabe: Beginne mit [AUFGABE 1] und teile sie in die angegebene Anzahl von Antworten auf.
```

Um dieses Template zu verwenden:

1. Füllen Sie die in [GROSSBUCHSTABEN] gekennzeichneten Platzhalter mit den spezifischen Details Ihres Projekts aus.
2. Passen Sie die Anzahl der Aufgaben und Abschnitte nach Bedarf an.
3. Fügen Sie spezifische Anweisungen oder Anforderungen hinzu, die für Ihr Projekt relevant sind.

Dieses Template hilft, eine klare Struktur für komplexe Aufgaben zu schaffen und stellt sicher, dass ChatGPT systematisch und detailliert vorgeht. Es ermöglicht auch eine einfache Anpassung an verschiedene Projekttypen und -anforderungen.