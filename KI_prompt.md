
# Rolle
"Für diese gesamte Konversation: Agiere als erfahrener Projektmanager und behalte folgende Projektziele im Blick: [Ziele]"
"Nimm für diese Konversation drei Perspektiven ein: Optimist [OPT], Pessimist [PES], Realist [REA]"
"Behalte während der gesamten Konversation die Perspektive eines strategischen Beraters bei"
"Für diese Konversation: Agiere als interdisziplinäres Expertenteam bestehend aus [TECH], [BUSINESS], [DESIGN]. Markiere die jeweilige Perspektive."
## Interaktion
"Fasse am Ende jeder deiner Antworten die bisher gesammelten Hauptpunkte in 2-3 Sätzen zusammen"


"Lass uns diese Aufgabe in 5 Schritten bearbeiten. Kennzeichne jeden Schritt mit [S1] bis [S5] und warte nach jedem Schritt auf meine Bestätigung"


# Gedächtnis
"Führe für diese Konversation ein Inhaltsverzeichnis. Aktualisiere es bei jeder neuen Antwort"
"Markiere Wissenslücken mit: [❓] Offene Fragen [❗] Wichtige Unklarheiten [💡] Recherchebedarf"


## Jede Antwort
"Bei jeder Antwort: Stelle zuerst dein Verständnis meiner Frage in eigenen Worten dar"
"Erstelle eine laufende Liste mit dem Titel 'Bisherige Erkenntnisse' und aktualisiere diese bei jeder Antwort"
"Agiere als mein persönlicher Berater. Fasse jede Antwort mit einer konkreten Empfehlung ab"
"Führe am Ende jeder Antwort eine Fortschrittsleiste [0%|-------|100%] für jedes Teilziel"
"Führe ein kontinuierliches Fortschrittsmonitoring mit: 📊 Fortschrittsbalken [0%====>100%] 📈 Trend [↗️aufwärts, →stabil, ↘️abwärts] 🎯 Zielerreichung [0-10]"
## Kreativ
"Generiere für jedes Problem drei Lösungsansätze: [K] Konservativ [I] Innovativ [R] Radikal"
"Entwickle Ideen nach dem Walt-Disney-Prinzip: [T] Träumer [R] Realist [K] Kritiker"
Analysiere das Problem aus drei zeitlichen Perspektiven: [VERGANGENHEIT] Was haben wir gelernt? [GEGENWART] Wo stehen wir? [ZUKUNFT] Wohin entwickelt sich das?"


Eine praktische Anleitung zur effizienten Nutzung großer Sprachmodelle wie ChatGPT oder Llama 3 mit Markdown-formatierten Prompts:

## Grundlagen des Markdown-Formats für Prompts

Markdown bietet vielfältige Möglichkeiten, Prompts klar zu strukturieren und die Ausgabe von Sprachmodellen zu steuern:

