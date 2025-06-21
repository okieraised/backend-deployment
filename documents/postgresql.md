## 🐘 Useful PostgreSQL Commands

### 🔹 Connection & Access

| Command | Description |
|--------|-------------|
| `psql -U <user> -d <db>` | Connect to a database with user |
| `psql -h <host> -p <port> -U <user> -d <db>` | Connect with host, port, user, and DB |
| `\q` | Quit `psql` CLI |
| `\l` or `\list` | List all databases |
| `\c <dbname>` | Connect to a different database |
| `\dt` | List tables in the current database |
| `\du` | List roles/users |
| `\dn` | List schemas |
| `\df` | List functions |
| `\d <table>` | Show schema of a table |

---

### 🔹 User and Role Management

| Command | Description |
|--------|-------------|
| `CREATE USER <name> WITH PASSWORD '<pass>';` | Create a new user |
| `ALTER USER <name> WITH SUPERUSER;` | Give superuser privileges |
| `GRANT <privileges> ON DATABASE <db> TO <user>;` | Grant privileges to user |
| `REVOKE <privileges> ON DATABASE <db> FROM <user>;` | Revoke privileges |
| `DROP USER <name>;` | Delete a user |

---

### 🔹 Database Management

| Command | Description |
|--------|-------------|
| `CREATE DATABASE <name>;` | Create a new database |
| `DROP DATABASE <name>;` | Delete a database |
| `ALTER DATABASE <name> RENAME TO <newname>;` | Rename a database |
| `\encoding` | Show current encoding |
| `SHOW server_encoding;` | Show DB encoding via SQL |

---

### 🔹 Table Operations

| Command | Description |
|--------|-------------|
| `CREATE TABLE <name> (...);` | Create a new table |
| `ALTER TABLE <name> ADD COLUMN ...;` | Add a column |
| `ALTER TABLE <name> DROP COLUMN ...;` | Drop a column |
| `DROP TABLE <name>;` | Delete a table |
| `TRUNCATE TABLE <name>;` | Delete all rows (fast) |

---

### 🔹 Data Querying

| Command | Description |
|--------|-------------|
| `SELECT * FROM <table>;` | Query all rows |
| `SELECT col1, col2 FROM <table> WHERE ...;` | Select specific columns |
| `INSERT INTO <table> (...) VALUES (...);` | Insert a row |
| `UPDATE <table> SET col = val WHERE ...;` | Update rows |
| `DELETE FROM <table> WHERE ...;` | Delete rows |
| `COPY <table> TO '/path/file.csv' CSV HEADER;` | Export data to CSV |
| `COPY <table> FROM '/path/file.csv' CSV HEADER;` | Import CSV into table |

---

### 🔹 Indexes and Constraints

| Command | Description |
|--------|-------------|
| `CREATE INDEX idx_name ON <table>(column);` | Add an index |
| `DROP INDEX idx_name;` | Remove an index |
| `ALTER TABLE <table> ADD CONSTRAINT ...;` | Add foreign key, unique, etc. |
| `\di` | List indexes |
| `\d <table>` | View indexes on table |

---

### 🔹 Backup and Restore

| Command | Description |
|--------|-------------|
| `pg_dump -U <user> -d <db> > dump.sql` | Dump database to SQL file |
| `pg_dump -Fc -U <user> <db> > dump.dump` | Custom binary format |
| `psql -U <user> -d <db> < dump.sql` | Restore from SQL file |
| `pg_restore -U <user> -d <db> dump.dump` | Restore from custom format |
| `pg_restore --list dump.dump` | List contents of a dump |

---

### 🔹 Performance & Debugging

| Command | Description |
|--------|-------------|
| `EXPLAIN <query>;` | Show query plan |
| `EXPLAIN ANALYZE <query>;` | Show actual run time |
| `VACUUM;` | Reclaim storage space |
| `VACUUM FULL;` | Reclaim more, but locks table |
| `ANALYZE;` | Update statistics |
| `\timing` | Toggle query timing |
| `SELECT now();` | Current timestamp |

---

### 🔹 Misc Tips

| Command | Description |
|--------|-------------|
| `\set AUTOCOMMIT off` | Toggle autocommit |
| `BEGIN; ... COMMIT;` | Use transactions |
| `SET search_path TO <schema>;` | Set default schema |
| `\x` | Expanded output (for wide results) |
| `\watch 5` | Re-run last query every 5 seconds |

---

### 🔹 SQL Examples
#### 1. 
```sql
-- Create table
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT UNIQUE,
  created_at TIMESTAMPTZ DEFAULT now()
);

-- Add foreign key
ALTER TABLE orders ADD CONSTRAINT fk_user FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE;
