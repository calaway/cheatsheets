# PostgreSQL CheatSheet

## Install
```bash
# Install via Homebrew
brew install postgresql
# Have launchd start postgresql now and restart at login
brew services start postgresql
```

## Create a new database
```bash
createdb my-db
```

## psql
`psql` is the PostgreSQL interactive terminal.

```bash
# In bash
# List all databases
psql --list
# Connect to the database named "my-db"
psql my-db
```

```sql
-- In psql terminal
-- Main help menu
help
-- Help with psql commands
\?
-- Help with SQL commands
\h
-- Quit
\q

-- List all databases
\l
-- List all tables in current database
\d
\d+ -- More detail
-- Describe table (also works with view, sequence, or index)
\d table_name
\d+ table_name -- More detail
```

## SQL
```sql
-- View full table contents
TABLE table_name;
```
