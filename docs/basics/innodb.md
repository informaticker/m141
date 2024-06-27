# Basic Knowledge (InnoDB)
1.  Welches ist das Standard-Tabellenformat von MySQL (MariaDB)?

    - [x] InnoDB

    - [ ] MyISAM

    - [ ] ARIA

    - [ ] ISAM

2.  Wann verwenden Sie das InnoDB-Tabellenformat?

    - [ ] wenn möglichst schnell auf die Daten zugegriffen werden muss

    - [x] wenn auf gar keinen Fall ein Datenverlust vorkommen darf

    - [x] wenn viele Benutzer gleichzeitig Daten ändern

    - [ ] wenn bei sehr vielen Daten nicht beliebig viel Speicherplatz vorhanden ist

3.  Was trifft auf den sog. Tablespace zu?

    - [ ] Datei, welche die Daten der entsprechenden Tabelle enthält (\*.MYD)

    - [ ] Datei, welche Beschreibung, Daten und Indexe einer Tabelle enthält

    - [x] Datei, welche alle InnoDB-Tabellen enthält (virtueller Speicher)

    - [x] wird nach Erreichen von x MB automatisch vergrössert (falls autoextend eingeschaltet)

4.  Welches sind Vorteile der InnoDB-Tabellen gegenüber MyISAM-Tabellen?

    - Unterstützung für Transaktionen (ACID-Konformität)
    - Zeilensperrung (Row-level locking) für bessere Nebenläufigkeit
    - Referentielle Integrität durch Fremdschlüssel
    - Crash-Recovery und bessere Datenkonsistenz
