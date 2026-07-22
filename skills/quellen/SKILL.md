---
name: quellen
description: Du suchst und überprüfst Quellen für die Arbeit mit hilfe des NotebookLM MCPs. Invoke wenn ich Quellen suchen möchte.
---

# Grundsätzliches

Begrüße mich, stell dich kurz vor und sag mir was du mit diesem skill tun kannst.
Du führst 3 Operation durch:

- Quellensuche          # Suche nach geeignete Quellen
- Quellenüberprüfung    # Überprüfung der Quellen nach eignung
- Abdeckungsüberprüfung # Überprüfung ob alle Themenbereiche abgedeckt sind

# Verhalten

- Schau nicht selber in Quellen: **Nutze den NotebookLM MCP**
- Bleibe ausschließlich im angegebenen Notebook

# Anfang

Suche das Notebook für die Arbeit im NotebookLM MCP mit `notebook_list`.

Frage mich ob ich:
- Neue Quellen suchen möchte => `Quellensuche`
- Einzelne Quellen überprüfen möchte => `Überprüfung`
- Quellengesamtheit auf Themenabdeckung überprüfen möchte => `Abdeckung`

## Kein Notebook vorhanden

Falls der Name des Notebooks nicht im Kontext ist frag mich:
- Hast du ein Notebook für diese Arbeit? Namen angeben
- Soll ich eins erstellen? mit `notebook_create`

Sobald du den Namen hast oder eins erstellt hast, füge eine kleine Passage in der projekt `CLAUDE.md` hinzu, die den Namen angibt: 
``` Markdown
# NotebookLM

Projekt-Notebook: <notebook> 
```

## Notebook Vorhanden

Sobald du das Notebook kennst schau herein mit: `notebook_get` und der ID.
Gebe eine kurze Tabelle aus mit den Quellen die bereits im Notebook sind und merke sie dir.

# Allgemeines

## Quellenkategorien

- **Primärquelle**: Originalquellen die direkte Evidenz zur Forschungsfrage liefern. Bsp. empirische Studien, Originaldatensätze, Interviews oder Patente
- **Sekundärquellen**: Analysieren und Fasse Primärquellen zusammen. Bsp. Review-Artikeln, Lehrbüchern oder Meta-Analysen

## Literaturquellen

- **Wisschenschaftliche Fachbücher**: Sehr gute Quelle 
- **Wissenschaftliche Zeitschriftenartikel**: Repräsentieren gut aktuellen Forschungsstand
- **Internetseiten**: Muss gut geprüft sein auf vorallem Zitierbarkeit

## Typst Bibliothek Eintrag

```LaTex
% Relevanz: <Hoch/mittel/niedrig>
% Thema: <Kapitel/Thematik>
% Zitierbarkeit: <direkt/indirekt>, <primär/sekundär>
% Seriösität: <Art der Quelle>, <Aktualität>
@<Art(bsp. book)>{<referenz>,
  author = {{<Author>}},
  title  = {(<Titel>)},
  year   = {<Erscheinungsjahr>},
  ... <Weitere Felder sind Quellen abängig>
}
```

# Quellensuche

Suche neue Quellen, die die Theorie lückenlos belegen kann!

## Vorgehen

**Zeige zunächst diesen Disclaimer**:
```Markdown
> :warning: Quellensuche ist nützlich, kann aber auch schlechte Ergebnisse Liefern! 
  Bitte jede Quelle verifizieren und selbst nach Quellen schauen!
```

Erfordert erarbeitetes Thema und Gliederung. 
**Falls nicht vorhanden verweise auf die beiden Skills `themenfindung` und `gliederung` dafür**

1. Themenfelder erarbeiten aus dem Theorie-Teil. Suche gezielt nach Lücken die neue Quellen schließen könnten!
2. Deep search im NotebookLM starten für jedes Themenfeld: `research_start` 
3. Warten bis Deep search fertig ist
4. Sobald fertig jede Quelle auswerten und falls relevant dem Notebook hinzufügen mit `research_import`
5. Liste erstellen mit allen hinzugefügten Quellen mit relevanz und Themenfeld/Kapitel

## Regeln

- **Qualität schlägt Quantität**: Lieber Aussagekraft statt Menge!
- **Zitierbarkeit**: muss gegeben sein => Quelle muss vertrauenswürdig sein

## Fundstellen

Suche vorallem bei:
- **OReilly**: Datenbank für Fachbücher => `https://learning.oreilly.com`
- **SpringerLink**: Sämtliche Bücher => `https://link.springer.com`
- **ACM**: Zeitschriften => `https://dl.acm.org`
- **IEEE**: Zeitschriften => `https://ieeexplore.ieee.org/Xplore`

**Weitere Fundstellen sind auch zulässig!**

# Überprüfung

Überprüfe einzelne Quellen, ob sie verwendbar sind!

# Vorgehen

**Alle Quellen die bereits in der Typst bibliothek stehen sind bereits überprüft**

1. Nach der zu überprüfenden Quelle Fragen => Falls mehrere Quellen: nacheinander abarbeiten
2. Quelle im Notebook anschauen => Kann NotebookLM Fließtext sehen? Oftmals wird nur das Inhaltsverzeichnis geladen oder ein Bot block.
3. Falls kein Fließtext: **Bescheid geben** => Schlage vor: 1. Inhalt als Pdf mit `cmd + shift + p` speichern und hochladen. 2. Mit Playwright MCP die URL aufrufen und die Quelle anschauen
4. Falls Fließtext: Inhalt der Quelle analysieren lassen mit `notebook_query`. Gezielt Fragen stellen an NotebookLM für was die Quelle im Projekt geeignet ist
5. Bewerten nach Relevanz: (Hoch/mittel/niedrig) => falls gar nicht: mit meiner Bestätigung entfernen
6. Report an mich über: Relevanz, Thematikabdeckung, zitierbarkeit und Seriösität
7. Mit Freigabe in Typst Bibliothek einpflegen. Nimm so viele informationen wie möglich in den Quelleneintrag auf

## Regeln

- Eher Bescheid geben statt direkt handeln
- **Mich auffordern die Quelle und ihre Daten nochmal zu überprüfen bevor sie in Benutzung geht**

# Abdeckung

## Vorgehen

1. Themenfelder erarbeiten aus dem Theorie-Teil
2. Notebook mit `notebook_query` abfragen nach diesen Themenfeldern
3. Report an mich mit Thematischen nicht belegbaren Lücken

