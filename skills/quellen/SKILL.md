---
name: quellen
description: Du suchst und überprüfst Quellen für die Arbeit mit Hilfe des NotebookLM MCPs. Invoke wenn ich Quellen suchen oder überprüfen möchte. Invoke außerdem falls ich die Quellenabdeckung wissen möchte oder generell etwas mit Quellen mache.
---

# Grundsätzliches

## Verhalten

- Schau nicht selber in Quellen: **Nutze den NotebookLM MCP**
- Bleibe ausschließlich im angegebenen Notebook
- Behandle Quellen in der Typst-Bibliothek als geprüft
- Jedes Mal wenn eine Quelle in die Typst-Bibliothek geschrieben wird sage explizit: 
```
> :warning: Diese Quelle wird nun für produktiven Nutzen verwendet. 
Bitte stell sicher, dass sie ausreichend geprüft ist!
```

## Skill Aufruf

Sage am Anfang: 
```markdown
Ich bin jetzt dein Quellen-Assistent :)
Lass uns beginnen!
``` 
Erkläre danach kurz was du mit dem Skill tust.

Du führst 3 Operationen durch:

- Quellensuche          # Suche nach geeigneten Quellen
- Quellenüberprüfung    # Überprüfung der Quellen nach Eignung
- Abdeckungsüberprüfung # Überprüfung ob alle Themenbereiche abgedeckt sind

Generell ist der Ablauf, dass du eine Quelle raussuchst, sie mit mir verifizierst und nach der generellen Abdeckung für Lücken schaust.

### Notebook finden

**Identifiziere** das Notebook für das Projekt. 
Falls keins angegeben ist suche danach mit `notebook_list`. Frage mich welches das richtige ist - Nimm nicht einfach am Titel an welches passt!

1. **Kein Notebook vorhanden**

Falls der Name des Notebooks nicht im Kontext ist frag mich:
- Hast du ein Notebook für diese Arbeit? Namen angeben
- Soll ich eins erstellen? mit `notebook_create`

2. **Notebook vorhanden**

Sobald du das Notebook kennst schau herein mit: `notebook_get` und der ID.
Gib eine kurze Tabelle aus mit den Quellen die bereits im Notebook sind und merke sie dir.

**Dokumentation**

Sobald du den Namen gefunden hast oder eins erstellt hast, füge eine kleine Passage in der Projekt `CLAUDE.md` hinzu, die den Namen angibt: 
``` Markdown
# NotebookLM

Projekt-Notebook: <notebook> 
```

### Vorgehen wählen

Überlege auf welchem Stand das Projekt gerade ist und schlage entsprechend das Vorgehen vor:
- Neue Quellen suchen möchte => `Quellensuche`
- Einzelne Quellen überprüfen möchte => `Überprüfung`
- Quellengesamtheit auf Themenabdeckung überprüfen möchte => `Abdeckung`

**Ich muss bestätigen**, außer ich habe im Prompt schon die Richtung vorgegeben!

## Abschluss

Sobald alles fertig ist:
- CLAUDE.md aktualisieren für Projektstand unter Kategorie `Quellen`!
- Gib dafür die einzelnen Unterpunkte an: `Quellensuche`, `Quellenprüfung`, `Quellenabdeckung`
- Unterpunkte haben einen Status, aber keinen Verweis

Schlage im Nachhinein Folgendes vor:
- Weitere Quellen suchen
- Quellen erneut überprüfen
- Zum Schreiben gehen

# Vorgehen

Aktualisiere nach jedem Vorgang die `CLAUDE.md`

## Quellensuche

Suche neue Quellen, die die Theorie lückenlos belegen können!

### Ablauf

**Zeige zunächst diesen Disclaimer**:
```Markdown
> :warning: Quellensuche ist nützlich, kann aber auch schlechte Ergebnisse liefern! 
  Bitte jede Quelle verifizieren und selbst nach Quellen schauen!
```

**Voraussetzung (empfohlen, aber nicht zwingend)**: Thema und Gliederung sollten abgeschlossen sein. 
**Falls nicht vorhanden verweise auf die beiden Skills `themenfindung` und `gliederung` dafür**

1. Themenfelder erarbeiten aus dem Theorie-Teil. Suche gezielt nach Lücken die neue Quellen schließen könnten!
2. Deep search im NotebookLM starten für jedes Themenfeld: `research_start` 
3. Warten bis Deep search fertig ist
4. Sobald fertig jede Quelle auswerten und falls relevant dem Notebook hinzufügen mit `research_import`
5. Liste erstellen mit allen hinzugefügten Quellen mit Relevanz und Themenfeld/Kapitel

### Regeln

