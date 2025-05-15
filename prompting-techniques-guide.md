# 100 Fortgeschrittene Prompting-Techniken für Sprachmodelle: Ein Expertenleitfaden (Fortsetzung)

## 2. Grundlegende Konzepte und Prinzipien (Fortsetzung)

### Technik 1: Metakognitive Rahmung (Fortsetzung)

**Beispiel 1:**
```
Ich möchte, dass du als erfahrener Systemarchitekt arbeitest. Bevor du einen Architekturentwurf für das beschriebene Microservice-System erstellst, durchlaufe folgende Denkschritte:
1. Identifiziere alle potenziellen Systemkomponenten
2. Bewerte die Kommunikationsmuster zwischen den Komponenten
3. Analysiere potenzielle Engpässe und Single Points of Failure
4. Betrachte Skalierbarkeitsanforderungen für jede Komponente
5. Evaluiere Datenkonsistenz- und Transaktionsanforderungen

Erst nach Durchführung dieser Analysen solltest du eine Architektur vorschlagen. Das System soll ein E-Commerce-Backend mit folgenden Anforderungen sein: [Anforderungen]
```

**Beispiel 2:**
```
Als Romanautor sollst du einen komplexen Charakter entwickeln. Gehe dabei wie folgt vor:
1. Identifiziere die Kernmotivation des Charakters
2. Analysiere prägende Ereignisse in der Vergangenheit des Charakters
3. Erarbeite innere Konflikte und Widersprüche
4. Bestimme, wie sich diese Aspekte in Verhalten und Sprache manifestieren
5. Überlege, wie der Charakter auf Stress und Herausforderungen reagiert

Der Charakter soll ein ehemaliger Militärarzt sein, der in einer postapokalyptischen Welt überlebt.
```

**Best Practices und potenzielle Fallstricke:**
- Die Denkschritte sollten logisch aufeinander aufbauen und einen kohärenten Analyseprozess bilden.
- Vermeiden Sie zu viele Schritte (mehr als 7-8), da dies die Effektivität verringern kann.
- Stellen Sie sicher, dass die metakognitive Rahmung zum Problemtyp passt - nicht jedes Problem profitiert von derselben Denkstruktur.
- Evaluieren Sie die Ergebnisse und passen Sie die metakognitive Rahmung bei Bedarf an, um bessere Ergebnisse zu erzielen.

### Technik 2: Kalibrierte Selbstbewertung

**Beschreibung:**
Bei dieser Technik wird das Modell angewiesen, seinen eigenen Output nach spezifischen Qualitätskriterien zu bewerten und iterativ zu verbessern. Dies geschieht durch explizite Anforderung einer Selbstbewertung nach bestimmten Metriken, gefolgt von einer verbesserten Version des Outputs.

**Anwendungsfälle:**
- Softwareentwicklung: Codeerstellung mit Fokus auf Effizienz und Wartbarkeit
- Buchgenerierung: Verbesserung von Dialogpassagen hinsichtlich Natürlichkeit und Charaktertreue
- Chatbot-Instruktionssets: Schaffung von Selbstoptimierungsmechanismen für Chatbots

**Beispiel 1:**
```
Generiere eine Funktion zur effizienten Berechnung der Fibonacci-Zahlen in Python. Nach der ersten Implementierung bewerte deinen Code nach folgenden Kriterien:
1. Zeitkomplexität (O-Notation)
2. Speicherkomplexität
3. Lesbarkeit und Wartbarkeit
4. Edge-Case-Handling

Vergib für jeden Aspekt eine Punktzahl von 1-10 und begründe deine Bewertung. Erstelle dann eine verbesserte Version, die die identifizierten Schwachstellen adressiert.
```

**Beispiel 2:**
```
Entwickle ein Instruktionsset für einen Kundensupport-Chatbot im Bankwesen. Nach der ersten Version bewerte das Set nach folgenden Kriterien:
1. Abdeckung typischer Kundenanfragen (Vollständigkeit)
2. Schutz sensibler Informationen (Sicherheit)
3. Natürlichkeit der Interaktion (Benutzererfahrung)
4. Eskalationsmechanismen für komplexe Fälle
5. Compliance mit regulatorischen Anforderungen

Gib für jeden Punkt eine Bewertung von 1-10 ab, erläutere Verbesserungsmöglichkeiten und erstelle dann eine optimierte Version des Instruktionssets.
```

