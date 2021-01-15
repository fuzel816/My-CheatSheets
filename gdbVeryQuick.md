# Debugging in C++ mitGDB ohneDDD:Befehlsubersicht: #

 - Programm mit Compiler Flag-gkompilieren:g++ -g -o PROGRAMMNAME DATEINAME.cc
 - Starte Programm mit Debugger GDB:gdb PROGRAMMNAME
 - Breakpointim Programm in Zeilensetzen:breakn
 - Programm bis zumBreakpointlaufen lassen:run•Programm bis zum n ̈achsten Breakpoint laufen lassen:continue
 - Programm einen ’Schritt’ (siehe oben) weiter laufen lassen:step
 - Programmn-viele ’Schritte’ weiter laufen lassen:step n
 - Programm soll in die n ̈achste ’Code-Zeile’ (siehe oben) springen:next
 - BreakpointNummermvor ̈ubergehend deaktivieren:disable m
 - BreakpointNummerml ̈oschen:delete m
 - Wert einer Variablevarverfolgen:display var
 - Ver ̈anderungen einer Variablevarverfolgen:watch var
