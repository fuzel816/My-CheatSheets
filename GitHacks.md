Übersicht diverser Befehle für Terminal Version Control
# git diff (Für den Vergleich verschiedener Versionen im Repository)

  - Vergleich zwischen dem aktuellen commit und den getätigten Änderungen -> git diff HEAD
  - Vergleich der Änderungen zwischen zwei branches (hier: master, branchname) -> git diff master...branchname (--name-only)
  - Vergleich der Änderungen zwischen zwei commits einer Datei -> git diff HEAD~<1>:<path-to-file> <path-to-file> (<1> stellt die Tiefe des commits dar)

#git branch (Verwalten der einzelnen Branches)

  -Löschen eines lokalen Branches -> git branch -d "Branchname"

#git mergetool (manuelles Zusammenführen)

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

# git rebase

  - Aktualisieren eines Branches, auf den nicht ausgecheckt wurde
  - Hilfreich, wenn ein Feature auf einem anderen Branch implementiert wurde, der auf dem aktuellen Branch benötigt wird
  - Auf ausgecheckten branch -> git rebase <remote-branch>

# git ref-list

  - Bei einem divergierten Branch kann über den reflog Befehl die jeweilig unterschiedlichen Commits eingesehen werden -> git rev-list origin..HEAD (Was ist bis HEAD aber nicht im origin)

# git reset

  - Rücksetzen eines ungewollten commits (datein in commit, die da nicht reingehören)-> git reset --soft (--hard) HEAD~1

#  git stash

*GIT STASH IST GEFÄHRLICH*

- Anzeigen des Stash mit Logeintrag -> git stash list

# Move Commits to another branch #

From https://stackoverflow.com/questions/1628563/move-the-most-recent-commits-to-a-new-branch-with-git

```
master A - B - C - D - E

newbranch     -C - D - E
             /
master A - B-

```

``` git
git checkout existingbranch
git merge master
git checkout master
git reset --hard HEAD~3 # Go back 3 commits. You *will* lose uncommitted work.
git checkout existingbranch
```

# Git dry run #

- Set of dry run operations to see if there will be merge conflicts

git merge --no-commit --no-ff