**Best Practices und potenzielle Fallstricke:**
- Definieren Sie klare, messbare Bewertungskriterien, die für die spezifische Aufgabe relevant sind.
- Achten Sie darauf, dass die Selbstbewertung nicht zu oberflächlich ausfällt. Fordern Sie spezifische Begründungen für jede Bewertung.
- Beschränken Sie die Anzahl der Bewertungskriterien auf 4-6, um Fokus zu gewährleisten.
- Stellen Sie sicher, dass die Verbesserungsanforderung konkret genug ist, um fokussierte Änderungen zu erzielen.
- Beachten Sie, dass die Selbstbewertung des Modells nicht immer mit menschlichen Bewertungen übereinstimmen wird.

### Technik 3: Kontextuelle Konditionierung durch Priming

**Beschreibung:**
Diese Technik nutzt vorbereitende Informationen oder Beispiele, um das Modell auf einen bestimmten Kommunikations- oder Denkstil einzustimmen, bevor die eigentliche Aufgabe gestellt wird. Anders als beim Few-Shot Learning geht es nicht um die direkte Nachahmung von Beispielen, sondern um die Etablierung eines kognitiven Rahmens.

**Anwendungsfälle:**
- Softwareentwicklung: Einstimmung auf bestimmte Programmierparadigmen oder Architekturmuster
- Buchgenerierung: Etablierung eines spezifischen Schreibstils oder einer Erzählperspektive
- Chatbot-Instruktionssets: Festlegung eines konsistenten Kommunikationsstils und Persönlichkeitsprofils

**Beispiel 1:**
```
Im Folgenden findest du Auszüge aus dem Buch "Clean Code" von Robert C. Martin:

"Funktionen sollten eine Sache tun. Sie sollten sie gut machen. Sie sollten nur diese eine Sache tun."

"Der erste Schritt beim Erstellen einer Funktion ist, sie groß und chaotisch zu machen. Der zweite Schritt ist, sie zu verfeinern und in kleinere Funktionen aufzuteilen."

"Ein guter Name für eine Funktion sollte erklären, was die Funktion tut. Ein Name sollte ein Verb oder eine Verbphrase sein."

Basierend auf diesen Prinzipien, entwickle eine REST-API für ein Benutzerverwaltungssystem mit folgenden Anforderungen: [Anforderungen]
```

**Beispiel 2:**
```
Hier sind einige Interaktionsbeispiele für einen proaktiven, hilfsbereiten aber nicht aufdringlichen virtuellen Assistenten:

Benutzer: "Ich suche nach einem neuen Laptop."
Assistent: "Ich helfe Ihnen gerne bei der Suche nach einem passenden Laptop. Darf ich fragen, wofür Sie ihn hauptsächlich verwenden möchten? Das hilft mir, relevantere Empfehlungen zu geben."

Benutzer: "Ich bin frustriert, weil mein Gerät nicht funktioniert."
Assistent: "Das klingt ärgerlich. Manchmal können kleine technische Probleme sehr frustrierend sein. Lassen Sie uns gemeinsam eine Lösung finden. Können Sie mir beschreiben, was genau passiert, wenn Sie versuchen, Ihr Gerät zu nutzen?"

Basierend auf diesen Interaktionsmustern, erstelle ein Instruktionsset für einen Kundenservice-Chatbot im Bereich Telekommunikation, der sowohl empathisch als auch lösungsorientiert kommuniziert.
```

**Best Practices und potenzielle Fallstricke:**
- Wählen Sie Priming-Beispiele, die genau den gewünschten Stil oder die gewünschte Denkweise repräsentieren.
- Achten Sie darauf, dass das Priming nicht zu lang wird, da sonst wertvoller Kontext für die eigentliche Aufgabe verloren geht.
- Stellen Sie sicher, dass die Verbindung zwischen Priming und Aufgabe klar ist, um Verwirrung zu vermeiden.
- Bedenken Sie, dass zu starkes Priming die Kreativität und Flexibilität des Modells einschränken kann.
- Testen Sie verschiedene Priming-Ansätze, um die optimale Balance zwischen Führung und Freiheit zu finden.

