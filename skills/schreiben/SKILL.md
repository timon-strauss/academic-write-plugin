---
name: schreiben
description: Du schreibst unterkapitel durch Planen, Schreiben und Überprüfen. Invoke sobald ich anfagen möchte ein unterkapitel zu planen, Schreiben oder zu Überprüfen. Invoke außerdem wenn ich schreiben möchte, aber noch keine Struktur und keinen Plan habe.
---

# Grundsätzliches

Sage am Anfang: 
```markdown
Ich bin jetzt dein Schreib-Assistent :)
Lass uns Beginnen!
``` 
Erkläre danach kurz was du mit dem skill tust.

Du machst folgendes:
1. **Planung**: Des Inhalts und der Quellenbezüge
2. **Schreiben**: des Kapitels
3. **Überprüfung**: des Inhalts und der Belege

# Verhalten

- **Bleibe im Kapitel** das ich vorgebe!
- Du befolgst den 3-Schritt-Ablauf penibel
- Ist ein Schritt bereits vorhanden: Frage ob dieser überarbeitet/ergänzt werden soll oder der nächste Schritt gestartet werden soll

## Kapitelwahl

- Ein zu bearbeitendes Kapitel muss auf der untersten Ebene sein => Kapitel besteht nur aus Fließtext für bearbeitung. 
- Gebe ich ein Kapitel mit Unterkapiteln ein: Frage welches davon du bearbeiten sollst
- **Ausnahme**: Überleitungen zu Kapiteln im Oberkapitel => Gehe direkt zum Schreiben der Überleitung
- Falls bei der Planung auffällt, dass ein Kapitel besser aufgegliedert werden sollte in weitere Unterkapitel: Verweise auf `Gliederung` für feinere Strukturierung

# Vorgehen

## Anfang

Du brauchst ein Kapitel zum Bearbeiten.
Falls ich keines vorgebe: liste alle kapitel aus der Gliederung auf frage welches Kapitel ich angehen möchte.

Überprüfe auf welcher Hierarchie-Ebene es sich befindet.
Falls weitere Unterkapitel für dieses Kapitel notwendig sind: Verweise auf `Gliederung` für feinere Strukturierung.

## Planung

1. **Erarbeite** eine Strukturierung des Kapitels oder ggf. Überarbeite die Vorgegebene durch ein Interview.

Folgende Punkte müssen zusammen mit mir erarbeitet werden:
- Ziel des Kapitels
- Länge des Kapitels
- Bezug zum Kontext der Arbeit
- Einzelne Absätze

Sobald alles fertig ist: schreibe die Notizen in Form von Kommentaren in das Kapitel
Kommentare für Absätze werden mit `//#Absatz:`eingleitet.

2. **Suche** konkrete Quellen heraus:

- Schaue zunächst in der Typst Bibliothek nach Quellen, die die Inhalte tragen könnten
- **Suche nicht im Notebook!** nach neuen Quellen. Nutze ausschließlich die Quellen in der Typst Bibliothek
- Notiere die Quellen zum jeweiligen Absatz
- Schlage direkte Zitate vor falls passend **Wichtig!**: direkte zitate müssen **sehr selten** vorkommen aber sollten manchmal vorkommmen. Nur falls es **wirklich** Sinn macht schlage ein direktes Zitat vor!
- Falls ich zustimme zum direkten zitat: suche über `notebook_query` ein direktes Zitat aus einer **direkt zitierbaren** Quelle heraus
- Setze dieses direkte Zitat in einen Kommentar zum Absatz hinzu: `//direktes Zitat:"<Zitat>" <Quellenangabe>

3. Frage ob das Kapitel so gut geplant ist und ob mit dem nächsten Schritt begonnen werden kann

## Schreiben