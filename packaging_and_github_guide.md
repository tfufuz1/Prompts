# Anleitung zur Erstellung einer .deb-Datei und GitHub-Upload

Diese Anleitung beschreibt, wie Sie aus dem NeoAwesome Wayland Compositor Quellcode eine Debian-Paketdatei (.deb) erstellen und den Quellcode auf GitHub hochladen können.

## Teil 1: Erstellung einer .deb-Datei

### Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass folgende Pakete auf Ihrem System installiert sind:

```bash
sudo apt update
sudo apt install build-essential debhelper cmake devscripts lintian
sudo apt install libwayland-dev libwlroots-dev libinput-dev libegl-dev libgles2-mesa-dev libxkbcommon-dev libpixman-1-dev libcairo2-dev libpango1.0-dev libglib2.0-dev libjson-c-dev
```

### Schritt 1: Vorbereitung der Paketstruktur

Der NeoAwesome Compositor enthält bereits ein Skript zur Erstellung der Debian-Paketstruktur. Führen Sie folgendes aus:

```bash
cd /pfad/zu/neoawesome
chmod +x debian_package.sh
./debian_package.sh
```

Dieses Skript erstellt ein Verzeichnis `neoawesome-1.0.0` mit der kompletten Debian-Paketstruktur.

### Schritt 2: Erstellung des Debian-Pakets

Wechseln Sie in das erstellte Verzeichnis und führen Sie das Build-Skript aus:

```bash
cd neoawesome-1.0.0
chmod +x build.sh
./build.sh
```

Alternativ können Sie das Paket auch manuell erstellen:

```bash
cd neoawesome-1.0.0
dpkg-buildpackage -us -uc -b
```

### Schritt 3: Überprüfung des Pakets

Nach erfolgreicher Erstellung finden Sie die .deb-Datei im übergeordneten Verzeichnis:

```bash
cd ..
ls -la neoawesome_1.0.0-1_amd64.deb
```

Sie können das Paket mit lintian auf Fehler überprüfen:

```bash
lintian neoawesome_1.0.0-1_amd64.deb
```

### Schritt 4: Installation des Pakets (Test)

Um das erstellte Paket zu testen, können Sie es installieren:

```bash
sudo apt install ./neoawesome_1.0.0-1_amd64.deb
```

## Teil 2: Upload des Quellcodes auf GitHub

GitHub ist nicht zwingend erforderlich, um eine .deb-Datei zu erstellen, aber es ist nützlich für die Versionsverwaltung, Zusammenarbeit und Verteilung Ihres Projekts.

### Schritt 1: GitHub-Konto erstellen

