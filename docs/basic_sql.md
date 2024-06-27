# Basic SQL and Queries
1.  Mit welchem Befehl kontrollieren Sie die Struktur einer Tabelle?

    - [ ] SHOW DATABASES;

    - [x] SHOW CREATE TABLE *tabellenname*;

    - [x] DESC *tabellenname*; 
    
    - [x] DESCRIBE *tabellenname*;

    - [ ] SELECT * FROM *tabellenname*;

    - [ ] SHOW TABLE *tabellenname*;
2.  Wie bezeichnet man die Ausführung mehrerer DB-Operationen in einem einzigen Schritt?

    - [ ] Referentielle Integrität

    - [ ] Replikation

    - [x] Transaktion

    - [ ] Storage Procedure

3.  Mit welchen Befehlen werden Transaktionen gesteuert?

    - [ ] UNLOCK TABLES;

    - [x] COMMIT; oder ROLLBACK;

    - [ ] ALTER TABLE ... TYPE= ...;

    - [x] BEGIN; oder START TRANSACTION;

4.  Was trifft auf das Locking bei Transaktionen auf InnoDB-Tabellen zu?

    - [ ] in Transaktionen kommt Table locking zur Anwendung

    - [x] es wird Row locking angewendet

    - [ ] es werden alle Datensätze der entsprechenden Tabelle(n) gesperrt

    - [x] es werden nur die gerade bearbeiteten Datensätze gesperrt

5.  Notieren Sie den SQL-Befehl, der die InnoDB-Tabelle BESTELLUNGEN erstellt.

```sql
CREATE TABLE BESTELLUNGEN (
        id INT PRIMARY KEY,
        bestelldatum DATE,
        kunde_id INT,
        gesamtbetrag DECIMAL(10,2)
    ) ENGINE=InnoDB;
```
