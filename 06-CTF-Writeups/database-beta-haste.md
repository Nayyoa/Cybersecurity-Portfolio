
# Database Beta Haste — SQLite Forensics

## Challenge Overview

**Competition:** Bits n Bytes CTF 2026
**Platform:** MetaCTF
**Category:** Miscellaneous
**Points:** 225/225
**Status:** Solved

## Scenario

A developer created a SQLite database
to store internal company notes but
lost the application code needed to
read its contents.

The objective was to recover the
stored information directly from
the SQLite database file.

## Investigation Methodology

### 1. Identify the Database Format

The provided artifact was an SQLite
database file.

SQLite is a lightweight relational
database engine that stores its
data in a local file.

### 2. Examine Database Structure

The investigation involved identifying
the database structure and examining
the available records.

An SQLite investigation can use the
following commands:

```sql
SELECT name
FROM sqlite_master
WHERE type = 'table';
```

This query lists the tables stored
in the database.

### 3. Inspect Stored Records

Once the relevant table is identified,
its records can be examined using SQL.

Example:

```sql
SELECT * FROM table_name;
```

The table name must be replaced with
the actual name found in the database.

These queries illustrate the
investigation technique; the exact
commands used during the competition
have not been preserved.

### 4. Result

The challenge was successfully solved,
earning 225 points.

## Security Lessons

- SQLite files can be examined
  without the original application.
- Database structures can reveal
  how information is organized.
- Direct database access may expose
  sensitive information.
- SQL is useful in digital forensics.

## Skills Demonstrated

- SQLite database investigation
- SQL querying
- Data extraction
- Digital forensics
- Structured data analysis
