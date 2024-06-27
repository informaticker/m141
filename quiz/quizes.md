# Quiz

## encoding

1. Welche der folgenden Aussagen über Unicode-Codierung sind korrekt?

   a) UTF-8 verwendet immer 8 Bit pro Zeichen
   b) UTF-16 und UTF-8 verwenden dasselbe Byte Order Mark
   c) Unicode hat einen 32-Bit Zeichensatz
   d) UTF steht für Unicode Transformation Format

2. Was passiert, wenn ein Text-Editor das UTF-8 Byte Order Mark (BOM) nicht erkennt?

   a) Der Editor stürzt ab
   b) Das BOM wird als sichtbare Zeichen "ï»¿" angezeigt  
   c) Der Text wird falsch codiert dargestellt
   d) Es passiert gar nichts

3. Welche Aussage zur Kollation in MySQL ist korrekt?

   a) 'utf8_general_cs' ist die Standardeinstellung
   b) Die Endung "_ci" bedeutet case-insensitive Sortierung
   c) Eine Kollation gilt immer für die gesamte Datenbank
   d) Binärsortierung ignoriert Groß- und Kleinschreibung

## basic_sql

1. Welcher SQL-Befehl wird verwendet, um die Struktur einer Tabelle anzuzeigen?

   a) SHOW TABLE
   b) SELECT * FROM
   c) DESCRIBE  
   d) CREATE TABLE

2. Was ist eine Transaktion in Bezug auf Datenbanken?

   a) Eine einzelne SQL-Anweisung
   b) Ein Satz von Datenbankoperationen, die als eine Einheit behandelt werden
   c) Der Prozess des Backups einer Datenbank
   d) Eine Methode zur Verschlüsselung von Daten

3. Welche Aussage zum Locking bei InnoDB-Tabellen ist korrekt?

   a) Es wird immer Table-Level-Locking verwendet
   b) Nur ganze Tabellen können gesperrt werden
   c) Es wird Row-Level-Locking verwendet
   d) Locking ist bei InnoDB nicht möglich

## auth_priviledges

1. Was bedeutet der Begriff "Autorisierung" im Kontext von Datenbanken?

   a) Die Überprüfung der Benutzeridentität
   b) Die Zuweisung von Zugriffsrechten für authentifizierte Benutzer
   c) Die Verschlüsselung von Benutzerdaten
   d) Die Erstellung neuer Benutzerkonten

2. Welcher Befehl wird verwendet, um Benutzerrechte in MySQL zu überprüfen?

   a) CHECK PRIVILEGES
   b) SHOW GRANTS FOR
   c) LIST USER RIGHTS
   d) DISPLAY PERMISSIONS

3. Was bewirkt der Befehl "REVOKE ALL PRIVILEGES ON *.* FROM 'user'@'host';"?

   a) Löscht den Benutzer aus der Datenbank
   b) Entzieht dem Benutzer alle Rechte auf allen Datenbanken und Tabellen
   c) Gibt dem Benutzer alle Rechte
   d) Ändert das Passwort des Benutzers

## innodb

1. Welches ist das aktuelle Standard-Tabellenformat von MySQL?

   a) MyISAM
   b) InnoDB
   c) MEMORY
   d) ARCHIVE

2. Welche Eigenschaft ist charakteristisch für InnoDB-Tabellen?

   a) Schnellster Lesezugriff
   b) Unterstützung für Transaktionen
   c) Keine Unterstützung für Fremdschlüssel
   d) Speicherung jeder Tabelle in separaten Dateien

3. Was ist ein "Tablespace" im Kontext von InnoDB?

   a) Eine physische Datei, die nur Indexdaten enthält
   b) Ein virtueller Speicherbereich, der alle InnoDB-Tabellen enthält
   c) Eine Konfigurationsdatei für InnoDB-Einstellungen
   d) Ein spezieller Cachebereich für häufig abgefragte Daten

## myisam

