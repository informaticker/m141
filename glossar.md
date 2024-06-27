# Glossar

## A

**Authentifizierung**
: Der Prozess der Identitätsprüfung eines Benutzers beim Zugriff auf den Datenbankserver. Es beantwortet die Frage "Wer?" und stellt sicher, dass nur berechtigte Benutzer Zugang erhalten.

**Autorisierung**
: Der Vorgang, bei dem einem authentifizierten Benutzer spezifische Rechte oder Privilegien für den Zugriff auf Ressourcen oder die Ausführung von Aktionen im Datenbanksystem zugewiesen werden.

**ACID**
: Ein Akronym für die vier Haupteigenschaften von Datenbanktransaktionen: Atomicity (Atomarität), Consistency (Konsistenz), Isolation (Isolation) und Durability (Dauerhaftigkeit). Das "I" steht für Isolation und bedeutet, dass parallel laufende Transaktionen sich nicht gegenseitig beeinflussen.

## B

**Byte Order Mark (BOM)**
: Eine spezielle Zeichenfolge am Anfang einer Textdatei, die die Byte-Reihenfolge und Codierung der Datei angibt. UTF-8 und UTF-16 verwenden unterschiedliche BOMs.

**Binärsortierung**
: Eine Sortiermethode, bei der Zeichen anhand ihres binären Codes verglichen und sortiert werden.

## C

**Codierung**
: Eine Vereinbarung zwischen dem Nutzer und dem System, die festlegt, welche binäre Bitkombination zu welchem Zeichen gehört. Sie ist entscheidend für die korrekte Darstellung und Verarbeitung von Textdaten.

**COMMIT**
: Ein SQL-Befehl, der eine Transaktion abschließt und alle Änderungen dauerhaft in der Datenbank speichert.

## D

**DCL (Data Control Language)**
: Ein Teil der SQL-Sprache, der für die Verwaltung von Benutzerrechten und -privilegien zuständig ist. Die wichtigsten DCL-Befehle sind GRANT und REVOKE.

## E

**EXPLAIN**
: Ein SQL-Befehl, der in Verbindung mit SELECT verwendet wird, um den Ausführungsplan einer Abfrage anzuzeigen und zu analysieren, wie Indexe die Geschwindigkeit beeinflussen.

## F

**FLUSH PRIVILEGES**
: Ein Befehl, der MySQL anweist, die Privilegien-Tabellen neu zu laden, damit Änderungen im Zugriffssystem sofort wirksam werden.

## G

**GRANT**
: Ein SQL-Befehl zum Erteilen von Privilegien an Benutzer. Er kann auch verwendet werden, um neue Benutzer zu erstellen, falls diese noch nicht existieren.

## I

**IDENTIFIED BY**
: Eine Klausel in SQL-Befehlen, die verwendet wird, um ein Passwort für einen Benutzer zu setzen oder zu ändern, typischerweise in GRANT- oder CREATE USER-Anweisungen.

**InnoDB**
: Das Standard-Tabellenformat von MySQL, das Transaktionen, Zeilensperrung und Fremdschlüssel unterstützt. Es bietet bessere Datenkonsistenz und Crash-Recovery als MyISAM.

**Index**
: Eine Datenstruktur, die verwendet wird, um die Geschwindigkeit von Datenbankabfragen zu erhöhen. Indexe werden typischerweise auf Schlüsselattribute gelegt und können einmalige Werte gewährleisten.

## K

**Kollation**
: Eine Reihe von Regeln, die bestimmen, wie Zeichenfolgen verglichen und sortiert werden. Sie berücksichtigt Aspekte wie Groß-/Kleinschreibung und sprachspezifische Sortierregeln.

## L

**Locking**
: Ein Mechanismus zur Kontrolle des gleichzeitigen Zugriffs auf Daten. InnoDB unterstützt Zeilensperrung (Row-level locking) für bessere Nebenläufigkeit, während MyISAM nur Tabellensperrung (Table-level locking) bietet.

## M

