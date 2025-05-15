# NeoAwesome Wayland Compositor - Entwicklerdokumentation

## Übersicht der Implementierung

Diese Dokumentation dient als Leitfaden für Entwickler, die am NeoAwesome Wayland Compositor arbeiten oder ihn erweitern möchten. Sie beschreibt die Architektur, die wichtigsten Komponenten und deren Zusammenspiel.

## Projektstruktur

```
neoawesome/
├── include/                 # Header-Dateien
│   ├── core/                # Kern-Komponenten
│   ├── rendering/           # Rendering-Komponenten
│   ├── input/               # Input-Handling
│   ├── window/              # Fenstermanagement
│   ├── widget/              # UI-Widgets
│   └── config/              # Konfiguration und Theming
├── src/                     # Implementierungsdateien
│   ├── core/                # Kern-Komponenten
│   ├── rendering/           # Rendering-Komponenten
│   ├── input/               # Input-Handling
│   ├── window/              # Fenstermanagement
│   ├── widget/              # UI-Widgets
│   └── config/              # Konfiguration und Theming
├── assets/                  # Ressourcen (Icons, Themes)
├── config/                  # Standard-Konfigurationsdateien
├── docs/                    # Dokumentation
└── build/                   # Build-Verzeichnis
```

## Implementierte Komponenten

### 1. Core-Komponenten

#### WaylandServer (wayland_server.hpp/cpp)
- Initialisiert den Wayland-Server
- Erstellt den Wayland-Socket
- Verwaltet Wayland-Clients und -Ressourcen
- Implementiert grundlegende Wayland-Protokolle

#### EventLoop (event_loop.hpp/cpp)
- Implementiert die Hauptereignisschleife
- Verarbeitet Ereignisse von Wayland, Input und Timer
- Bietet Callback-Mechanismen für Ereignisbehandlung

#### BackendManager (backend_manager.hpp/cpp)
- Integriert mit wlroots für Hardware-Zugriff
- Verwaltet Ausgabegeräte (Monitore)
- Initialisiert Rendering-Backends (OpenGL/EGL)

### 2. Rendering-Komponenten

#### Renderer (renderer.hpp/cpp)
- Implementiert OpenGL/EGL-Rendering
- Verwaltet Shader und Rendering-Ressourcen
- Bietet Schnittstellen für 2D-Rendering

#### SceneGraph (scene_graph.hpp/cpp)
- Implementiert eine hierarchische Szenenstruktur
- Verwaltet Transformationen und Sichtbarkeit
- Optimiert Rendering durch Culling und Batching

#### SurfaceManager (surface_manager.hpp/cpp)
- Verwaltet Wayland-Surfaces
- Implementiert Damage-Tracking für effizientes Rendering
- Koordiniert Surface-Komposition

### 3. Input-Komponenten

#### InputManager (input_manager.hpp/cpp)
- Integriert libinput für Eingabegeräte
- Verwaltet Eingabegeräte (Tastatur, Maus, Touch)
- Leitet Eingabeereignisse an entsprechende Handler weiter

#### KeyboardManager (keyboard_manager.hpp/cpp)
- Verarbeitet Tastatureingaben
- Implementiert Keybindings und Modifikatoren
- Verwaltet Tastatur-Layouts und XKB-Zustand

#### PointerManager (pointer_manager.hpp/cpp)
- Verarbeitet Mauseingaben
- Implementiert Cursor-Verwaltung und -Rendering
- Verwaltet Maus-Fokus und Hover-Effekte

### 4. Fenstermanagement-Komponenten

#### WindowManager (window_manager.hpp/cpp)
- Zentrale Komponente für Fensterverwaltung
- Erstellt, zerstört und verwaltet Fenster
- Implementiert Fenster-Fokus und -Navigation
- Integriert mit LayoutManager und TagManager

#### LayoutManager (layout_manager.hpp/cpp)
- Implementiert verschiedene Fensterlayouts
- Unterstützt Tiling- und Floating-Layouts
- Berechnet Fensterpositionen und -größen

#### TagManager (tag_manager.hpp/cpp)
- Implementiert Tag-System für Workspaces
- Verwaltet Zuordnung von Fenstern zu Tags
- Implementiert Tag-Sichtbarkeit und -Auswahl

### 5. Widget-Komponenten

#### WidgetBase (widget_base.hpp/cpp)
- Basisklasse für alle UI-Widgets
- Implementiert gemeinsame Widget-Funktionalität
- Verwaltet Widget-Hierarchie und -Events

#### Panel (panel.hpp/cpp)
- Implementiert Panel/Leiste am Bildschirmrand
- Verwaltet Panel-Position und -Größe
- Container für andere Widgets (Taskbar, Systray)

#### Taskbar (taskbar.hpp/cpp)
- Zeigt laufende Anwendungen an
- Implementiert Fenster-Interaktion (Fokus, Minimieren)
- Unterstützt verschiedene Anzeigemodi (alle Fenster, aktueller Tag)