1. Welche Dateien werden für eine MyISAM-Tabelle namens "CUSTOMERS" erstellt?

   a) CUSTOMERS.myd, CUSTOMERS.myi, CUSTOMERS.frm
   b) CUSTOMERS.data, CUSTOMERS.index, CUSTOMERS.struct
   c) CUSTOMERS.tb, CUSTOMERS.idx, CUSTOMERS.def
   d) CUSTOMERS.table, CUSTOMERS.index, CUSTOMERS.format

2. Welche Aussage über MyISAM-Tabellen ist korrekt?

   a) Sie unterstützen Transaktionen
   b) Sie verwenden standardmäßig Row-Level-Locking
   c) Sie speichern Daten und Indizes in separaten Dateien
   d) Sie sind das neueste und empfohlene Tabellenformat in MySQL

3. Welcher Vorteil wird oft MyISAM-Tabellen zugeschrieben?

   a) Bessere Unterstützung für gleichzeitige Schreibzugriffe
   b) Automatische Datenkomprimierung
   c) Schnellere Leseoperationen bei bestimmten Anwendungsfällen
   d) Integrierte Verschlüsselung der Daten

## client

1. Welcher Befehl wird verwendet, um eine Verbindung zu einem MySQL-Server auf einem entfernten Host herzustellen?

   a) mysql connect 139.79.124.97
   b) mysql -h 139.79.124.97 -u root -p
   c) mysqladmin -connect 139.79.124.97
   d) mysql_connect('139.79.124.97')

2. Was bewirkt der Befehl "mysqldump -h 139.79.124.97 hotel > datei.txt"?

   a) Stellt die Datenbank "hotel" aus der Datei "datei.txt" wieder her
   b) Erstellt ein Backup der Datenbank "hotel" vom Server mit der IP 139.79.124.97
   c) Führt die SQL-Befehle aus "datei.txt" auf der Datenbank "hotel" aus
   d) Zeigt den Inhalt der Datenbank "hotel" auf dem Bildschirm an

3. Wie kann man prüfen, ob ein MySQL-Server auf einer bestimmten IP-Adresse läuft?

   a) ping 139.79.124.97
   b) mysql -h 139.79.124.97 -u root -p
   c) mysqladmin -h 139.79.124.97 -u [Benutzername] -p ping
   d) netstat -an | grep 3306

## client_server

1. Welche Aufgabe hat der Datenbankserver im Vergleich zum Datenbankclient?

   a) Nur Anfragen an die Datenbank senden
   b) Benutzeroberfläche für Dateneingabe bereitstellen
   c) Datenbank verwalten, Abfragen ausführen und Zugriffe kontrollieren
   d) Ausschließlich Daten anzeigen

2. Warum könnte man MS Access zusammen mit einem MySQL-Server verwenden?

   a) Um die Sicherheit von MySQL zu verbessern
   b) Um Access als Frontend für Benutzeroberfläche zu nutzen, während MySQL als robuster Datenspeicher dient
   c) Um die Geschwindigkeit von MySQL-Abfragen zu erhöhen
   d) Um Daten automatisch zwischen beiden Systemen zu synchronisieren

3. Wozu dient der Datenbankclient "mysqlshow"?

   a) Um Backups zu erstellen
   b) Um das Datenbankschema anzuzeigen
   c) Um die Verbindung zum Datenbankserver zu testen
   d) Um den Inhalt von Protokolldateien anzuzeigen

## transactions

1. Wie stellen Transaktionen die Datenkonsistenz bei einem Datenbankserver-Absturz sicher?

   a) Durch automatische Datenkompression
   b) Durch regelmäßige Backups
   c) Durch Verwendung von Logging-Mechanismen wie Write-Ahead Logging
   d) Durch Sperrung aller Tabellen während der Transaktion

2. Welche Art von Sperre (Lock) verwendet ein SELECT-Befehl, um zu warten, bis alle Transaktionen auf die angeforderte Tabelle entsperrt sind?

   a) Exclusive Lock
   b) Update Lock
   c) Shared Lock oder Read Lock
   d) Write Lock

