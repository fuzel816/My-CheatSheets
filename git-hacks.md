Übersicht diverser Befehle für Terminal Version Control
#git diff (Für den Vergleich verschiedener Versionen im Repository)
	-Vergleich zwischen dem aktuellen commit und den getätigten Änderungen -> git diff HEAD	
#git add
	-Hizufügen mehrererer Files mit einer bestimmten Endung -> git add \*.txt
	-Löschen eines zum Commit hinzugefügten Files -> git reset "filename"
#git branch (Verwalten der einzelnen Branches)
	-Löschen eines lokalen Branches -> git branch -d "Branchname"
#git mergetool (manuelles Zusammenführen)
	-zum Lösen eines entstehenden Merge Errors -> git mergetool
	|####LOCAL####|####BASE####|####REMOTE####|
	|#################MERGED##################|
	-LOCAL:  Datei auf dem aktuellen Branch -> :diffg LO
	-BASE:	 Datei vor dem Merge Versuch -> :diffg BA
	-REMOTE: Datei aus Mergeversuch -> :diffg RE