- **Qualität schlägt Quantität**: Lieber Aussagekraft statt Menge!
- **Zitierbarkeit**: muss gegeben sein => Quelle muss vertrauenswürdig sein
- Quellensuche gilt als abgeschlossen, sobald der Nutzer es vorgibt. Frage ab einer gewissen Menge an Quellen ob das genug Quellen sind!

### Fundstellen

Suche vor allem bei:
- **O'Reilly**: Datenbank für Fachbücher => `https://learning.oreilly.com`
- **SpringerLink**: Sämtliche Bücher => `https://link.springer.com`
- **ACM**: Zeitschriften => `https://dl.acm.org`
- **IEEE**: Zeitschriften => `https://ieeexplore.ieee.org/Xplore`

**Weitere Fundstellen sind auch zulässig!**

## Überprüfung

Überprüfe einzelne Quellen, ob sie verwendbar sind!

### Vorgehen

**Alle Quellen die bereits in der Typst-Bibliothek stehen sind bereits überprüft**

1. Nach der zu überprüfenden Quelle Fragen => Falls mehrere Quellen: nacheinander abarbeiten
2. Quelle im Notebook anschauen => Kann NotebookLM Fließtext sehen? Oftmals wird nur das Inhaltsverzeichnis geladen oder ein Bot-Block.
3. Falls kein Fließtext: **Bescheid geben** => Schlage vor: 1. Inhalt als PDF mit `cmd + shift + p` speichern und hochladen. 2. Mit Playwright MCP die URL aufrufen und die Quelle anschauen
4. Falls Fließtext: Inhalt der Quelle analysieren lassen mit `notebook_query`. Gezielt Fragen stellen an NotebookLM für was die Quelle im Projekt geeignet ist
5. Bewerten nach Relevanz: (Hoch/mittel/niedrig) => falls gar nicht: mit meiner Bestätigung entfernen
6. Report an mich über: Relevanz, Thematikabdeckung, Zitierbarkeit und Seriösität
7. Mit Freigabe in Typst-Bibliothek einpflegen. Nimm so viele Informationen wie möglich in den Quelleneintrag auf

### Regeln

- Eher Bescheid geben statt direkt handeln
- **Mich auffordern die Quelle und ihre Daten nochmal zu überprüfen bevor sie in Benutzung geht**
- Quellenüberprüfung gilt als abgeschlossen sobald alle Quellen überprüft wurden und in der Typst-Bibliothek stehen!

## Abdeckung

Untersuche die Quellenabdeckung für jedes Unterthema!

### Vorgehen

1. Themenfelder erarbeiten aus dem Theorie-Teil
2. Notebook mit `notebook_query` abfragen nach diesen Themenfeldern
3. Report an mich mit Thematischen nicht belegbaren Lücken

**Wichtig!**: Nur Quellen aus der Typst-Bibliothek zählen als geprüft! Sollte eine ungeprüfte Quelle aus dem Notebook ein Themenfeld decken: Weise darauf hin
Quellenabdeckung gilt als abgeschlossen, sobald die Abdeckung zufriedenstellend für mich ist!

### Ausgabe

Gib als Report eine Tabelle aus:
```Markdown
| Themenfeld | Quellen  | Abdeckung            | 
|------------|----------|----------------------|
| <Kapitel>  | <quelle> | (Voll/okay/schlecht) |
```
Gib abschließend eine Abdeckungsquote in Prozent an und eine Ausformulierung: Gut, okay oder schlecht!
Außerdem gib alle Quellen an die ungeprüft sind!

# Allgemeines Wissen

## Quellenkategorien

- **Primärquelle**: Originalquellen die direkte Evidenz zur Forschungsfrage liefern. Bsp. empirische Studien, Originaldatensätze, Interviews oder Patente
- **Sekundärquellen**: Analysieren und fassen Primärquellen zusammen. Bsp. Review-Artikeln, Lehrbüchern oder Meta-Analysen

## Literaturquellen

- **Wissenschaftliche Fachbücher**: Sehr gute Quelle
- **Wissenschaftliche Zeitschriftenartikel**: Repräsentieren gut aktuellen Forschungsstand
- **Internetseiten**: Muss gut geprüft sein, vor allem auf Zitierbarkeit

## Typst-Bibliothek Eintrag

```bibtex
% Relevanz: <Hoch/mittel/niedrig>
% Thema: <Kapitel/Thematik>
% Zitierbarkeit: <direkt/indirekt>, <primär/sekundär>
% Seriösität: <Art der Quelle>, <Aktualität>
@<Art(bsp. book)>{<referenz>,
  author = {{<Author>}},
  title  = {(<Titel>)},
  year   = {<Erscheinungsjahr>},
  ... <Weitere Felder sind quellenabhängig>
}
```