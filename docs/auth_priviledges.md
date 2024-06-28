# Authentication & Privileges
1.  Was bedeutet der Begriff "Authentifizierung" im Zusammenhang mit einem DB-Server?

    - [ ] Prüfung der Privilegien des Benutzers

    - [ ] Antwort auf die Frage: Wer?

    - [x] Identitätsprüfung

    - [ ] Antwort auf die Frage: Was?

2.  Wann werden Änderungen im Zugriffssystem von MySQL wirksam?

    - [ ] sofort nach Eingabe der Änderung

    - [x] nach dem Befehl FLUSH PRIVILEGES

    - [ ] nach dem Neustart des DB-Servers

    - [ ] nach dem Befehl GRANT

3.  Was bewirkt der SQL-Befehl GRANT ... ON ... TO ...;

    - [x] Privileg(ien) erteilen

    - [ ] Privileg(ien) wegnehmen

    - [x] User erstellen, falls noch nicht vorhanden

    - [ ] User löschen

4.  Mit welchem Befehl werden Privilegien kontrolliert?

    - [ ] REVOKE ... ON ... FROM ;

    - [ ] SELECT user, host, password FROM user ;

    - [ ] SHOW TABLES;

    - [x] SHOW GRANTS FOR ... ;

5.  Welches sind die beiden wichtigsten DCL-Befehle (data control)?

    - [ ] SELECT

    - [x] REVOKE

    - [ ] DELETE

    - [x] GRANT

6.  Was ist nötig, dass Benutzer "meier" keinen Zugang mehr auf den DB-Server hat.

    - [ ] in Systemtabelle user für diesen Benutzer jedes Privileg auf "N" setzen

    - [x] mit DELETE FROM user WHERE user = 'meier'; und FLUSH PRIVILEGES;

    - [ ] in allen Systemtabellen für diesen Benutzer jedes Privileg auf "N" setzen

    - [ ] dem Benutzer das GRANT-Privileg (Grant_priv) wegnehmen

7.  Erklären Sie den Begriff "Autorisierung" im Zusammenhang mit einem DB-Server.

    Autorisierung ist der Prozess, bei dem einem authentifizierten Benutzer bestimmte Rechte oder Privilegien für den Zugriff auf Ressourcen oder die Ausführung von Aktionen im Datenbanksystem zugewiesen werden.
      

8.  Wann wird das Schlüsselwort IDENTIFIED BY verwendet?

    ``IDENTIFIED BY`` wird verwendet, um ein Passwort für einen Benutzer zu setzen oder zu ändern, typischerweise in GRANT- oder CREATE USER-Anweisungen.
      

9.  Ergänzen Sie den Befehl REVOKE ... ON ... FROM ... ; mit eigenen Angaben.
```sql
REVOKE SELECT, INSERT ON database_name.table_name FROM 'username'@'localhost';
```
      
10.  Mit welchem Befehl ändern Sie das Passwort von Benutzer Meier auf "abc123"?
```sql
ALTER USER 'Meier'@'localhost' IDENTIFIED BY 'abc123';
```

11. Geben Sie eine Erklärung für folgende Fehlermeldung.  
    
```sql
GRANT USAGE ON \*.\* TO abc IDENTIFIED BY 'a12';  
ERROR 1045: Access denied for user: '@127.0.0.1'
```
    
Der aktuelle Benutzer hat nicht die erforderlichen Rechte, um GRANT-Befehle auszuführen. 
      

12.  Korrigieren Sie den folgenden Befehl:  
    
```sql 
REVOKE ALL FROM ''@localhost;  
ERROR 1064: You have an error
```
```sql    
REVOKE ALL PRIVILEGES ON *.* FROM ''@'localhost';
```