**MyISAM**
: Ein älteres Tabellenformat in MySQL, das keine Transaktionen oder Fremdschlüssel unterstützt, aber für bestimmte Anwendungsfälle wie schnelle Lesezugriffe nützlich sein kann.

**mysql**
: Der Kommandozeilen-Client für MySQL, der verwendet wird, um eine Verbindung zum MySQL-Server herzustellen und SQL-Befehle auszuführen.

**mysqldump**
: Ein Befehlszeilen-Dienstprogramm, das verwendet wird, um Backups von MySQL-Datenbanken zu erstellen.

## O

**ODBC-Driver**
: Ein Treiber, der den Zugriff einer Anwendung auf eine bestimmte Datenbank ermöglicht, indem er eine standardisierte Schnittstelle zwischen der Anwendung und der Datenbank bereitstellt.

**OPTIMIZE TABLE**
: Ein SQL-Befehl, der verwendet wird, um den Speicherplatz zu defragmentieren und die Datenstrukturen von Tabellen zu optimieren, insbesondere nach vielen Einfüge-, Update- oder Löschvorgängen.

## Q

**Query Cache**
: Ein Feature in älteren MySQL-Versionen, das die Ergebnisse von SELECT-Abfragen zwischenspeichert, um die Leistung zu verbessern. In neueren Versionen (ab 8.0) wurde es entfernt.

## R

**REVOKE**
: Ein SQL-Befehl zum Entziehen von Privilegien von Benutzern.

**ROLLBACK**
: Ein SQL-Befehl, der eine Transaktion abbricht und alle Änderungen rückgängig macht, die seit dem Beginn der Transaktion vorgenommen wurden.

## S

**Shared Lock (S-Lock)**
: Auch bekannt als Read Lock, ermöglicht es mehreren Transaktionen, gleichzeitig auf Daten zuzugreifen, solange keine Änderungen vorgenommen werden.

**Slow Query Log**
: Eine Protokolldatei, die SQL-Anweisungen aufzeichnet, die länger als ein festgelegter Schwellenwert zur Ausführung benötigen. Es ist ein nützliches Werkzeug zur Leistungsoptimierung.

## T

**Tablespace**
: Eine logische Speicherstruktur in InnoDB, die als virtueller Speicher für alle InnoDB-Tabellen dient. Er kann automatisch vergrößert werden, wenn die Option "autoextend" aktiviert ist.

**Transaktion**
: Eine Folge von Datenbankoperationen, die als eine logische Einheit behandelt werden. Transaktionen gewährleisten die Datenkonsistenz, indem sie entweder vollständig ausgeführt oder vollständig rückgängig gemacht werden.

## U

**UTF (Unicode Transformation Format)**
: Eine Zeichenkodierung, die den gesamten Unicode-Zeichensatz abdecken kann. UTF-8 ist die empfohlene Kodierung für MySQL seit Version 5.5.3.

**USAGE**
: Ein spezielles Privileg in MySQL, das keine tatsächlichen Rechte gewährt, aber verwendet wird, um einen Benutzer zu erstellen oder sein Passwort zu ändern, ohne ihm spezifische Rechte zu geben.

## V

**Verbindungstest**
: Eine Methode zur Überprüfung, ob eine Verbindung zum MySQL-Server hergestellt werden kann. Dies kann mit Befehlen wie `ping` für die Netzwerkverbindung oder `mysqladmin ping` für den MySQL-Dienst durchgeführt werden.

## W

**Write-Ahead Logging (WAL)**
: Ein Protokollierungsmechanismus, bei dem Änderungen zuerst in ein Log geschrieben werden, bevor sie in der Datenbank ausgeführt werden. Dies ermöglicht die Wiederherstellung der Datenkonsistenz nach einem Systemabsturz.

## Z

**Zeilensperrung (Row-level locking)**
: Eine Sperrmethode in InnoDB, bei der nur die gerade bearbeiteten Datensätze gesperrt werden, was eine bessere Nebenläufigkeit ermöglicht als die Tabellensperrung.