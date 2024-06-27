# Basic Knowledge (mysql client)
1.  Welcher Befehl testet die Verbindung zum Server-Rechner mit Adresse 139.79.124.97?

    - [ ] mysql -h 139.79.124.97

    - [ ] ipconfig

    - [x] ping 139.79.124.97

    - [ ] mysqladmin -h 139.79.124.97 -u root -p ping

2.  Wozu wird der Parameter -h bei MySQL verwendet?

    - [ ] bewirkt die Abfrage des Passworts

    - [ ] bewirkt die Verbindung als bestimmter Benutzer

    - [ ] Angabe der Adresse des Client-Rechners

    - [x] Angabe der Adresse des Server-Rechners

3.  Was bewirkt der Befehl 'mysqldump -h 139.79.124.97 hotel \> datei.txt'?

    - [ ] Backup der DB hotel in die Datei datei.txt auf Adresse 139.79.124.97

    - [x] Backup der angegebenen DB auf dem Server mit der IP-Adresse 139.79.124.97

    - [ ] Restore der Datenbank hotel auf dem Server mit der Adresse 139.79.124.97

    - [ ] Ausführen des SQL-Skripts datei.txt auf Adresse 139.79.124.97 auf die DB hotel

4.  Wie greifen Sie vom Konsolenfenster auf einen DB-Server mit Adresse 139.79.124.97 zu?

    - [ ] mysqladmin -h 139.79.124.97

    - [ ] mysql -h 139.79.124.97 hotel \< hotel.bkp

    - [x] mysql -h 139.79.124.97 -u root -p

    - [ ] ping 139.79.124.97
5.  Wie prüfen Sie, ob der DB-Server auf Adresse 139.79.124.97 läuft?

    mysqladmin -h 139.79.124.97 -u [Benutzername] -p ping
    Oder: Versuch einer Verbindung mit mysql -h 139.79.124.97 -u [Benutzername] -p

6.  Welcher Befehl führt das SQL-Skript xy.sql auf die DB hotel auf Adresse 139.79.124.97 aus?

    mysql -h 139.79.124.97 -u [Benutzername] -p hotel < xy.sql

7.  Wie beeinflusst der Parameter --opt beim Erstellen eines Backup das Tabellenlocking?

    --opt aktiviert das Tabellenlocking während des Backups, um Konsistenz zu gewährleisten. (Enabled by default)

8. Beschreiben Sie eine praktische Anwendung für den READ-Lock.

    Ein READ-Lock kann verwendet werden, um konsistente Backups zu erstellen, ohne Schreiboperationen zu blockieren. Dies ermöglicht das Lesen der Daten für Backup-Zwecke, während andere Benutzer weiterhin lesend auf die Daten zugreifen können.