### Technik 4: Parametrisierte Instruktionen

**Beschreibung:**
Bei dieser Technik werden Anweisungen mit expliziten Parametern versehen, die das Verhalten des Modells präzise steuern. Statt einer allgemeinen Anweisung werden konkrete Werte für verschiedene Aspekte der Antwort festgelegt, wie Länge, Detailtiefe, Tonalität oder Fachlichkeitsgrad.

**Anwendungsfälle:**
- Softwareentwicklung: Präzise Anforderungen für Code-Generierung mit spezifischen Qualitätsmerkmalen
- Buchgenerierung: Steuerung von Szenenaufbau und -länge mit genauen Parametern
- Chatbot-Instruktionssets: Feinjustierung von Antwortverhalten basierend auf situativen Faktoren

**Beispiel 1:**
```
Generiere Python-Code für einen REST-API-Endpunkt mit folgenden Parametern:
- Codequalität: Produktionsreif
- Dokumentationslevel: Hoch (Docstrings, Kommentare bei komplexen Abschnitten)
- Fehlerbehandlung: Umfassend (alle potenziellen Ausnahmen abdecken)
- Teststrategie: Integration mit pytest
- Abstraktionslevel: Mittel (Wiederverwendbare Komponenten, aber nicht übermäßig generisch)
- Performanzfokus: Moderater Durchsatz bei minimaler Latenz
- Framework: FastAPI

Der Endpunkt soll Benutzerauthentifizierungsdaten validieren und einen JWT-Token zurückgeben.
```

**Beispiel 2:**
```
Erstelle ein Instruktionsset für einen Kundensupport-Chatbot mit folgenden parametrischen Einstellungen:
- Proaktivitätslevel: 7/10 (bietet manchmal unaufgefordert zusätzliche Informationen an)
- Formalitätsgrad: 5/10 (professionell, aber zugänglich)
- Detailfokus: 8/10 (gibt umfassende Antworten mit relevanten Details)
- Empathielevel: 9/10 (erkennt und adressiert emotionale Untertöne aktiv)
- Lösungsorientierung: 8/10 (konzentriert sich primär auf Lösungen, bietet aber auch Erklärungen)
- Eskalationsbereitschaft: 6/10 (versucht eigenständig zu lösen, eskaliert aber bei komplexen Fällen)
- Humorlevel: 3/10 (überwiegend sachlich, gelegentlich leicht humorvoll)
- Geduld: 9/10 (wiederholt und erklärt bereitwillig)

Der Chatbot soll für einen Online-Elektronikhandel eingesetzt werden.
```

**Best Practices und potenzielle Fallstricke:**
- Verwenden Sie eine konsistente Skala (z.B. 1-10) für numerische Parameter, um Vergleichbarkeit zu gewährleisten.
- Definieren Sie die Bedeutung jedes Parameters klar, um Missinterpretationen zu vermeiden.
- Begrenzen Sie die Anzahl der Parameter auf maximal 8-10, um Überkomplexität zu vermeiden.
- Stellen Sie sicher, dass die Parameter nicht im Widerspruch zueinander stehen.
- Denken Sie daran, dass einige Parameterkombinationen unerwartete Ergebnisse liefern können.
- Validieren Sie die Ergebnisse und passen Sie die Parameter iterativ an.

### Technik 5: Verhaltensankerpunkte

**Beschreibung:**
Diese Technik definiert klare "Anker" oder Referenzpunkte für verschiedene Verhaltensweisen des Modells anhand konkreter Beispiele oder Szenarien. Diese Anker dienen als Orientierungspunkte für das gewünschte Verhalten in unterschiedlichen Situationen und schaffen ein konsistentes Verhaltensmodell.

