---
name: setup
description: Setup the plugin for a project by doing an interview and writing a `CLAUDE.md`. Invoke when starting a new project is mentioned or the Keyword `setup` is used in the context of writing an essay or assignment.
---

# General purpose

using this skill you create or modify the `CLAUDE.md` in the projects `.claude/` folder.
This shall only be project scoped.
If there is no `.claude/` folder ask me to add it.

You will go through this tasklist, use the task display: 

1. **Analysis:** run the `/academic-paper-plugin:doctor` and look into the `CLAUDE.md` of the project if there is one. 
2. **Interview:** Ask me about necessary information for the project
3. **Write `CLAUDE.md`**: Based on the Information write the `CLAUDE.md` into the Projects `.claude/` folder

# CLAUDE.md Layout

Default language for this is german as the assignment will be written in german. tell me this when setting up and talk german with me.

```markdown
# Projekt <!-- Grobe beschreibung des Projekts und worüber die Arbeit geht -->

# Struktur <!-- Struktur der Arbeit auf der Festplatte. Das ist ein Struktur-vorschlag, wie die meisten projekte aussehen -->

<Ordner>/
└── <Template>/            # Die eigentliche Arbeit (Typst)
    ├── main.typ           # Typst dokument mit dem Inhalt der Arbeit
    ├── main.pdf           # compilierte Arbeit. Wenn du Änderungen sehen möchtest, compiliere main.typ und inspiziere main.pdf
    ├── sources.bib        # LaTeX bibliothek mit allen Quellen
    ├── glossary.typ       # Sammlung aller glossar einträge
    └── assets/            # Ordner mit allen Bildern, etc.

# Vorgaben

## NotebookLM <!-- enthält Profil und Notebook für die Quellen des projekts -->

## Github <!-- enthält remote github repo und git regeln -->

## Typst konvention <!-- enthält typst coding conventionen -->
```

# Fragen für Interview

Use the user interface for interviewing me. i want to click things rather than type. If the questions demand type i want to type into a box, not a seperate prompt

## Projekt

- Wer bist du? (Name, Rolle, etc.)
- Was für eine Art wissenschaftliche Arbeit schreibst du? (projektarbeit, bachelorarbeit, etc.)
- Worüber geht die Arbeit? (Grobes Thema)

## Struktur
 
Schau dir die Struktur des Projekts an. Falls sie nicht wie das Beispiel aussieht, frag mich ob die Struktur so fix ist oder das Template noch hinzugefügt wird.

## NotebookLM

- Hast du ein NotebookLM notebook? Auswahl: Ja ~Eingabe; nein, erstelle eins; nein, ich erstelle eins

## Github

- Hast du ein Github Repository für diese Arbeit? (Link für repo)
- Soll automatisch oder nur nach Befehl commited/gepusht werden?
- wie oft soll commited/nach commit gefragt werden? Auswahl: Nach jedem Kapitel; nur nach anweisung

## Typst Konvention

- Was ist dir bei Typst code wichtig? (Regeln für Typst)
- Hast du ein Typst skript als beispiel? (Nimm ein typst skript entgegen und entnehme die wichtigsten Formatierungs regeln des codes)