- **Überschriften** (#, ##, ###) für Hierarchie und Gliederung
- *Kursiv* und **Fettdruck** für Betonung
- Listen (- oder 1., 2., 3.) für Aufzählungen
- `Codeblöcke` für Formatierung
- > Blockzitate für Hervorhebungen
- Horizontale Linien (---) als Trenner

## Vorteile von Markdown-formatierten Prompts

- Verbesserte Lesbarkeit und Struktur
- Präzisere Steuerung der Modellausgabe
- Einfachere Unterscheidung von Anweisungen und Inhalt
- Möglichkeit, komplexe Szenarien übersichtlich darzustellen

## Effektive Prompt-Strukturierung

### 1. Rollendefinition und Kontext

```markdown
# Rolle: Experte für erneuerbare Energien
## Kontext: Beratungsgespräch mit Hausbesitzer zur Solaranlage
```

### 2. Aufgabenbeschreibung und Ziele

```markdown
## Aufgabe:
- Erkläre Vor- und Nachteile von Solaranlagen
- Berechne potenzielle Einsparungen
- Empfehle geeignete Systeme

## Ziel: Fundierte Entscheidungsgrundlage für den Kunden schaffen
```

### 3. Ausgabeformat und -struktur

```markdown
## Ausgabeformat:
1. Kurze Einleitung (2-3 Sätze)
2. Vor- und Nachteile (Tabelle)
3. Kostenberechnung (Liste mit Formeln)
4. Produktempfehlungen (3-5 Optionen)
5. Fazit und nächste Schritte
```

### 4. Verhaltensvorgaben und Ton

```markdown
## Verhalten:
- Freundlich und geduldig
- Technische Begriffe erklären
- Auf Kundenfragen eingehen

## Ton: Professionell, aber verständlich für Laien
```

### 5. Interaktionsmechanismen

```markdown
## Interaktion:
- Stelle Verständnisfragen nach jedem Abschnitt
- Biete 3 Optionen zur Vertiefung an
- Bei Unklarheiten: Bitte um Präzisierung
```

## Beispiele für spezifische Prompt-Techniken

### Gesprächseinstieg mit Optionen

```markdown
# Gesprächseinstieg: Solarenergie-Beratung

Willkommen zur Solarenergie-Beratung! Womit möchten Sie beginnen?

1. Überblick über Solaranlagen
2. Kostenanalyse für Ihr Haus
3. Aktuelle Fördermöglichkeiten

Bitte wählen Sie eine Option (1-3):
```

### Automatische Gesprächsführung

```markdown
## Gesprächsablauf:
1. Begrüßung und Einführung
2. Bedarfsanalyse (3-5 Fragen stellen)
3. Informationsphase (basierend auf Antworten)
4. Empfehlungen präsentieren
5. Fragen beantworten
6. Nächste Schritte vereinbaren

-> Beginne mit Schritt 1 und fahre automatisch fort
```

### Aktivierung spezifischer Verhaltensweisen

```markdown
## Verhaltensaktivierung:
- Bei technischen Fragen: [TECH_MODUS]
- Bei Kostenfragen: [FINANZ_MODUS]
- Bei Unsicherheiten: [EMPATHIE_MODUS]

Beispiel: Kunde fragt nach Amortisationszeit
[FINANZ_MODUS] Erklärung der Amortisationsberechnung...
```

### Portionierte Ausgaben

```markdown
## Ausgabestruktur:
1. Einleitung (max. 50 Wörter)
2. Hauptteil (3 Abschnitte, je 100-150 Wörter)
3. Fazit (max. 75 Wörter)

-> Generiere jeden Abschnitt einzeln und warte auf Bestätigung
```

## Fortgeschrittene Techniken

### Persona-Definition für konsistentes Verhalten

```markdown
# Persona: Dr. Solar

## Eigenschaften:
- 15 Jahre Erfahrung in Solarenergie
- Pragmatisch und lösungsorientiert
- Leicht humorvoller Kommunikationsstil

## Verhaltensmuster:
- Verwendet Analogien zur Erklärung
- Fragt nach praktischen Anwendungsszenarien
- Gibt proaktiv Energiespartipps
```

### Dynamische Gesprächsanpassung

```markdown
## Adaptives Verhalten:
- Bei hohem Interesse: Vertiefe technische Details
- Bei Zögern: Fokussiere auf praktische Vorteile
- Bei Kostenfokus: Betone langfristige Einsparungen

-> Passe Gesprächsstil basierend auf Kundenreaktionen an
```

### Selbstständige Problemlösung

```markdown
## Problemlösungsprotokoll:
1. Problem identifizieren
2. Mögliche Ursachen auflisten (min. 3)
3. Lösungsansätze pro Ursache entwickeln
4. Vor- und Nachteile jeder Lösung abwägen
5. Beste Lösung auswählen und begründen
6. Umsetzungsplan in 3-5 Schritten erstellen

-> Wende dieses Protokoll auf alle auftretenden Probleme an
```

Diese Beispiele demonstrieren die Vielseitigkeit und Effizienz von Markdown-formatierten Prompts für große Sprachmodelle. Durch klare Strukturierung und präzise Anweisungen können Nutzer die Ausgabe und das Verhalten der Modelle gezielt steuern und optimieren.

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/17380598/cda40374-f24c-4abb-bd84-85d499a02c19/Systematische_Prompts.txt