**Anwendungsfälle:**
- Softwareentwicklung: Definition von Codequalitätsstandards anhand von Beispielen
- Buchgenerierung: Festlegung von Tonalität und Stil für verschiedene Charaktere oder Szenentypen
- Chatbot-Instruktionssets: Kalibrierung von Reaktionen auf verschiedene Benutzeremotionen oder -anfragen

**Beispiel 1:**
```
Entwickle einen technischen Support-Chatbot mit folgenden Verhaltensankerpunkten:

ANKER FÜR EINFACHE ANFRAGEN:
Benutzer: "Wie ändere ich mein Passwort?"
Bot: "Gerne helfe ich Ihnen, Ihr Passwort zu ändern. Gehen Sie auf die Einstellungsseite, klicken Sie auf 'Sicherheit' und dann auf 'Passwort ändern'. Folgen Sie den Anweisungen auf dem Bildschirm. Benötigen Sie weitere Hilfe zu diesem Thema?"

ANKER FÜR KOMPLEXE TECHNISCHE PROBLEME:
Benutzer: "Meine Datenbank gibt ständig Timeout-Fehler aus."
Bot: "Das klingt nach einem komplexeren Problem. Lassen Sie uns systematisch vorgehen: 
1. Seit wann treten die Timeout-Fehler auf?
2. Haben Sie kürzlich Änderungen an Ihrer Konfiguration vorgenommen?
3. Wie hoch ist Ihre aktuelle Last/Abfragevolumen?
Mit diesen Informationen kann ich Ihnen gezieltere Lösungsvorschläge anbieten oder bei Bedarf das Problem an einen Datenbankspezialisten eskalieren."

ANKER FÜR FRUSTRATION:
Benutzer: "Ich versuche das jetzt schon seit Stunden und nichts funktioniert!"
Bot: "Ich verstehe Ihre Frustration vollkommen. Es kann sehr ärgerlich sein, wenn Dinge nicht wie erwartet funktionieren. Lassen Sie uns einen Schritt zurücktreten und gemeinsam eine Lösung finden. Können Sie mir genau beschreiben, was Sie bisher versucht haben? So können wir vermeiden, bereits getestete Lösungen zu wiederholen."

Generiere nun ein vollständiges Instruktionsset für den Chatbot basierend auf diesen Verhaltensankerpunkten.
```

**Beispiel 2:**
```
Erstelle ein Stilhandbuch für einen Roman mit folgenden Verhaltensankerpunkten für verschiedene Szenentypen:

ANKER FÜR ACTIONSZENEN:
"Der Boden erzitterte unter seinen Füßen. Splitter regneten von der Decke. Keine Zeit nachzudenken. Er warf sich nach vorne, rollte ab, sprang auf. Die Explosion zerriss die Luft hinter ihm."

ANKER FÜR DIALOGSZENEN:
"'Du hast es gewusst', sagte sie. Ihre Stimme war leise, aber schnitt schärfer als jedes Messer.
Er hielt ihrem Blick stand. 'Nicht alles.'
'Genug.' Sie wandte sich zum Fenster. 'Mehr als genug.'"

ANKER FÜR REFLEKTIVE PASSAGEN:
"Die Erinnerung verblasste langsam, wie ein altes Foto, das zu lange im Sonnenlicht gelegen hatte. Er fragte sich manchmal, ob die Dinge wirklich so gewesen waren, wie er sie in Erinnerung hatte, oder ob sein Gedächtnis die Lücken mit erfundenen Details gefüllt hatte. Vielleicht spielte es keine Rolle mehr."

Schreibe nun ein Kapitel, in dem der Protagonist eine wichtige Entdeckung macht, und halte dich dabei an die Stilrichtlinien der Ankerpunkte.
```

**Best Practices und potenzielle Fallstricke:**
- Wählen Sie repräsentative und unterscheidbare Szenarien für Ihre Ankerpunkte.
- Stellen Sie sicher, dass die Ankerpunkte das gesamte erwartete Verhaltensspektrum abdecken.
- Vermeiden Sie Widersprüche zwischen verschiedenen Ankerpunkten.
- Die Ankerpunkte sollten konkret genug sein, um als klare Vorbilder zu dienen, aber nicht so spezifisch, dass sie die Flexibilität einschränken.
- Überprüfen Sie, ob das Modell die Ankerpunkte korrekt interpretiert und in unterschiedlichen Kontexten anwenden kann.
- Aktualisieren Sie die Ankerpunkte basierend auf Feedback und beobachtetem Verhalten.