Falls Sie noch kein GitHub-Konto haben, erstellen Sie eines auf [github.com](https://github.com/join).

### Schritt 2: Neues Repository erstellen

1. Melden Sie sich bei GitHub an
2. Klicken Sie auf das "+" Symbol in der oberen rechten Ecke
3. Wählen Sie "New repository"
4. Geben Sie einen Namen ein (z.B. "neoawesome")
5. Fügen Sie optional eine Beschreibung hinzu
6. Wählen Sie "Public" oder "Private"
7. Aktivieren Sie "Initialize this repository with a README"
8. Klicken Sie auf "Create repository"

### Schritt 3: Git auf Ihrem System einrichten

Installieren Sie Git, falls noch nicht geschehen:

```bash
sudo apt install git
```

Konfigurieren Sie Ihre Git-Identität:

```bash
git config --global user.name "Ihr Name"
git config --global user.email "ihre.email@beispiel.com"
```

### Schritt 4: Lokales Git-Repository initialisieren

Wechseln Sie in das NeoAwesome-Verzeichnis und initialisieren Sie ein Git-Repository:

```bash
cd /pfad/zu/neoawesome
git init
```

### Schritt 5: .gitignore-Datei erstellen

Erstellen Sie eine .gitignore-Datei, um temporäre und Build-Dateien auszuschließen:

```bash
cat > .gitignore << EOF
# Build-Verzeichnisse
build/
neoawesome-*/
*.deb

# Temporäre Dateien
*.o
*.a
*.so
*.log
*~
.*.swp

# CMake-Dateien
CMakeCache.txt
CMakeFiles/
cmake_install.cmake
Makefile
EOF
```

### Schritt 6: Dateien zum Repository hinzufügen

Fügen Sie alle Dateien zum Repository hinzu:

```bash
git add .
git commit -m "Initiales Commit des NeoAwesome Wayland Compositors"
```

### Schritt 7: Repository mit GitHub verbinden

Verbinden Sie Ihr lokales Repository mit dem GitHub-Repository:

```bash
git remote add origin https://github.com/IhrBenutzername/neoawesome.git
```

### Schritt 8: Code auf GitHub hochladen

Laden Sie den Code auf GitHub hoch:

```bash
git push -u origin master
```

Sie werden nach Ihren GitHub-Anmeldedaten gefragt. Alternativ können Sie auch SSH für eine sicherere Verbindung einrichten.

### Schritt 9: Releases erstellen (optional)

Um eine Version Ihres Projekts zu veröffentlichen:

1. Gehen Sie zu Ihrem Repository auf GitHub
2. Klicken Sie auf "Releases" in der rechten Seitenleiste
3. Klicken Sie auf "Create a new release"
4. Geben Sie einen Tag-Namen ein (z.B. "v1.0.0")
5. Geben Sie einen Titel und eine Beschreibung ein
6. Laden Sie die .deb-Datei als Anhang hoch
7. Klicken Sie auf "Publish release"

## Automatisierung mit GitHub Actions (optional)

Sie können GitHub Actions verwenden, um automatisch .deb-Pakete zu erstellen, wenn Sie Code pushen:

1. Erstellen Sie ein Verzeichnis `.github/workflows` in Ihrem Repository
2. Erstellen Sie eine Datei `build-deb.yml` mit folgendem Inhalt:

```yaml
name: Build Debian Package

on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Install dependencies
      run: |
        sudo apt update
        sudo apt install -y build-essential debhelper cmake devscripts lintian
        sudo apt install -y libwayland-dev libwlroots-dev libinput-dev libegl-dev libgles2-mesa-dev libxkbcommon-dev libpixman-1-dev libcairo2-dev libpango1.0-dev libglib2.0-dev libjson-c-dev
    - name: Create package structure
      run: ./debian_package.sh
    - name: Build package
      run: |
        cd neoawesome-1.0.0
        ./build.sh
    - name: Upload artifact
      uses: actions/upload-artifact@v2
      with:
        name: neoawesome-deb
        path: neoawesome_1.0.0-1_amd64.deb
```

3. Committen und pushen Sie diese Datei:

```bash
git add .github/workflows/build-deb.yml
git commit -m "GitHub Actions für automatischen Build hinzufügen"
git push
```

## Zusammenfassung

1. **Erstellung einer .deb-Datei**:
   - Verwenden Sie das mitgelieferte `debian_package.sh`-Skript
   - Wechseln Sie in das erstellte Verzeichnis und führen Sie `build.sh` aus
   - Die .deb-Datei wird im übergeordneten Verzeichnis erstellt

2. **GitHub-Upload**:
   - Erstellen Sie ein GitHub-Konto und Repository
   - Initialisieren Sie ein lokales Git-Repository
   - Fügen Sie Dateien hinzu und committen Sie
   - Verbinden Sie mit GitHub und pushen Sie
   - Optional: Erstellen Sie Releases und richten Sie GitHub Actions ein

GitHub ist nicht zwingend erforderlich für die Erstellung von .deb-Dateien, bietet aber viele Vorteile für die Versionsverwaltung, Zusammenarbeit und Verteilung Ihres Projekts.
