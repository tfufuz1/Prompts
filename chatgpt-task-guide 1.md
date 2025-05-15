# ChatGPT-Leitfaden: Aufgabenbearbeitung für das soziale Kennenlernnetzwerk

Dieser Leitfaden soll ChatGPT bei der systematischen Bearbeitung jeder Aufgabe des Projektplans unterstützen. Für jede Phase und Aufgabe werden die notwendigen Schritte und Überlegungen aufgeführt.

## Allgemeine Anweisungen für ChatGPT

1. Analysiere jede Aufgabe sorgfältig und identifiziere die Hauptziele.
2. Berücksichtige den Kontext des Gesamtprojekts bei jeder Aufgabe.
3. Gib detaillierte, schrittweise Anleitungen für jede Aufgabe.
4. Verweise auf relevante Technologien, Bibliotheken oder Best Practices.
5. Berücksichtige potenzielle Herausforderungen und biete Lösungsansätze.
6. Stelle sicher, dass deine Antworten spezifisch und umsetzbar sind.

## Phase 1: Konzeption und Planung

### 1.1 Anforderungsanalyse

1. Recherchiere die Hauptfunktionen von Tinder, Tellonym und Lovoo.
2. Erstelle eine Liste der Kernfunktionen jeder App.
3. Identifiziere Überschneidungen und einzigartige Features.
4. Priorisiere die Funktionen basierend auf ihrer Relevanz für das Projekt.
5. Definiere die Alleinstellungsmerkmale des neuen Netzwerks.

### 1.2 Funktionale Spezifikation

1. Erstelle eine detaillierte Liste aller Funktionen des Netzwerks.
2. Definiere Benutzerrollen (z.B. normaler Benutzer, Premium-Benutzer, Administrator).
3. Beschreibe die Rechte und Einschränkungen jeder Benutzerrolle.
4. Verfasse User Stories für jede Hauptfunktion (z.B. "Als Benutzer möchte ich...").
5. Erstelle Use Cases für komplexe Interaktionen (z.B. Matching-Prozess).

### 1.3 Technische Spezifikation

1. Wähle die Hauptkomponenten des technischen Stacks aus (z.B. React Native, Expo, TypeScript, Firebase).
2. Skizziere die Systemarchitektur (Frontend, Backend, Datenbank, externe Dienste).
3. Entwirf ein detailliertes Datenmodell für Benutzer, Tags, Fragen, Matches und Chats.
4. Definiere die API-Endpunkte für die Kommunikation zwischen Frontend und Backend.
5. Berücksichtige Skalierbarkeit und Leistungsaspekte in der Architektur.

### 1.4 UI/UX-Design-Konzept

1. Erstelle Wireframes für alle Hauptbildschirme (z.B. Login, Profil, Matching, Chat).
2. Definiere den visuellen Stil (Farbschema, Typografie, Ikonografie).
3. Entwerfe die Markenidentität (Logo, Slogan, visuelle Elemente).
4. Erstelle einen klickbaren Prototyp mit einem Tool wie Figma oder Adobe XD.
5. Definiere Animationen und Übergänge zwischen Bildschirmen.

## Phase 2: Setup und Grundlagen

### 2.1 Entwicklungsumgebung

1. Installiere Node.js und npm (neueste LTS-Version).
2. Installiere Expo CLI global (`npm install -g expo-cli`).
3. Installiere TypeScript (`npm install -g typescript`).
4. Richte ein Git-Repository ein und erstelle eine `.gitignore`-Datei.
5. Konfiguriere ESLint und Prettier für konsistenten Code-Stil.

### 2.2 Projekt-Initialisierung

1. Erstelle ein neues Expo-Projekt mit TypeScript-Template (`expo init ProjectName --template expo-template-blank-typescript`).
2. Installiere react-navigation und erforderliche Abhängigkeiten.
3. Erstelle die Basisordnerstruktur (components, screens, services, utils).
4. Initialisiere die App.tsx mit einem grundlegenden NavigationContainer.
5. Erstelle Platzhalter-Komponenten für Hauptbildschirme.

### 2.3 Backend-Setup

1. Erstelle ein neues Firebase-Projekt in der Firebase-Konsole.
2. Aktiviere Firestore, Authentication und Realtime Database.
3. Installiere Firebase SDK im Projekt (`npm install firebase`).
4. Konfiguriere Firebase in der App (erstelle eine firebase.ts-Konfigurationsdatei).
5. Implementiere grundlegende Authentifizierungsfunktionen (Registrierung, Login, Logout).

(Die Anleitung wird für jede Phase und Aufgabe des Projektplans fortgesetzt...)

## Abschlusshinweise für ChatGPT

- Passe die Detailtiefe deiner Antworten an die Komplexität der Aufgabe an.
- Biete bei Bedarf alternative Lösungsansätze oder Technologien an.
- Weise auf potenzielle Fallstricke oder häufige Fehler hin.
- Ermuntere zu Best Practices in Bezug auf Code-Qualität, Sicherheit und Benutzerfreundlichkeit.
- Empfehle bei komplexen Aufgaben, diese in kleinere, überschaubare Teilaufgaben zu unterteilen.