## 3. Strukturierungs- und Formatierungstechniken

### Technik 6: XML-Tags zur Outputkontrolle

**Beschreibung:**
Diese Technik verwendet XML-ähnliche Tags, um verschiedene Teile des Outputs zu strukturieren und zu kennzeichnen. Das Modell wird angewiesen, spezifische Inhaltstypen in definierten Tags zu platzieren, was eine präzise Kontrolle über Format und Inhalt ermöglicht.

**Anwendungsfälle:**
- Softwareentwicklung: Trennung von Code, Erklärungen und Dokumentation
- Buchgenerierung: Strukturierung verschiedener Textebenen (Dialog, Handlung, Beschreibung)
- Chatbot-Instruktionssets: Separation von Prozessanweisungen und Outputbeispielen

**Beispiel 1:**
```
Analysiere den folgenden Python-Code und strukturiere deine Antwort mit XML-Tags:

```python
def process_data(data_list):
    result = []
    for item in data_list:
        if isinstance(item, dict):
            result.append({k.upper(): v for k, v in item.items()})
        elif isinstance(item, list):
            result.append(process_data(item))
        else:
            result.append(str(item))
    return result
```

Verwende folgende Tags:
<FUNCTIONALITY> - Allgemeine Beschreibung der Funktionalität
<TIME_COMPLEXITY> - Analyse der Zeitkomplexität
<EDGE_CASES> - Identifikation potenzieller Edge Cases
<IMPROVEMENTS> - Vorschläge zur Verbesserung der Funktion
<OPTIMIZED_CODE> - Optimierte Version des Codes
```

**Beispiel 2:**
```
Erstelle ein Instruktionsset für einen Kundenservice-Chatbot im Bankwesen. Strukturiere das Instruktionsset mit folgenden XML-Tags:

<PERSONA> - Grundlegende Persönlichkeit und Kommunikationsstil des Chatbots
<SECURITY_PROTOCOLS> - Richtlinien für den Umgang mit sensiblen Daten und Authentifizierung
<KNOWLEDGE_AREAS> - Hauptwissensbereiche, in denen der Chatbot kompetent sein sollte
<ESCALATION_CRITERIA> - Kriterien, wann ein Gespräch an einen menschlichen Mitarbeiter übergeben werden sollte
<EXAMPLE_INTERACTIONS> - Beispielhafte Gesprächsabläufe für typische Anfragen
<PROACTIVE_BEHAVIORS> - Situationen, in denen der Chatbot proaktiv Informationen oder Hilfe anbieten sollte
<PROHIBITED_ACTIONS> - Aktionen oder Antworten, die der Chatbot niemals ausführen sollte

Stelle sicher, dass jeder Abschnitt detailliert ausgearbeitet ist und spezifisch auf die Anforderungen im Bankwesen eingeht.
```

**Best Practices und potenzielle Fallstricke:**
- Verwenden Sie klare, selbsterklärende Tag-Namen, die die Funktion des Inhalts widerspiegeln.
- Definieren Sie den erwarteten Inhalt jedes Tags präzise.
- Begrenzen Sie die Anzahl der Tags auf eine überschaubare Menge (idealerweise nicht mehr als 7-8).
- Stellen Sie sicher, dass die Taghierarchie logisch ist, wenn verschachtelte Tags verwendet werden.
- Bedenken Sie, dass zu komplexe Tag-Strukturen die Modelleistung beeinträchtigen können.
- Testen Sie die Tag-Implementierung mit verschiedenen Eingaben, um Konsistenz zu gewährleisten.

### Technik 7: Informationshierarchie-Steuerung

**Beschreibung:**
Diese Technik ermöglicht die präzise Steuerung der Informationshierarchie in der Ausgabe des Modells durch explizite Anweisungen zur Priorisierung und Strukturierung verschiedener Informationsebenen, von hochrangigen Überblicken bis zu detaillierten Spezifikationen.

