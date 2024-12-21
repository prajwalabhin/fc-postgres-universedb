```markdown
# Universe Database

This project is part of the FreeCodeCamp PostgreSQL project. It involves creating a database with tables for galaxies, stars, planets, and moons.

## Getting Started

Follow these steps to set up and run the database:

### 1. Clone the Repository
Clone this repository to your local machine:
```bash
git clone https://github.com/prajwalabhin/fc-postgres-universedb.git
```

### 2. Restore the Database
Navigate to the project directory and restore the database using the `universe.sql` file:
```bash
psql -U postgres < universe.sql
```

### 3. Connect to the Database
Connect to the `universe` database using the `psql` command-line tool:
```bash
psql --username=freecodecamp --dbname=universe
```

## Features

- **Tables**: 
  - `galaxy`
  - `star`
  - `planet`
  - `moon`

- **Key Attributes**:
  - Foreign key relationships between tables.
  - Unique constraints for specific columns.
  - Variety of data types (`VARCHAR`, `INT`, `NUMERIC`, `TEXT`, `BOOLEAN`).

## Example SQL Queries

Here are some example queries you can run to interact with the database:

### Fetch all galaxies:
```sql
SELECT * FROM galaxy;
```

### Count planets in each star system:
```sql
SELECT star_id, COUNT(*) AS planet_count FROM planet GROUP BY star_id;
```

### Find moons orbiting a specific planet:
```sql
SELECT * FROM moon WHERE planet_id = 1;
```

## Additional Notes
If you make changes to the database and want to back it up, use the following command:
```bash
pg_dump -cC --inserts -U freecodecamp universe > universe.sql
```

You can restore the database using:
```bash
psql -U postgres < universe.sql
```

Enjoy exploring the universe database!
```