#### SystemTray (system_tray.hpp/cpp)
- Implementiert System-Tray für Statusanzeigen
- Verwaltet System-Tray-Icons
- Unterstützt XDG-Systray-Protokoll

#### Dashboard (dashboard.hpp/cpp)
- Implementiert Dashboard/Übersichtsseite
- Verwaltet Dashboard-Widgets
- Unterstützt verschiedene Layouts (Grid, Flow)

### 6. Konfigurations-Komponenten

#### ConfigManager (config_manager.hpp/cpp)
- Verwaltet Konfigurationseinstellungen
- Lädt und speichert Konfigurationsdateien (JSON)
- Implementiert Konfigurationsänderungs-Callbacks
- Unterstützt Hot-Reload für Konfigurationen

#### ThemeEngine (theme_engine.hpp/cpp)
- Verwaltet Themes mit Farben, Schriftarten und Eigenschaften
- Lädt und speichert Themes (JSON)
- Implementiert Theme-Änderungs-Callbacks
- Bietet Standard-Themes (Dracula)

#### StyleManager (style_manager.hpp/cpp)
- Wendet Themes auf Widgets an
- Implementiert CSS-ähnliche Stildefinitionen
- Unterstützt Stil-Vererbung
- Aktualisiert Stile bei Theme-Änderungen

## Schlüssel-Algorithmen und Datenstrukturen

### Tiling-Algorithmus
Der Tiling-Algorithmus in `LayoutManager` implementiert ein Master-Stack-Layout:
- Der erste Bereich (Master) erhält einen konfigurierbaren Anteil des Bildschirms
- Die restlichen Fenster (Stack) teilen sich den verbleibenden Platz
- Die Größenverhältnisse können durch den Benutzer angepasst werden

### Tag-System
Das Tag-System in `TagManager` verwendet:
- Eine Map für die Zuordnung von Fenstern zu Tags
- Eine Map für die Zuordnung von Tags zu Fenstern
- Fenster können mehreren Tags zugeordnet sein
- Tags können sichtbar oder unsichtbar sein

### Event-System
Das Event-System verwendet:
- Callback-basierte Ereignisbehandlung
- Ereignisweitergabe durch die Widget-Hierarchie
- Fokus-Management für Eingabeereignisse

## Erweiterungspunkte

### Neue Layouts hinzufügen
Um ein neues Layout hinzuzufügen:
1. Von der `Layout`-Basisklasse ableiten
2. Die `apply`-Methode implementieren
3. Das neue Layout beim `LayoutManager` registrieren

### Neue Widgets hinzufügen
Um ein neues Widget hinzuzufügen:
1. Von der `Widget`-Basisklasse ableiten
2. Die `render`- und `handleEvent`-Methoden implementieren
3. Das Widget in die Widget-Hierarchie einfügen

### Neue Themes hinzufügen
Um ein neues Theme hinzuzufügen:
1. Eine neue Theme-JSON-Datei erstellen
2. Das Theme mit der `ThemeEngine` laden
3. Das Theme über den `ConfigManager` aktivieren

## Bekannte Einschränkungen und zukünftige Erweiterungen

### Einschränkungen
- Aktuell werden nur grundlegende Wayland-Protokolle unterstützt
- Keine Unterstützung für Wayland-Erweiterungen wie xdg-decoration
- Begrenzte Unterstützung für HiDPI-Displays

### Geplante Erweiterungen
- Unterstützung für weitere Wayland-Protokolle
- Verbesserte HiDPI-Unterstützung
- Erweiterte Animations- und Übergangseffekte
- Lua-Scripting für Konfiguration und Erweiterungen

## Build-System und Abhängigkeiten

### CMake-Build-System
Das Projekt verwendet CMake als Build-System:
- Unterstützung für verschiedene Compiler und Plattformen
- Automatische Erkennung von Abhängigkeiten
- Konfigurierbare Build-Optionen

### Hauptabhängigkeiten
- wlroots: Wayland-Compositor-Bibliothek
- libinput: Eingabegeräte-Verwaltung
- EGL/OpenGL: Rendering
- xkbcommon: Tastatur-Handling
- json: Konfigurationsverwaltung

## Testframework

### Komponententests
- Unit-Tests für einzelne Komponenten
- Mocking-Framework für Abhängigkeiten
- Automatisierte Tests für kritische Funktionen

### Integrationstests
- Tests für das Zusammenspiel von Komponenten
- Simulierte Wayland-Clients für End-to-End-Tests
- Performance- und Stabilitätstests

## Debugging und Logging

### Logging-System
- Verschiedene Log-Level (DEBUG, INFO, WARNING, ERROR)
- Konfigurierbare Log-Ausgabe (Konsole, Datei)
- Kontextbezogene Log-Nachrichten

### Debugging-Tools
- Integrierte Debugging-Widgets
- Performance-Profiling
- Visuelle Debugging-Hilfen (Rahmen, Overlays)