3. Wie muss Autocommit konfiguriert werden, damit jeder SQL-Befehl zu einer Transaktion gehört und explizit mit COMMIT abgeschlossen werden muss?

   a) SET autocommit = 1;
   b) SET autocommit = 0;
   c) SET autocommit = TRUE;
   d) SET autocommit = OFF;

## dbms

1. Was ist die Hauptaufgabe eines ODBC-Treibers?

   a) SQL-Befehle an den entsprechenden Datenbankserver anpassen
   b) ODBC-Datenquellen (DSN) erstellen und konfigurieren
   c) Einheitlichen Zugriff einer Anwendung auf verschiedene Datenbanken ermöglichen
   d) Zugriff einer Anwendung auf eine bestimmte Datenbank ermöglichen

2. Welche Aussage über ODBC-Treiber ist korrekt?

   a) Sie sind nur für Microsoft-Datenbanken verfügbar
   b) Sie ermöglichen direkten Zugriff auf die Datenbankdateien
   c) Sie übersetzen Anwendungsanfragen in datenbankspezifische Befehle
   d) Sie ersetzen die Notwendigkeit von SQL-Kenntnissen vollständig

3. In welchem Kontext wird ODBC häufig verwendet?

   a) Nur für den Zugriff auf MySQL-Datenbanken
   b) Ausschließlich in Webanwendungen
   c) Für den datenbankunabhängigen Zugriff in verschiedenen Anwendungen
   d) Nur für die Verbindung zwischen zwei Datenbankservern

configuration

1. Auf welche Weise können Konfigurationsparameter für einen MySQL-Server nicht definiert werden?

   a) Durch Eintrag in einer Konfigurationsdatei
   b) Durch Eintrag auf der Kommandozeile
   c) Durch einen INSERT-Befehl in eine spezielle Systemtabelle
   d) Durch Setzen von Umgebungsvariablen

2. Welcher Konfigurationsparameter bestimmt den Speicherort für Log-Dateien in MySQL?

   a) logdir
   b) datadir
   c) basedir
   d) log-bin

3. Mit welchem Eintrag beginnt der Abschnitt für Server-Parameter in der MySQL-Konfigurationsdatei?

   a) [mysql]
   b) [mysqld]
   c) [server]
   d) [configuration]

## logging

1. In welcher Log-Datei von MySQL würden Sie Informationen über einen Benutzer finden, der bestimmte Daten gelöscht hat?

   a) Error Log
   b) General Query Log oder Binary Log
   c) Slow Query Log
   d) Redo Log

2. Welche Informationen enthält das Slow Query Log?

   a) Alle erfolgreichen Anmeldeversuche
   b) Detaillierte Fehlerinformationen des Servers
   c) SQL-Anweisungen, die länger als ein festgelegter Schwellenwert zur Ausführung benötigen
   d) Alle Datenbankänderungen in binärem Format

3. Wie können Sie den Inhalt des Binary Logs überprüfen?

   a) Mit einem gewöhnlichen Texteditor
   b) Mit dem Befehl "SHOW BINARY LOGS"
   c) Mit dem Tool "mysqlbinlog"
   d) Durch direktes Lesen der Datei mit "cat" oder "type"

## optimization

1. Welche der folgenden Maßnahmen kann die Leistung eines Datenbankservers nicht verbessern?

   a) Optimierung der Serverparameter
   b) Verwendung von Transaktionen
   c) Vermeidung von Indizes
   d) Optimierung von SQL-Abfragen

2. Wie kann man Daten schneller in eine Datenbanktabelle laden?

   a) Durch Komprimieren der Daten vor der Übertragung
   b) Durch Verwendung vieler einzelner INSERT-Befehle
   c) Durch Importieren der Daten aus einer Textdatei
   d) Durch Erhöhung der Netzwerklatenz

3. Wozu wird der Befehl EXPLAIN in MySQL verwendet?

   a) Um langsame Abfragen zu finden
   b) Um den Ausführungsplan einer SELECT-Abfrage anzuzeigen
   c) Um Daten schneller in die Datenbank zu laden
   d) Um Datenbankfehler zu erklären
