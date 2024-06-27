# Quiz Solutions

## encoding

1. Welche der folgenden Aussagen über Unicode-Codierung sind korrekt?

   Lösung: d) UTF steht für Unicode Transformation Format

2. Was passiert, wenn ein Text-Editor das UTF-8 Byte Order Mark (BOM) nicht erkennt?

   Lösung: b) Das BOM wird als sichtbare Zeichen "ï»¿" angezeigt  

3. Welche Aussage zur Kollation in MySQL ist korrekt?

   Lösung: b) Die Endung "_ci" bedeutet case-insensitive Sortierung

## basic_sql

1. Welcher SQL-Befehl wird verwendet, um die Struktur einer Tabelle anzuzeigen?

   Lösung: c) DESCRIBE  

2. Was ist eine Transaktion in Bezug auf Datenbanken?

   Lösung: b) Ein Satz von Datenbankoperationen, die als eine Einheit behandelt werden

3. Welche Aussage zum Locking bei InnoDB-Tabellen ist korrekt?

   Lösung: c) Es wird Row-Level-Locking verwendet

## auth_priviledges

1. Was bedeutet der Begriff "Autorisierung" im Kontext von Datenbanken?

   Lösung: b) Die Zuweisung von Zugriffsrechten für authentifizierte Benutzer

2. Welcher Befehl wird verwendet, um Benutzerrechte in MySQL zu überprüfen?

   Lösung: b) SHOW GRANTS FOR

3. Was bewirkt der Befehl "REVOKE ALL PRIVILEGES ON *.* FROM 'user'@'host';"?

   Lösung: b) Entzieht dem Benutzer alle Rechte auf allen Datenbanken und Tabellen

## innodb

1. Welches ist das aktuelle Standard-Tabellenformat von MySQL?

   Lösung: b) InnoDB

2. Welche Eigenschaft ist charakteristisch für InnoDB-Tabellen?

   Lösung: b) Unterstützung für Transaktionen

3. Was ist ein "Tablespace" im Kontext von InnoDB?

   Lösung: b) Ein virtueller Speicherbereich, der alle InnoDB-Tabellen enthält

## myisam

1. Welche Dateien werden für eine MyISAM-Tabelle namens "CUSTOMERS" erstellt?

   Lösung: a) CUSTOMERS.myd, CUSTOMERS.myi, CUSTOMERS.frm

2. Welche Aussage über MyISAM-Tabellen ist korrekt?

   Lösung: c) Sie speichern Daten und Indizes in separaten Dateien

3. Welcher Vorteil wird oft MyISAM-Tabellen zugeschrieben?

   Lösung: c) Schnellere Leseoperationen bei bestimmten Anwendungsfällen

## client

1. Welcher Befehl wird verwendet, um eine Verbindung zu einem MySQL-Server auf einem entfernten Host herzustellen?

   Lösung: b) mysql -h 139.79.124.97 -u root -p

2. Was bewirkt der Befehl "mysqldump -h 139.79.124.97 hotel > datei.txt"?

   Lösung: b) Erstellt ein Backup der Datenbank "hotel" vom Server mit der IP 139.79.124.97

3. Wie kann man prüfen, ob ein MySQL-Server auf einer bestimmten IP-Adresse läuft?

   Lösung: c) mysqladmin -h 139.79.124.97 -u [Benutzername] -p ping

## client_server

1. Welche Aufgabe hat der Datenbankserver im Vergleich zum Datenbankclient?

   Lösung: c) Datenbank verwalten, Abfragen ausführen und Zugriffe kontrollieren

2. Warum könnte man MS Access zusammen mit einem MySQL-Server verwenden?

   Lösung: b) Um Access als Frontend für Benutzeroberfläche zu nutzen, während MySQL als robuster Datenspeicher dient

3. Wozu dient der Datenbankclient "mysqlshow"?

   Lösung: b) Um das Datenbankschema anzuzeigen

## transactions

1. Wie stellen Transaktionen die Datenkonsistenz bei einem Datenbankserver-Absturz sicher?

   Lösung: c) Durch Verwendung von Logging-Mechanismen wie Write-Ahead Logging

2. Welche Art von Sperre (Lock) verwendet ein SELECT-Befehl, um zu warten, bis alle Transaktionen auf die angeforderte Tabelle entsperrt sind?

   Lösung: c) Shared Lock oder Read Lock

3. Wie muss Autocommit konfiguriert werden, damit jeder SQL-Befehl zu einer Transaktion gehört und explizit mit COMMIT abgeschlossen werden muss?

   Lösung: b) SET autocommit = 0;

## dbms

1. Was ist die Hauptaufgabe eines ODBC-Treibers?

   Lösung: c) Einheitlichen Zugriff einer Anwendung auf verschiedene Datenbanken ermöglichen

2. Welche Aussage über ODBC-Treiber ist korrekt?

   Lösung: c) Sie übersetzen Anwendungsanfragen in datenbankspezifische Befehle

3. In welchem Kontext wird ODBC häufig verwendet?

   Lösung: c) Für den datenbankunabhängigen Zugriff in verschiedenen Anwendungen

## configuration

1. Auf welche Weise können Konfigurationsparameter für einen MySQL-Server nicht definiert werden?

   Lösung: c) Durch einen INSERT-Befehl in eine spezielle Systemtabelle

2. Welcher Konfigurationsparameter bestimmt den Speicherort für Log-Dateien in MySQL?

   Lösung: d) log-bin

3. Mit welchem Eintrag beginnt der Abschnitt für Server-Parameter in der MySQL-Konfigurationsdatei?

   Lösung: b) [mysqld]

## logging

1. In welcher Log-Datei von MySQL würden Sie Informationen über einen Benutzer finden, der bestimmte Daten gelöscht hat?

   Lösung: b) General Query Log oder Binary Log

2. Welche Informationen enthält das Slow Query Log?

   Lösung: c) SQL-Anweisungen, die länger als ein festgelegter Schwellenwert zur Ausführung benötigen

3. Wie können Sie den Inhalt des Binary Logs überprüfen?

   Lösung: c) Mit dem Tool "mysqlbinlog"

## optimization

1. Welche der folgenden Maßnahmen kann die Leistung eines Datenbankservers nicht verbessern?

   Lösung: c) Vermeidung von Indizes

2. Wie kann man Daten schneller in eine Datenbanktabelle laden?

   Lösung: c) Durch Importieren der Daten aus einer Textdatei

3. Wozu wird der Befehl EXPLAIN in MySQL verwendet?

   Lösung: b) Um den Ausführungsplan einer SELECT-Abfrage anzuzeigen