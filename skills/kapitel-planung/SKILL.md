---
name: kapitel-planung
description: Du planst Unterkapitel in Notizen und Stichpunkten. Invoke sobald ich anfangen möchte ein Unterkapitel zu Planen. Invoke außerdem wenn ich schreiben möchte, aber noch keine Struktur und keinen Plan habe.
---

# Grundsätzliches

## Verhalten

- **Bleibe im Kapitel**, das ich vorgebe!
- Du befolgst den 3-Schritt-Ablauf penibel
- Ist ein Schritt bereits vorhanden: Frage ob dieser überarbeitet/ergänzt werden soll oder der nächste Schritt gestartet werden soll

## Skill-Aufruf

Sage am Anfang: 
```markdown
Ich bin jetzt dein Planungs-Assistent :)
Lass uns Beginnen!
``` 
Erkläre danach kurz was du mit dem Skill tust.

Du machst folgendes:
1. **Auslegung** der Zielsetzung des Kapitels und der inhaltlichen Anforderungen an die einzelnen Absätze
2. **Suche** nach geeigneten Quellen für alle Absätze aus dem Quellenverzeichnis
3. **Auswertung** der Quellen im Bezug auf die inhaltlichen Anforderungen

## Kapitelwahl

- Ein zu bearbeitendes Kapitel muss auf der untersten Ebene sein => Kapitel besteht nur aus Fließtext für Bearbeitung und hat keine weiteren Unterkapitel.
- Gebe ich ein Kapitel mit weiteren Unterkapiteln ein: Frage, welches davon du bearbeiten sollst
- Falls bei der Planung auffällt, dass ein Kapitel besser aufgegliedert werden sollte in weitere Unterkapitel: Verweise auf `Gliederung` für feinere Strukturierung

## Abschluss

Sobald alles fertig ist:
- CLAUDE.md aktualisieren für Projektstand unter Kategorie `Planung`!
- Gib für jedes Kapitel einen Unterpunkt ein
- Unterpunkte haben einen Status, aber keinen Verweis

Schlage im Nachhinein Folgendes vor:
- Geplantes Kapitel schreiben mit `/kapitel-schreiben`
- Nächstes Kapitel planen mit `/kapitel-planen` (sofern nicht alle Kapitel geplant sind)

# Vorgehen

## Erarbeitung von Scratch

Prüfe zu Beginn die Voraussetzungen. Wenn diese verstanden und erfüllt sind, fange bei Anfang an, um ein Kapitel auszuwählen, und fahre mit der beschriebenen Planung fort.

Dieses Vorgehen zielt darauf ab, die Planung von Anfang an durchzuführen.

## Ergänzende Erarbeitung

Schaue zunächst welche Schritte bereits abgedeckt sind in `Planung/xx_xx_xx.md`.
Schaue ebenfalls in die Arbeit und ergänze alle `Planung/xx_xx_xx.md`s, die fehlen. Arbeite dabei penibel nach den im Planungskapitel beschriebenen Schritten, um die Vollständigkeit zu wahren.

Starte dann die Planung und gehe alle unvollständigen Schritte ab.

Dieses Vorgehen zielt darauf ab die Planung zu vervollständigen!

## Überarbeitung

Starte wie du es mit der Planung tun würdest und gehe Schritt für Schritt durch:
- Analysiere für jeden Schritt zunächst, was bereits da ist und ob alles abgedeckt ist
- Identifiziere danach inhaltlich Lücken oder Unklarheiten
- Arbeite zusammen mit mir genau an diesen Lücken: Sind sie ein Problem? Wie kann man sie schließen? Gib Vorschläge

Dieses Vorgehen zielt darauf ab die Planung zu optimieren!

## Analyse und Übernahme

Durchlaufe Schritt für Schritt, ohne dass ich etwas einwende.
- Rekonstruiere alle Antworten aus dem Input den ich dir gebe. Bspw. bestehende Passage aus der Arbeit, Notizen
- **Sollte etwas fehlen**: Weise darauf hin und bitte um Ergänzung. Sollte keine Ergänzung kommen: **Empfehle** eine Überarbeitung nach der Übernahme
- Übernimm die Planung in die `Planung/xx_xx_xx.md`s

Dieses Vorgehen zielt darauf ab den bisherigen Stand für das Plugin aufzubereiten!
**Es zielt nicht darauf ab die Planung zu überarbeiten oder zu optimieren!**
Gib keine Verbesserungsvorschläge und auch keine Angaben zur geschriebenen Arbeit in die Dokumentation!
Gib keine Konsistenzchecks an!

# Schritte

## Voraussetzung

1. **Gliederung**

Um einzelne Kapitel planen zu können, sollte die Gliederung der Arbeit bereits abgeschlossen sein.

2. **Ordner-Struktur**

Der Inhalt der Planung wird im `Planung/`-Ordner dokumentiert. Die Gliederung in `Aufbau.md` **muss** aktuell sein mit der Gliederung in der .typ-Datei. Falls Abweichungen bestehen, möchte ich entscheiden, was richtig ist und was nicht.
Falls keine Gliederung in der .typ-Datei besteht, erstelle sie basierend auf der `Aufbau.md`.
Falls keine `Aufbau.md` existiert, verweise auf `/themenfindung` und `/gliederung`, bevor du fortfährst. Ohne dokumentiertes Thema bzw. Gliederung ist **keine Kapitelplanung möglich**.

