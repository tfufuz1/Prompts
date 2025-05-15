  
  
Um eine umfassende und strategisch ausgearbeitete Taxonomie für Prompts an Sprachmodelle zu erstellen, die sich auf die Ausgabeprodukte konzentriert, würde ich folgenden Ansatz vorschlagen:  
  
Hauptkategorien definieren: Zunächst sollten wir die grundlegenden Kategorien von Ausgabeprodukten festlegen. Diese könnten wie folgt aussehen:  
a) Informative Inhalte  
b) Analytische Inhalte  
c) Kreative Inhalte  
d) Praktische Hilfestellungen  
e) Interaktive Inhalte  
  
Unterkategorien entwickeln: Für jede Hauptkategorie erstellen wir Unterkategorien, die spezifische Ausgabeprodukte repräsentieren.  
Prompt-Struktur festlegen: Für jede Unterkategorie entwickeln wir eine einheitliche Prompt-Struktur, die die wesentlichen Elemente für das gewünschte Ausgabeprodukt enthält.  
Variablen und Platzhalter einführen: Wir verwenden Variablen und Platzhalter, um die Prompts flexibel und anpassbar zu gestalten.  
Metadaten hinzufügen: Jeder Prompt erhält Metadaten wie Tags, Beschreibungen und Anwendungsbeispiele.  
Hier ist ein Beispiel für die Umsetzung dieser Strategie:  
  
json  
  
Copy  
{  
  "Informative Inhalte": {  
    "Erklärung": {  
      "prefix": ["/", "Erklärung"],  
      "scope": "plaintext",  
      "body": [  
        "Erkläre ausführlich und leicht verständlich das Konzept von ${1:Thema}:",  
        "- Was ist ${1:Thema}?",  
        "- Wie funktioniert ${1:Thema}?",  
        "- Warum ist ${1:Thema} wichtig?",  
        "- Nenne einige praktische Beispiele für ${1:Thema}."  
      ],  
      "description": "Detaillierte Erklärung eines Konzepts",  
      "tags": ["erklärung", "konzept", "definition"]  
    },  
    "Zusammenfassung": {  
      "prefix": ["/", "Zusammenfassung"],  
      "scope": "plaintext",  
      "body": [  
        "Fasse die wichtigsten Punkte von ${1:Thema} in maximal 5 Stichpunkten zusammen:",  
        "1.",  
        "2.",  
        "3.",  
        "4.",  
        "5."  
      ],  
      "description": "Kurze Zusammenfassung eines Themas",  
      "tags": ["zusammenfassung", "überblick", "kernpunkte"]  
    }  
  },  
  "Analytische Inhalte": {  
    "Vergleich": {  
      "prefix": ["/", "Vergleich"],  
      "scope": "plaintext",  
      "body": [  
        "Vergleiche ${1:Objekt_A} und ${2:Objekt_B} in Bezug auf folgende Aspekte:",  
        "1. Gemeinsamkeiten:",  
        "2. Unterschiede:",  
        "3. Vor- und Nachteile von ${1:Objekt_A}:",  
        "4. Vor- und Nachteile von ${2:Objekt_B}:",  
        "5. Anwendungsbereiche:",  
        "Fazit: Welches ist in welchen Situationen vorzuziehen?"  
      ],  
      "description": "Detaillierter Vergleich zweier Objekte oder Konzepte",  
      "tags": ["vergleich", "analyse", "gegenüberstellung"]  
    },  
    "SWOT-Analyse": {  
      "prefix": ["/", "SWOT"],  
      "scope": "plaintext",  
      "body": [  
        "Führe eine SWOT-Analyse für ${1:Unternehmen/Produkt} durch:",  
        "Stärken (Strengths):",  
        "- ",  
        "Schwächen (Weaknesses):",  
        "- ",  
        "Chancen (Opportunities):",  
        "- ",  
        "Risiken (Threats):",  
        "- ",  
        "Fazit und Handlungsempfehlungen:"  
      ],  
      "description": "SWOT-Analyse für ein Unternehmen oder Produkt",  
      "tags": ["swot", "analyse", "strategisch"]  
    }  
  },  
  "Kreative Inhalte": {  
    "Kurzgeschichte": {  
      "prefix": ["/", "Kurzgeschichte"],  
      "scope": "plaintext",  
      "body": [  
        "Schreibe eine Kurzgeschichte mit folgenden Elementen:",  
        "- Hauptfigur: ${1:Charakter}",  
        "- Setting: ${2:Ort/Zeit}",  
        "- Konflikt: ${3:Problem}",  
        "- Genre: ${4:Genre}",  
        "Länge: Etwa 500 Wörter"  
      ],  
      "description": "Generierung einer Kurzgeschichte mit vorgegebenen Elementen",  
      "tags": ["kreativ", "geschichte", "fiktion"]  
    },  
    "Gedicht": {  
      "prefix": ["/", "Gedicht"],  
      "scope": "plaintext",  
      "body": [  
        "Verfasse ein Gedicht zum Thema ${1:Thema}:",  
        "- Stil: ${2:Stil (z.B. Sonett, Haiku, frei)}",  
        "- Stimmung: ${3:Stimmung}",  
        "- Besondere Anforderung: ${4:Anforderung (z.B. Reim, Alliteration)}"  
      ],  
      "description": "Erstellung eines Gedichts mit spezifischen Vorgaben",  
      "tags": ["kreativ", "poesie", "lyrik"]  
    }  
  },  
  "Praktische Hilfestellungen": {  
    "Schritt-für-Schritt-Anleitung": {  
      "prefix": ["/", "Anleitung"],  
      "scope": "plaintext",  
      "body": [  
        "Erstelle eine detaillierte Schritt-für-Schritt-Anleitung für ${1:Aufgabe}:",  
        "1. Schritt: ",  
        "2. Schritt: ",  
        "3. Schritt: ",  
        "...",  
        "Tipps und Tricks:",  
        "Häufige Fehler und wie man sie vermeidet:"  
      ],  
      "description": "Erstellung einer schrittweisen Anleitung",  
      "tags": ["anleitung", "how-to", "tutorial"]  
    },  
    "Problemlösung": {  
      "prefix": ["/", "Problemlösung"],  
      "scope": "plaintext",  
      "body": [  
        "Entwickle einen strukturierten Lösungsansatz für folgendes Problem: ${1:Problem}",  
        "1. Problemdefinition:",  
        "2. Mögliche Ursachen:",  
        "3. Lösungsansätze:",  
        "   a) ",  
        "   b) ",  
        "   c) ",  
        "4. Bewertung der Lösungsansätze:",  
        "5. Empfohlene Vorgehensweise:",  
        "6. Mögliche Hindernisse und deren Überwindung:"  
      ],  
      "description": "Strukturierte Problemlösung",  
      "tags": ["problemlösung", "strategie", "entscheidungshilfe"]  
    }  
  },  
  "Interaktive Inhalte": {  
    "Quiz": {  
      "prefix": ["/", "Quiz"],  
      "scope": "plaintext",  
      "body": [  
        "Erstelle ein Quiz mit 5 Fragen zum Thema ${1:Thema}:",  
        "1. Frage: ",  
        "   a) ",  
        "   b) ",  
        "   c) ",  
        "   d) ",  
        "   Richtige Antwort: ",  
        "2. Frage: ",  
        "...",  
        "Erklärungen zu den richtigen Antworten:"  
      ],  
      "description": "Erstellung eines Quizes zu einem bestimmten Thema",  
      "tags": ["quiz", "interaktiv", "lernhilfe"]  
    },  
    "Dialogsimulation": {  
      "prefix": ["/", "Dialog"],  
      "scope": "plaintext",  
      "body": [  
        "Simuliere einen Dialog zwischen ${1:Person_A} und ${2:Person_B} zum Thema ${3:Thema}:",  
        "${1:Person_A}: ",  
        "${2:Person_B}: ",  
        "${1:Person_A}: ",  
        "${2:Person_B}: ",  
        "...",  
        "Fazit des Gesprächs:"  
      ],  
      "description": "Simulation eines Dialogs zwischen zwei Personen",  
      "tags": ["dialog", "interaktiv", "rollenspiel"]  
    }  
  }  
}  
Diese Struktur bietet mehrere Vorteile:  
  