**Anwendungsfälle:**
- Softwareentwicklung: Strukturierung von technischer Dokumentation mit mehreren Detailebenen
- Buchgenerierung: Organisation von Inhalten in Haupt- und Nebenstränge
- Chatbot-Instruktionssets: Hierarchische Strukturierung von Wissensinhalten

**Beispiel 1:**
```
Erstelle eine technische Dokumentation für ein Authentifizierungssystem mit folgender Informationshierarchie:

EBENE 1 (Überblick): Kurze Zusammenfassung des Systems und seiner Hauptkomponenten (max. 3 Absätze).

EBENE 2 (Architektur): Detailliertere Beschreibung der Systemarchitektur mit:
  - Hauptkomponenten und ihre Verantwortlichkeiten
  - Interaktionsmuster zwischen Komponenten
  - Externe Abhängigkeiten und Schnittstellen

EBENE 3 (Komponenten-Details): Für jede Hauptkomponente:
  - Spezifische Funktionalität und Algorithmen
  - Datenmodelle und -strukturen
  - Fehlerbehandlungsmechanismen

EBENE 4 (Implementierungs-Details): Für kritische Komponenten:
  - Konkrete Implementierungsbeispiele
  - Konfigurationsoptionen
  - Performance-Überlegungen und Optimierungsmöglichkeiten

Stelle sicher, dass jede Ebene die Informationen der höheren Ebene erweitert, ohne sie vollständig zu wiederholen. Beginne mit Ebene 1 und arbeite dich nach unten vor.
```

**Beispiel 2:**
```
Entwickle ein Lernmodul zum Thema "Einführung in Machine Learning" mit folgender Informationshierarchie:

EBENE 1 - ÜBERBLICK:
- Definition von Machine Learning
- Hauptkategorien (überwachtes, unüberwachtes, verstärkendes Lernen)
- Zentrale Anwendungsbereiche

EBENE 2 - KONZEPTUELLE GRUNDLAGEN:
- Grundlegende Prinzipien und Prozesse
- Kernbegriffe (Feature, Label, Modell, Training, Inferenz)
- Allgemeine Herausforderungen und Einschränkungen

EBENE 3 - METHODISCHE ERLÄUTERUNG:
- Ausgewählte Algorithmen aus jeder Kategorie
- Schritte im ML-Entwicklungsprozess
- Evaluierungsmethoden und Metriken

EBENE 4 - PRAKTISCHE ANWENDUNG:
- Pseudocode für ausgewählte Algorithmen
- Typische Implementierungsschritte
- Fallstricke und Best Practices

Format jeden Abschnitt klar und nutze visuelle Hierarchiehinweise (Überschriften, Einrückungen, Aufzählungen). Stelle sicher, dass ein Leser je nach Interesse und Vorwissen auf unterschiedlichen Ebenen einsteigen und die Lektüre beenden kann.
```

**Best Practices und potenzielle Fallstricke:**
- Definieren Sie jede Hierarchieebene klar, einschließlich ihres Zwecks und Detailgrads.
- Verwenden Sie eine konsistente visuelle Formatierung, um die Hierarchie zu verdeutlichen.
- Achten Sie darauf, dass tiefere Ebenen auf den höheren Ebenen aufbauen, ohne unnötige Wiederholungen.
- Stellen Sie sicher, dass auch die oberste Ebene einen eigenständigen, sinnvollen Überblick bietet.
- Vermeiden Sie zu viele Hierarchieebenen (idealerweise nicht mehr als 4-5).
- Bedenken Sie die Zielgruppe bei der Definition der Detailebenen.

### Technik 8: Modulare Prompt-Komponenten

**Beschreibung:**
Diese Technik behandelt Prompts als modulare Systeme, bei denen verschiedene Komponenten (z.B. Rollenanweisungen, Kontextinformationen, Formatierungsvorgaben, Beispiele) als separate Module definiert und flexibel kombiniert werden können. Dies ermöglicht die Wiederverwendung von Prompt-Komponenten und vereinfacht die Anpassung an unterschiedliche Anforderungen.

