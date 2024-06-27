# M141 TLDR 
###### you should still read the docs :( 

## Encoding
- Encoding is an agreement between user and system, not automatically detected
- UTF-8 (see [glossar](glossar.md)) recommended for MySQL 5.5.3+ (use `utf8mb4`)
- Unicode Transformation Format (UTF) has variable bit lengths
- Byte Order Mark (BOM) differs for UTF-8 and UTF-16
- Collation affects sorting: '_ci' (case-insensitive), '_cs' (case-sensitive)
- Binary collation sorts based on character codes

## Basic SQL and Queries
- Check table structure: `SHOW CREATE TABLE tablename;`, `DESC tablename;`, `DESCRIBE tablename;`
- Transactions: `BEGIN;` or `START TRANSACTION;`, `COMMIT;`, `ROLLBACK;`
- InnoDB uses row-level locking, improving concurrency
- Create InnoDB table:
  ```sql
  CREATE TABLE tablename (
    id INT PRIMARY KEY,
    column2 datatype,
    ...
  ) ENGINE=InnoDB;
  ```

## Authentication & Privileges
- `GRANT` gives privileges, `REVOKE` removes them
- `FLUSH PRIVILEGES;` after privilege changes
- `SHOW GRANTS FOR username;` to check privileges
- Delete user: `DELETE FROM user WHERE user = 'username';` then `FLUSH PRIVILEGES;`
- Change password: `ALTER USER 'username'@'localhost' IDENTIFIED BY 'newpassword';`
- Authentication: Who are you? | Authorization: What can you do?

## InnoDB
- Default table format for MySQL/MariaDB
- Features: ACID-compliant transactions (see [glossar](glossar.md)), row-level locking, foreign keys
- Uses tablespace for data storage
- Better crash recovery and data consistency than MyISAM

## MyISAM
- Stores tables in three files:
  - `.frm`: Table structure
  - `.MYD`: Data
  - `.MYI`: Indexes
- Faster for read-heavy operations, but lacks transaction support

## MySQL Client
- Connect: `mysql -h hostname -u username -p`
- Backup: `mysqldump -h hostname dbname > backup.sql`
- Restore: `mysql -h hostname dbname < backup.sql`
- Execute script: `mysql -h hostname dbname < script.sql`
- Test connection: `mysqladmin -h hostname -u username -p ping`

## Transactions
- Ensure data consistency, follow ACID principles:
  - Atomicity: All or nothing
  - Consistency: Valid state to valid state
  - Isolation: Transactions don't interfere
  - Durability: Committed changes are permanent
- `SET autocommit = 0;` to control transaction boundaries manually
- Use `START TRANSACTION;` ... `COMMIT;` or `ROLLBACK;`

## Configuration
- Set via command line, config file (my.cnf or my.ini), or runtime
- Server parameters in config file start with `[mysqld]`
- Important parameters:
  - `datadir`: Where data is stored
  - `log-bin`: Enable binary logging
  - `max_connections`: Maximum simultaneous connections

## Logging
- General Query Log: All queries (can be resource-intensive)
- Slow Query Log: Queries exceeding `long_query_time`
- Error Log: Startup, shutdown, and error messages
- Binary Log: All data-changing queries, used for replication and point-in-time recovery
- Use `mysqlbinlog` tool for binary log analysis
- Enable general logging: `log = 1` in config or `SET GLOBAL general_log = 'ON';`

## Optimization
- Use appropriate indexes on frequently queried columns
- Optimize queries:
  - Avoid `SELECT *`, use specific columns
  - Use `EXPLAIN` to analyze query execution plans
  - Avoid wildcards at the start of `LIKE` patterns
  - Use `LIMIT` for large result sets
- Server optimization:
  - Adjust `key_buffer_size`, `innodb_buffer_pool_size`, etc.
  - Use `query_cache_type` and `query_cache_size` (pre-MySQL 8.0)
- Table optimization:
  - `OPTIMIZE TABLE` for defragmentation (especially after many DELETEs)
- Monitor slow queries:
  - Enable slow query log
  - Analyze with tools like mysqldumpslow

## Additional Important Points
- ODBC (Open Database Connectivity) driver enables application-to-database communication
- Locking types: Table-level (MyISAM) vs Row-level (InnoDB)
- Shared (read) locks vs Exclusive (write) locks
- Use `LOAD DATA INFILE` for faster data loading
- Regularly backup your database
- Keep MySQL and its components updated for security and performance