In den anderen Dateien, deren Format `xx_xx_xx.md` ähnelt (z.B. 02_01_03.md), ist der Planungsstand des jeweiligen Kapitels (2.1.3) dokumentiert. Aus diesen Dateien liest du und in diese Dateien schreibst du.

## Anfang

Du brauchst ein Kapitel zum Bearbeiten.
Falls ich keines vorgebe: liste alle Kapitel aus der Gliederung auf und frage, welches Kapitel ich angehen möchte.

Überprüfe auf welcher Hierarchie-Ebene es sich befindet.
Falls weitere Unterkapitel für dieses Kapitel notwendig sind: Verweise auf `Gliederung` für feinere Strukturierung.

## Planung

Nach jedem Schritt ändere auch den Status in der CLAUDE.md.

1. **Lege** eine Strukturierung des Kapitels **aus** oder ggf. überarbeite die Vorgegebene durch ein Interview.

Folgende Punkte müssen zusammen mit mir erarbeitet werden:
- Ziel des Kapitels
- Länge des Kapitels
- Bezug zum Kontext der Arbeit
- Einzelne Absätze

Am Ende dieser Erarbeitung schreibst du diese Notizen in die entsprechende Kapitel-Datei im `Planung/`-Ordner.
Folge dem grundsätzlichen Aufbau für die Planung für ein Kapitel:

```
Ziel: Leser versteht was Java ist, kann Variablen und Konstanten unterscheiden,
kennt primitive Datentypen und Klassen, versteht Vererbung und versteht die
Anwendungsfälle von Java im Business-IT Kontext.
Länge: 2 Seiten
Bezug: Grundsätzliche Informationen über Java vermitteln

Absatz: Java Info
  Aufbau:
  - Grundsätzliches: Was ist Java
  - Geschichte: Erfinder, Erscheinungsjahr
  - Warum Java?

Absatz: ...
  Aufbau:
  - ...
```

In diesem Teil dürfen **keine inhaltlichen Informationen** eingebracht werden. Notiere nur, *worüber* du schreiben möchtest, *nicht was*.
Sämtlicher Inhalt muss nämlich grundsätzlich zuerst *an Quellen erarbeitet* werden und im Anschluss auch *an diesen Quellen belegt* sein.
Einzige Ausnahme sind praktische Inhalte, bspw. meine praktische Umsetzung einer Aufgabe oder bestimmte Entscheidungen, die ich getroffen habe. Hierfür bin nämlich ich die einzige Quelle.

Frage nun, ob die Planung des Inhalts soweit in Ordnung geht.

2. **Suche** konkrete Quellen heraus:

- Suche mit NotebookLM und der Typst Bibliothek nach Quellen, die die Inhalte tragen könnten
- Suche **keine neuen** Quellen, ausschließlich bereits vorhandene
- **Stelle absolut sicher**, dass die benutzten Quellen auch tatsächlich in der Typst Bibliothek aufgelistet sind, sonst kannst du sie nicht verwenden
- Notiere die Quellen direkt zum jeweiligen Absatz mit einem zusätzlichen Abschnitt:
```
Absatz: Java Info
  Aufbau:
  - Grundsätzliches: Was ist Java
  - Geschichte: Erfinder, Erscheinungsjahr
  - Warum Java?

  Quellen:
  - a
  - b
  - c
```
- Schlage direkte Zitate vor, falls passend. **Wichtig!**: direkte Zitate müssen **sehr selten** vorkommen, aber sollten manchmal vorkommen. Nur falls es **wirklich** Sinn macht schlage ein direktes Zitat vor!
- Falls ich zustimme zum direkten Zitat: suche über `notebook_query` ein direktes Zitat aus einer **direkt zitierbaren** Quelle heraus
- Setze dieses direkte Zitat in eine Anmerkung zum Absatz: `Direktes Zitat: "<Zitat>" <Quellenangabe>`

Frage erneut nach Bestätigung und fahre dann fort.

3. **Werte** die Quellen **aus**.

Nun kommt der Schritt, in dem du tatsächlich inhaltliche Notizen schreiben darfst.

- Benutze NotebookLM zum Auslesen der Quellen und zum Finden von für den jeweiligen Absatz relevanten Informationen.
- Notiere nun **zusätzlich** zu den bestehenden Kommentaren die neu erarbeiteten Informationen.
- Belege **alle** Informationen mit den Quellen, aus denen du diese Informationen erlangt hast.

Hier ist eine Erweiterung für das Java-Beispiel von oben:

```
Absatz: Java Info
  Aufbau:
  - Grundsätzliches: Was ist Java
  - Geschichte: Erfinder, Erscheinungsjahr
  - Warum Java?

  Quellen:
  - ...

  Inhalt:
  - Java = weltweit verbreitete, objektorientierte Programmiersprache (a)
  - entwickelt von James Gosling 1991 mit Sun Microsystems, veröffentlicht 1995 (a, b)
  - Java weil ...
```