Hierarchische Organisation: Die Taxonomie ist klar strukturiert und ermöglicht eine einfache Navigation und Erweiterung.  
Flexibilität: Durch die Verwendung von Variablen (${1:Variable}) können die Prompts leicht an verschiedene Themen und Kontexte angepasst werden.  
Konsistenz: Jede Kategorie folgt einem ähnlichen Aufbau, was die Benutzung und Erweiterung erleichtert.  
Metadaten: Tags und Beschreibungen erleichtern die Suche und Auswahl passender Prompts.  
Erweiterbarkeit: Neue Kategorien, Unterkategorien und Prompts können einfach hinzugefügt werden, ohne die bestehende Struktur zu beeinträchtigen  
Copy  
Retry  
  
  
Claude does not have the ability to run the code it generates yet.  
Claude can make mistakes. Please double-check responses.  
  
Wie würdest du eine Taxonomie für Prompts/Eingabeaufforderung an Sprachmodelle wie ChatGPT,Claue,Gemini usw. anlegen ?  
Der Fokus sollte auf die Ausgabe "Produkte" wie z.B. "Inhaltsverzeichnis, Beschreibung, Vergleich, Erklärung, Ratgeber ... und so weiter" gelegt sein.  
Erkläre umfassend und strategisch ausgearbeitet wie du das anlegen würdest.  
Genau gesagt geht es um eine Prompt-Bibliothek in form von Snippets.  
Als Beispiel :  
"Erkläre Unterschied": {  
  "prefix": ["/","Unterschied"],  
  "scope": "plaintext",  
  "body": [  
    "Erkläre umfassend aber einfach die Unterschiede zwischen ${1:Vergleich_A} und ${2:Vergleich_B}:",  
    "Was haben ${1:Vergleich_A} und ${2:Vergleich_B} gemeinsam ?",  
    "Worin Unterscheiden sich ${1:Vergleich_A} und ${2:Vergleich_B} ?",  
    "Was ist besonders an ${1:Vergleich_A}?",  
    "Was ist besonders an ${2:Vergleich_B}?",  
    "Was ist der Zweck von ${1:Vergleich_A} und welche Anwendungsgebiete gibt es für ${1:Vergleich_A}?",  
    "Was ist der Zweck von ${2:Vergleich_B} und welche Anwendungsgebiete gibt es für ${2:Vergleich_B}?",  
  ],  
  "description": "Erkläre Unterschied"  
},  
  
Keine ausgewählt

