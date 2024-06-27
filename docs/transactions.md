# Transactions
1.  Wie stellen Transaktionen bei einem DB-Server-Crash die Datenkonsistenz sicher?

    Transaktionen verwenden Logging-Mechanismen wie Write-Ahead Logging (WAL). Alle Änderungen werden zuerst in ein Log geschrieben, bevor sie in der Datenbank ausgeführt werden. Bei einem Crash kann der Server anhand des Logs unvollständige Transaktionen rückgängig machen und abgeschlossene Transaktionen wiederholen, um die Datenkonsistenz wiederherzustellen.
***Note: probably not needed knowledge in my opinion***

2. Mit welcher Locking-Art wartet ein SELECT-Befehl, bis alle Transaktionen auf die angeforderte Tabelle entsperrt sind? 

    Shared Lock (S-Lock) oder Read Lock
          
3. Wie muss Autocommit gesetzt werden, damit jeder SQL-Befehl zu einer Transaktion gehört und damit explizit mit COMMIT abgeschlossen werden muss, damit er ausgeführt wird? 
```sql
SET autocommit = 0;
```

4.  Welche Locking-Art ist a) bei MyISAM-Tabellen b) bei InnoDB-Tabellen möglich?

    a) MyISAM: Table-level locking
    b) InnoDB: Row-level locking und Table-level locking
5.  Beschreiben Sie den Begriff Datenbank-Transaktion

    Eine Datenbank-Transaktion ist eine Folge von Datenbankoperationen, die als eine logische Einheit behandelt werden. Sie wird entweder vollständig ausgeführt oder gar nicht, um die Datenintegrität zu gewährleisten.

6.  Beschreiben Sie die Bedeutung von I in der Abkürzung ACID.

    I steht für "Isolation". Es bedeutet, dass parallel laufende Transaktionen sich nicht gegenseitig beeinflussen und jede Transaktion so ausgeführt wird, als wäre sie die einzige im System.
