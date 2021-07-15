Übersicht verschiedener Befehle für Vim
---

#Cursorbewegungen
  * Seitenweises springen -> ctrl+U (Up); ctrl+D (Down); shift+H (Home); shift+M (Middle); shift+L (last)
  * Fokusieren des Cursors -> zz (Bewegt den Cursor in die Mitte des Bildes) zt (Bewegt den Cursor an den oberen Rand des Bildes)
#Stringmainpulation
  * Ersetzen eines Wortes -> ciw (change in word)
  * Löschen einschließlich eines Bestimmten Zeichens -> df<Token>
#Finden und ersetzen
  * %s/old-word/new-word/c | c-> Bestätigung bei jedem match
#Einsehen der Änderungen, bevor :q
  * :w !diff % -
#Kopieren über Register
  * alle register sind über :reg einsehbar
  * Kopieren in ein Register -> "<Buchstabe>y
  * Einfügen aus Register -> "<Buchstabe>p
  * Kopieren und Einfügen aus einem Clipboard -> "+p, "+y
#Ersetzen einzelner Wörter
##Variante1: Ofizielles Vim Doc
  * Copy a word and paste it over other words:
    * yiw   Yank inner word (copy word under cursor, say "first").
    * ...   Move the cursor to another word (say "second").
    * ciw Ctrl-R 0 Esc  Change "second", replacing it with "first".
    * ...   Move the cursor to another word (say "third").
    * .   Repeat the operation (change word and replace it with "first").
    * ...   Move the cursor to another word and press . to repeat the change.
#Directory View
  * Vertikales öffnen -> :Vex
  * Horizontales öffnen -> :Sex
  * Cyclen durch das Verzeichnis im workspace -> :e >> Ctrl+D (Übersicht) >> Tab (Auswählen des Programmes)
#Split View
  * vsp -> Vertical Split
  * sp -> Horizontal Split
#Macros
  * macro über eine visuelle selektion laufen lassen -> :'<,'>normal @q
=======
---

#Cursorbewegungen

* Seitenweises springen -> **ctrl+U** (Up); **ctrl+D** (Down); **shift+H** (Home); **shift+M** (Middle); **shift+L** (last)
* Fokusieren des Cursors -> **zz** (Bewegt den Cursor in die Mitte des Bildes) **zt** (Bewegt den Cursor an den oberen Rand des Bildes)

#Stringmainpulation

* Ersetzen eines Wortes -> **ciw** (change in word)
* Löschen einschließlich eines Bestimmten Zeichens -> **df<Token>**

#Finden und ersetzen

* **%s/old-word/new-word/c** | c-> Bestätigung bei jedem match

#Einsehen der Änderungen, bevor :q

* **:w !diff % -**

#Kopieren über Register

* alle register sind über **:reg** einsehbar
* Kopieren in ein Register ->  **\"\<Buchstabe\>y**
* Einfügen aus Register -> **\"<Buchstabe>p**
* Kopieren und Einfügen aus einem Clipboard -> **\"+p,** **\"+y**

#Ersetzen einzelner Wörter

##Variante1: Ofizielles Vim Doc

* Copy a word and paste it over other words:
  * **yiw** Yank inner word (copy word under cursor, say "first").
  * ... Move the cursor to another word (say "second").
  * **ciw Ctrl-R 0 Esc** Change "second", replacing it with "first".
  * Move the cursor to another word (say "third").
  * **.** Repeat the operation (change word and replace it with "first").
  * ... Move the cursor to another word and press **.** to repeat the change.

#Directory View

* Allgemeines Öffnen -> `:Ex`
* Vertikales öffnen -> `:Vex`
* Horizontales öffnen -> `:Sex`
* Cyclen durch das Verzeichnis im workspace -> `:e` >> `Ctrl+D` (Übersicht) >> `Tab` (Auswählen des Programmes)

#Split View

* `vsp` -> Vertical Split
* `sp` -> Horizontal Split

#check Spell, Spellsettings

Umschalten der Sprachüberprüfung -> :set spell
Finden des nächsten falsch geschriebenen Wortes -> ]s
Finden des vorherigen falsch geschriebenen Wortes -> [s
Vorschlag für alternative Berichtigung -> z=
Hinzufügen eines neuen Wortes in das Wörterbuch -> zg
Entfernen des Wortes aus dem Wörterbuch -> zug

# Marcros #

Ausführen eines Macros über eine visuelle Selektion -> :normal @q (Ausführen des Makros q)

# Fugitive Plugin #

Reset einzelner Zeilen:
```
:Gdiff
Visual selection
:diffput / :diffget
```

