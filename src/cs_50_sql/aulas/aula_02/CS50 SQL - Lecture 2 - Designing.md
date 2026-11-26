# CS50 SQL - Lecture 2 - Designing

TABLE OF CONTENTS

- 00:00:00 - Introduction
- 00:00:17 - Designing
- 00:06:48 - MBTA
- 00:14:04 - Normalization
- 00:20:24 - CREATE TABLE
- 00:27:25 - Data Types and Storage Classes
- 00:45:27 - Table Constraints
- 00:53:34 - Column Constraints
- 01:00:45 - Altering Tables
- 01:20:01 - Charlie

## Commands

- .schema
- .quit
- .read


## Normalization

- When normalizing, we put each entity in its own table—as we did with riders and subway stations. Any information about a specific entity, for example a rider’s address, goes into the entity’s own table.

## Relating

 ```mermaid
---
title: ER Diagram
---
erDiagram
    Rider }o--|{ Station : visits
```

## CREATE TABLE

> MBTA - Massachussetts Bay Transportation Authority

## Data Types and Storage Classes

- SQLite has five storage classes:
    - Null: nothing, or empty value
    - Integer: numbers without decimal points
    - Real: decimal or floating point numbers
    - Text: characters or strings
    - Blob: Binary Large Object, for storing objects in binary (useful for images, audio etc.)

## Type Affinities

- It is possible to specify the data type of a column while creating a table.
- However, columns in SQLite don’t always store one particular data type. They are said to have type affinities, meaning that they try to convert an input value into the type they have an affinity for.
- The five type affinities in SQLite are: Text, Numeric (either integer or real values based on what the input value best converts to), Integer, Real and Blob.
- Consider a column with a type affinity for Integers. If we try to insert “25” (the number 25 but stored as text) into this column, it will be converted into an integer data type.
- Similarly, inserting an integer 25 into a column with a type affinity for text will convert the number to its text equivalent, “25”.

## Table Constraints

- We can use table constraints to impose restrictions on certain values in our tables.
- For example, a primary key column must have unique values. The table constraint we use for this is PRIMARY KEY.
- Similarly, a constraint on a foreign key value is that it must be found in the primary key column of the related table! This table constraint is called, predictably, FOREIGN KEY.

## Column Constraints

- A column constraint is a type of constraint that applies to a specified column in the table.
- SQLite has four column constraints:
    - CHECK: allows checking for a condition, like all values in the column must be greater than 0
    - DEFAULT: uses a default value if none is supplied for a row
    - NOT NULL: dictates that a null or empty value cannot be inserted into the column
    - UNIQUE: dictates that every value in this column must be unique

## Altering Tables

- Consider the following updated ER diagram, where the entity “Rider” has been swapped out with a new entity “Card” used to represent CharlieCards. CharlieCards, in the Boston Subway, can be loaded with money and are used to swipe into and sometimes out of stations.

 ```mermaid
---
title: ER Diagram
---
erDiagram
    Card ||--o{ Swipe : makes
    Swipe }o--|| Station : at

    Card {
        id INTEGER
    }
    Swipe {
        id INTEGER
        type TEXT
        datetime NUMERIC
        amount NUMERIC
    }
    Station {
        id INTEGER
        name TEXT
        line TEXT
    }
```

- Notice that a card can be swiped many times in total, but only at one station at a given time.
- The “Card” entity has an ID, which is also its primary key.
- There is also now an entity “Swipe”, with an ID of its own and a type. “Swipe” also records the time at which a card was swiped and the amount that was subtracted (equivalent to the amount of money needed to ride the subway)!