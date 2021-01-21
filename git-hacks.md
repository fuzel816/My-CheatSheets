Übersicht diverser Befehle für Terminal Version Control
# git diff (Für den Vergleich verschiedener Versionen im Repository)

  - Vergleich zwischen dem aktuellen commit und den getätigten Änderungen -> git diff HEAD
  - Vergleich der Änderungen zwischen zwei branches (hier: master, branchname) -> git diff master...branchname (--name-only)
  - Vergleich der Änderungen zwischen zwei commits einer Datei -> git diff HEAD~<1>:<path-to-file> <path-to-file> (<1> stellt die Tiefe des commits dar)

# git add

  - Hizufügen mehrererer Files mit einer bestimmten Endung -> git add \*.txt

# git branch (Verwalten der einzelnen Branches)

  - Löschen eines lokalen Branches -> git branch -d "Branchname"
  - Umbenennen eines lokalen Branches wenn auf diesen ausgecheckt -> git branch -m <new name>
  - Anzeigen aller branches -> git branch -a

# git mergetool (manuelles Zusammenführen)

  - vzum Lösen eines entstehenden Merge Errors -> git mergetool
  |####LOCAL####|####BASE####|####REMOTE####|
  |#################MERGED##################|
  - LOCAL:  Datei auf dem aktuellen Branch -> :diffg LO
  - BASE:   Datei vor dem Merge Versuch -> :diffg BA
  - REMOTE: Datei aus Mergeversuch -> :diffg RE

# git reset

  - Rücksetzen eines ungewollten commits (datein in commit, die da nicht reingehören)-> git reset --soft (--hard) HEAD~1

#  git stash

*GIT STASH IST GEFÄHRLICH*

- Anzeigen des Stash mit Logeintrag -> git stash list
