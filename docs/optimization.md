# Optimization
1.  Welche Möglichkeiten können die Geschwindigkeit eines DB-Server verbessern?

    - [ ] Indexe möglichst vermeiden

    - [x] Serverparameter einstellen

    - [x] Transaktionen verwenden

    - [ ] Locks verwenden

2.  Wie werden Daten schneller in eine DB-Tabelle geladen?

    - [ ] durch Komprimieren der Daten vor der Übertragung

    - [x] durch Verwenden des Parameters --opt beim Erstellen des Backup-Skripts

    - [x] durch Importieren der Daten aus einer Textdatei

    - [ ] durch Verwenden von vielen INSERT-Befehlen

3.  Was trifft auf den Befehl OPTIMIZE TABLE zu?

    - [x] entfernt nicht genutzten Speicherplatz aus MyISAM-Tabellendateien

    - [ ] ist auf MyISAM- und InnoDB-Tabellen anwendbar

    - [ ] wird angewendet bei Tabellen, die häufig abgefragt werden

    - [x] defragmentiert DB-Dateien

4.  Wie finden Sie langsame DB-Abfragen?

    - [ ] mit EXPLAIN SELECT

    - [ ] im Query Log

    - [x] im Slow Query Log

    - [ ] im Error Log

5.  Welche Aussagen betreffend DB-Optimierung sind korrekt?

    - [ ] Abfragen, die LIKE enthalten, können immer optimiert werden

    - [x] Indexe beschleunigen Abfragen

    - [x] Indexe werden allgemein auf Schlüsselattribute gelegt

    - [ ] durch Indexe werden DB-Einträge und -änderungen schneller
    
6.  Wann verwenden Sie den Befehl EXPLAIN?

    - [ ] um Daten schneller in die DB zu laden

    - [x] immer im Zusammenhang mit SELECT

    - [ ] um langsame Abfragen zu finden

    - [x] um zu erkennen, wie sich ein Index auf die Geschwindigkeit einer Abfrage auswirkt

7.  Welches sind Gründe für die Verwendung eines Index?

    - [ ] um das Eintragen von Daten in Tabellen bei Unique-Attributen zu beschleunigen

    - [x] um DB-Abfragen zu beschleunigen

    - [ ] um das Ändern von Daten zu verlangsamen

    - [x] um einmalige Werte zu gewährleisten

8.  Was wird optimiert, um die Geschwindigkeit eines DB-Servers zu verbessern?

    - Datenbankstruktur (Normalisierung, Denormalisierung)
    - Indexe
    - SQL-Abfragen
    - Serverkonfiguration
    - Hardware (RAM, CPU, Festplatten)
      

9.  Mit welchen 2 prinzipiellen Massnahmen werden DB-Abfragen beschleunigt?

    - Optimierung der SQL-Abfragen
    - Verwendung von Indexen
      

10.  Beschreiben Sie kurz, wie Sie den Befehl EXPLAIN verwenden.

        EXPLAIN wird vor einem SELECT-Befehl verwendet, um den Ausführungsplan der Abfrage anzuzeigen. Beispiel: EXPLAIN SELECT * FROM users WHERE id = 1;
      

11.  Wozu wird der Befehl OPTIMIZE TABLE angewendet?

        OPTIMIZE TABLE wird verwendet, um den Speicherplatz zu defragmentieren und die Datenstrukturen von Tabellen zu optimieren, insbesondere nach vielen Einfüge-, Update- oder Löschvorgängen.
      

12.  Wie werden SELECT-Befehle optimiert?

        - Verwendung spezifischer Spalten statt *
        - Vermeidung von Wildcard-Suchen am Anfang von LIKE-Ausdrücken
        - Verwendung von JOINs statt Subqueries wo möglich
        - Hinzufügen relevanter Indexe
        - Verwendung von LIMIT für Ergebnisbegrenzung
      

13.  Wie viele DB-Tabellen können standardmässig gleichzeitig geöffnet sein?

        Dies variiert je nach MySQL-Version und Systemkonfiguration, typischerweise zwischen 64 und 1024. Der genaue Wert kann mit SHOW VARIABLES LIKE 'open_tables_cache'; überprüft werden.
      

14.  Wie schalten Sie den Query Cache ein bzw. aus?

        In neueren MySQL-Versionen (ab 8.0) wurde der Query Cache entfernt. In älteren Versionen:
Einschalten: SET GLOBAL query_cache_type = 1;
Ausschalten: SET GLOBAL query_cache_type = 0;
