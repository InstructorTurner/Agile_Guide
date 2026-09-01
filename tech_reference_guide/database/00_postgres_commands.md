# 🐘 Postgres Commands Cheat Sheet

## 🚀 CLI Quick Reference (`psql`)

| Action | Command | Description |
| :--- | :--- | :--- |
| **Connect** | `psql -U <user> -d <db_name>` | Connect to a specific database |
| **List DBs** | `\l` | List all databases |
| **Connect DB** | `\c <db_name>` | Switch to another database |
| **List Tables** | `\dt` | List all tables in current DB |
| **Describe Table**| `\d <table_name>` | See columns, types, and indexes |
| **Quit** | `\q` | Exit psql |

## 🛠️ Basic SQL Operations

### Data Manipulation (DML)
```sql
-- Insert record
INSERT INTO users (username, email) VALUES ('dev1', 'dev1@example.com');

-- Update record
UPDATE users SET status = 'active' WHERE id = 5;

-- Delete record
DELETE FROM users WHERE id = 10;
```

### Data Definition (DDL)
```sql
-- Create Table
CREATE TABLE products (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  price NUMERIC(10, 2),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Add Column
ALTER TABLE products ADD COLUMN description TEXT;
```
