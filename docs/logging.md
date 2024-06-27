# Logging
1.  In welcher Log-Datei finden Sie, den Anwender, der bestimmte Daten löschte?

    Im General Query Log oder Binary Log
      

2.  Welche Informationen finden Sie im Slow Query Log?

    - SQL-Anweisungen, die länger als ein festgelegter Schwellenwert zur Ausführung benötigen
    - Ausführungszeit der Abfrage
    - Betroffene Tabellen
    - Anzahl der untersuchten Zeilen

3.  Geben Sie für jede Protokolldatei an, wie Sie deren Inhalt kontrollieren.

    - Error Log: nano oder `tail -f`
    - General Query Log: nano oder `mysqlbinlog` Tool
    - Slow Query Log: nano
    - Binary Log: `mysqlbinlog` Tool