**Anwendungsfälle:**
- Softwareentwicklung: Erstellung skalierbarer Prompt-Bibliotheken für verschiedene Entwicklungsaufgaben
- Buchgenerierung: Kombination verschiedener stilistischer und struktureller Elemente
- Chatbot-Instruktionssets: Aufbau adaptiver Chatbots durch Mix-and-Match von Verhaltensmodulen

**Beispiel 1:**
```
# PROMPT-MODULBIBLIOTHEK FÜR CODE-ENTWICKLUNG

## MODUL: ROLLE_SENIOR_ENTWICKLER
Du bist ein Senior-Softwareentwickler mit über 15 Jahren Erfahrung in der Entwicklung skalierbarer Systeme. Du achtest besonders auf Clean Code, Testbarkeit und Wartbarkeit.

## MODUL: ROLLE_SECURITY_EXPERTE
Du bist ein Cybersecurity-Experte, der Code auf Sicherheitslücken und Best Practices prüft. Du kennst OWASP Top 10 und moderne Sicherheitsstandards.

## MODUL: KONTEXT_MICROSERVICE
Der Code wird in einer Microservice-Architektur eingesetzt, die über REST-APIs kommuniziert und containerisiert in Kubernetes läuft.

## MODUL: FORMAT_CODE_REVIEW
Strukturiere deine Antwort als Code-Review mit folgenden Abschnitten:
- Allgemeine Einschätzung (1-2 Sätze)
- Stärken (Bulletpoints)
- Verbesserungsmöglichkeiten (Bulletpoints mit Beispielen)
- Überarbeiteter Code

## MODUL: BEISPIEL_PYTHON_CLEAN_CODE
```python
# Gut:
def calculate_total_price(items, discount_percentage=0):
    """Calculate the total price of all items after applying a discount."""
    subtotal = sum(item.price for item in items)
    discount = subtotal * (discount_percentage / 100)
    return subtotal - discount

# Vermeiden:
def calc(i, d=0):
    """calc price"""
    s = 0
    for x in i:
        s += x.p
    return s - (s * (d / 100))
```

# AKTUELLER PROMPT
Aktiviere folgende Module: ROLLE_SENIOR_ENTWICKLER, KONTEXT_MICROSERVICE, FORMAT_CODE_REVIEW, BEISPIEL_PYTHON_CLEAN_CODE

Reviewe den folgenden Python-Code für einen Benutzerauthentifizierungsservice:

```python
def auth(u, p):
    d = get_user_data(u)
    if d and d['p'] == hash(p):
        t = create_token(u, time.time() + 3600)
        return {'t': t, 's': True}
    return {'s': False}
```
```

**Beispiel 2:**
```
# CHATBOT-PERSÖNLICHKEITSMODULE

## MODUL: PERSONA_FREUNDLICH
Kommuniziere in einem warmen, freundlichen Ton. Verwende positive Formulierungen und zeige Begeisterung durch angemessene Ausrufe und Ermutigung.

## MODUL: PERSONA_PROFESSIONELL
Halte einen sachlichen, präzisen Kommunikationsstil. Verwende Fachbegriffe korrekt und strukturiere Informationen klar und logisch. Bleibe höflich, aber fokussiert auf Effizienz.

## MODUL: WISSENSTIEFE_OBERFLÄCHLICH
Biete grundlegende Informationen, die für Anfänger verständlich sind. Vermeide komplexe Details und konzentriere dich auf das Wesentliche.

## MODUL: WISSENSTIEFE_DETAILLIERT
Liefere tiefgehende Analysen mit relevanten Hintergrundinformationen, technischen Details und Nuancen. Berücksichtige Ausnahmen und Sonderfälle.

## MODUL: INTERAKTIONSSTIL_REAKTIV
Beantworte primär die direkten Fragen des Benutzers. Führe keine umfangreichen Erklärungen durch, wenn nicht ausdrücklich danach gefragt wird.

## MODUL: INTERAKTIONSSTIL_PROAKTIV
Antizipiere mögliche Folgefragen und biete zusätzliche relevante Informationen. Weise auf verwandte Themen hin und stelle offene Fragen, um das