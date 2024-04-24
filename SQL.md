## SQL VS NO SQL

| Feature                      | SQL (Relational Database)                                      | NoSQL (Non-Relational Database)                        |
|------------------------------|----------------------------------------------------------------|---------------------------------------------------------|
| Data Model                   | Follows a structured data model with tables and relationships | Offers flexible schema design, including key-value, document, column-family, and graph databases |
| Schema                       | Requires a predefined schema                                    | Can have a dynamic or flexible schema                    |
| Query Language               | Uses SQL (Structured Query Language) for queries               | Doesn't necessarily use SQL, may have its query language or APIs |
| Scalability                  | Vertical scalability (scaling up)                               | Horizontal scalability (scaling out)                     |
| ACID Compliance              | ACID compliant (Atomicity, Consistency, Isolation, Durability) | May or may not be ACID compliant depending on the database |
| Transactions                 | Supports transactions                                           | May support transactions, but implementation varies       |
| Examples                     | MySQL, PostgreSQL, Oracle                                      | MongoDB, Cassandra, Redis, Couchbase                     |


#### Examples:

1. **SQL Example:**
   - Database: PostgreSQL
   - Schema: 
     - Table: `employees`
       - Columns: `id`, `name`, `department`, `salary`
   - Query: 
     ```sql
     SELECT * FROM employees WHERE department = 'IT';
     ```

2. **NoSQL Example:**
   - Database: MongoDB
   - Schema:
     - Collection: `employees`
       - Documents:
         ```json
         {
           "_id": ObjectId("60a825f83436eb054384b75e"),
           "name": "John Doe",
           "department": "IT",
           "salary": 75000
         }
         ```
   - Query:
     ```javascript
     db.employees.find({ department: 'IT' });
     ```

> These examples illustrate the differences in data modeling, schema, query language, and scalability between SQL and NoSQL databases.


# SQL

![WhatsApp Image 2024-04-24 at 12 31 33_1f65253f](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/fb1c4bd4-5bc3-4f72-bfbf-763c2bff7a57)
![WhatsApp Image 2024-04-24 at 12 31 34_026e8ced](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/945fab13-940f-4d15-b819-f110da3a2e62)

## Filter the Columns

![WhatsApp Image 2024-04-24 at 12 31 34_575710c6](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/6727dbf1-6dbc-4c59-9501-a367d5ba66c6)
![WhatsApp Image 2024-04-24 at 12 31 34_9794d172](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/840f6354-9d43-4bf9-98b5-fa2bfe2f7686)

### Exercise 1 

1. **Find the title of each film:**
   ```sql
   SELECT Title FROM Movies;
   ```
   This query retrieves the titles of all the films from the "Movies" table.

2. **Find the director of each film:**
   ```sql
   SELECT Director FROM Movies;
   ```
   This query fetches the directors of all the films from the "Movies" table.

3. **Find the title and director of each film:**
   ```sql
   SELECT Title, Director FROM Movies;
   ```
   This query retrieves both the title and director of each film from the "Movies" table.

4. **Find the title and year of each film:**
   ```sql
   SELECT Title, Year FROM Movies;
   ```
   This query fetches both the title and the year of release for each film from the "Movies" table.

5. **Find all the information about each film:**
   ```sql
   SELECT * FROM Movies;
   ```
   This query selects all columns (attributes) for each film in the "Movies" table, effectively fetching all available information about each film.

> These queries return columns from the "Movies" table that meet the specified criteria.

## Filter the Rows

![WhatsApp Image 2024-04-24 at 12 44 32_425ccc16](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/14694446-088a-4fce-a594-26834e960e9a)
![WhatsApp Image 2024-04-24 at 12 44 33_a4c96844](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/29c03576-6541-4bfa-be78-64074915bacd)
![WhatsApp Image 2024-04-24 at 12 45 52_e507cd36](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/13572ac7-e919-460e-8022-efbf62281e2f)

### Exercise 2

1. **Find the movie with a row id of 6:**
   ```sql
   SELECT * FROM Movies WHERE Id = 6;
   ```
   This query retrieves all columns for the movie with a row ID of 6 from the "Movies" table.

2. **Find the movies released in the years between 2000 and 2010:**
   ```sql
   SELECT * FROM Movies WHERE Year BETWEEN 2000 AND 2010;
   ```
   This query fetches all columns for movies released between the years 2000 and 2010 from the "Movies" table.

3. **Find the movies not released in the years between 2000 and 2010:**
   ```sql
   SELECT * FROM Movies WHERE Year NOT BETWEEN 2000 AND 2010;
   ```
   This query retrieves all columns for movies not released between the years 2000 and 2010 from the "Movies" table.

4. **Find the first 5 Pixar movies and their release year:**
   ```sql
   SELECT * FROM Movies WHERE Director = 'Pixar' LIMIT 5;
   ```
   This query selects all columns for the first 5 movies where the director's name contains 'Pixar' (case-insensitive) and also limits the result to 5 rows.

5. **Retrieve all movies released in the years 1999, 2007, and 2010.**
   ```sql
    SELECT * FROM Movies WHERE Year IN (1999, 2007, 2010);
   ```

6. **Retrieve all movies except those released in the years 1999, 2007, and 2010.**
   ```sql
    SELECT * FROM Movies WHERE Year NOT IN (1999, 2007, 2010);
   ```
   These (5th n 6th) queries provide a way to filter movies based on whether their release year is within or outside the specified set of years.

> These queries return rows from the "Movies" table that meet the specified criteria.

## Text Comparison Operators
![WhatsApp Image 2024-04-24 at 13 05 32_d9f7ae18](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/f9ed886d-630f-4ada-bd5a-4b51b373198c)
![WhatsApp Image 2024-04-24 at 14 13 57_3b93bc1e](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/86867eb5-75c4-4d55-a295-e4abdadf74f8)

### Exercise 4

**1. Find all the Toy Story movies:**
```sql
SELECT * FROM Movies WHERE Title LIKE 'Toy Story%';
```
This command selects all movies with titles starting with "Toy Story".

```sql
SELECT * FROM Movies WHERE Title LIKE 'Toy Story_';
```
This command selects all movies with titles exactly matching "Toy Story" followed by one additional character.

```sql
SELECT * FROM Movies WHERE Title LIKE '%Toy Story%';
```
This command selects all movies with "Toy Story" appearing anywhere in the title.

**2. Find all the movies directed by John Lasseter:**
```sql
SELECT * FROM Movies WHERE Director = 'John Lasseter';
```
This command selects all movies directed by "John Lasseter".

**3. Find all the movies (and director) not directed by John Lasseter:**
```sql
SELECT * FROM Movies WHERE Director != 'John Lasseter';
```
This command selects all movies not directed by "John Lasseter".

**4. Find all the WALL movies:**
```sql
SELECT * FROM Movies WHERE Title LIKE '%WALL%';
```
This command selects all movies with "WALL" in their title.

> These SQL operators and wildcards are commonly used for pattern matching and comparison in queries to filter rows based on specific conditions or patterns.

## Refining Results with Filtering and Sorting

![WhatsApp Image 2024-04-24 at 14 31 00_500ca04b](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/c6855890-22c2-4ea9-951c-592c432d5af4)
![WhatsApp Image 2024-04-24 at 14 31 00_fdae9189](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/e00a977c-c8b8-4f89-a486-27ce0261bda6)
![WhatsApp Image 2024-04-24 at 14 31 00_a577c040](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/0faf7a3a-f5f0-4ef7-b984-4b7bc3813585)

### Exercise 4

**1. List all directors of Pixar movies (alphabetically), without duplicates**
```sql
SELECT DISTINCT Director FROM Movies WHERE Director LIKE '%Pixar%' ORDER BY Director;
```
This command selects all unique directors from the Movies table whose names contain "Pixar" and orders them alphabetically without duplicates.

**2. List the last four Pixar movies released (ordered from most recent to least)**
```sql
SELECT * FROM Movies WHERE Director LIKE '%Pixar%' ORDER BY Id DESC LIMIT 4;
```
This command selects the last four movies from the Movies table whose directors contain "Pixar" and orders them by their Id in descending order, representing the most recent releases.

**3. List the first five Pixar movies sorted alphabetically**
```sql
SELECT * FROM Movies WHERE Director LIKE '%Pixar%' ORDER BY Title ASC LIMIT 5;
```
This command selects the first five movies from the Movies table whose directors contain "Pixar" and orders them alphabetically by their title in ascending order.

**4. List the next five Pixar movies sorted alphabetically**
```sql
SELECT * FROM Movies WHERE Director LIKE '%Pixar%' ORDER BY Title ASC LIMIT 5 OFFSET 5;
```
This command selects the next five movies from the Movies table whose directors contain "Pixar" and orders them alphabetically by their title in ascending order, starting from the sixth row.

> These SQL commands provide various queries to retrieve information about Pixar movies, sorted and limited in different ways to meet specific requirements. Utilizing SQL commands like ORDER BY, LIMIT, and DISTINCT to narrow down and organize data according to specific criteria, ensuring clarity and relevance in the result set.

## Geographic Data Analysis: SQL Queries

![WhatsApp Image 2024-04-24 at 14 47 41_d3f62ca4](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/c3f639ea-5c99-4ce4-8c76-07fb65c4c053)
![WhatsApp Image 2024-04-24 at 14 49 29_8eb55b4c](https://github.com/nandini-gangrade/Hexaware-Python-Training/assets/87817417/f0a74157-5d06-405a-a4d2-9573bd55b24f)

### Exercise 5

**1. List all the Canadian cities and their populations:**
```sql
SELECT City, Population FROM North_American_Cities WHERE Country = 'Canada';
```
This command retrieves cities and their populations from the North American Cities table specifically for Canada. It helps understand the distribution of population within Canada.

**2. Order all the cities in the United States by the latitude from north to south:**
```sql
SELECT City, Latitude FROM North_American_Cities WHERE Country = 'United States' ORDER BY Latitude DESC;
```
By ordering cities based on latitude in descending order, this query sorts them from north to south. This arrangement aligns with the fact that latitude increases towards the North Pole, providing insights into the geographical layout of cities in the United States.

**3. List all the cities west of Chicago, ordered from west to east:**
```sql
SELECT City FROM North_American_Cities WHERE Longitude < (SELECT Longitude FROM North_American_Cities WHERE City = 'Chicago') ORDER BY Longitude ASC;
```
This command retrieves cities located west of Chicago and orders them from west to east based on longitude. It aligns with the principle that as longitude increases towards the east, cities are arranged from west to east.

**4. List the two largest cities in Mexico by population:**
```sql
SELECT City, Population FROM North_American_Cities WHERE Country = 'Mexico' ORDER BY Population DESC LIMIT 2;
```
By ordering cities in Mexico by population in descending order and limiting the result to the top two, this query identifies the two largest cities in Mexico. It provides insights into the demographic distribution and urbanization within the country.

**5. List the third and fourth largest cities by population in the United States:**
```sql
SELECT City, Population FROM North_American_Cities WHERE Country = 'United States' ORDER BY Population DESC LIMIT 2 OFFSET 2;
```
This command retrieves the third and fourth largest cities in the United States by population. By skipping the first two results and then limiting to the next two, it provides insights into the population hierarchy and urbanization trends within the country.

> Explore how the relationship between longitude and latitude impacts geographic positioning: longitude increases towards the east, while latitude increases towards the north.

----------------------------------------------------------

# Normalization in Databases

## What is Normalization?
Normalization is a process used in database design to organize data efficiently, reduce redundancy, and ensure data integrity. It involves breaking down a large table into smaller, more manageable tables and establishing relationships between them. Normalization helps in eliminating data anomalies and ensures that the database structure adheres to certain rules.

## Why Normalization?
Normalization is essential for several reasons:
- Reduces data redundancy
- Minimizes update anomalies
- Improves data integrity
- Enhances database performance
- Facilitates easier database maintenance and management

### Keywords:

- **Primary Key**: A unique identifier for each record in a table.
  - Example: Student_ID in a table of students.
  
- **Composite Primary Key**: A primary key that consists of more than one attribute.
  - Example: {Order_ID, Product_ID} in a table of orders and products.

- **Foreign Key**: A column in one table that references the primary key in another table.
  - Example: Department_ID in a table of employees, referencing the Department_ID in a table of departments.

- **Functional Dependency**: When knowing the value of one attribute determines the value of another attribute.
  - Example: Knowing the Social Security Number (SSN) of a person determines their Name.

- **Transitive Dependency**: When one non-key attribute determines another non-key attribute indirectly through a third attribute.
  - Example: In a table where City determines State, and State determines Country, City → State → Country is a transitive dependency.

- **Indirect Dependency**: Similar to transitive dependency, it refers to a situation where one attribute depends on another, which, in turn, depends on a third attribute.
  - Example: If a customer's Address depends on the Location, and the Location depends on the ZIP code, then Address → Location → ZIP code is an indirect dependency.

- **Candidate Key**: A minimal set of attributes that uniquely identify each tuple in a relation.
  - Example: {Student_ID} or {Email} can be candidate keys in a table of students.

- **Atomic Value**: A value that cannot be divided further.
  - Example: A cell in a table containing a single value like "John Smith" or "123 Main Street".

- **Partial Dependency**: When non-key attributes are dependent on only part of the primary key.
  - Example: In a table where {Student_ID, Course} → Grade, if Grade depends only on Course, it's a partial dependency.

- **Normalization**: The process of organizing data in a database to reduce redundancy and improve data integrity. (safety)
  - Example: Splitting a single table with customer information into separate tables for customers and their orders to avoid duplicating customer data.

- **Denormalization**: The process of intentionally adding redundancy to a database for performance reasons.
  - Example: Storing calculated values, like total order amount, in a table to avoid having to calculate them each time they're needed.

- **Anomaly**: An error or inconsistency in the data that occurs due to improper database design.
  - Example: Insertion, update, or deletion anomalies that arise when a database table is not properly normalized.

- **Dependency**: A relationship between attributes in a database, where the value of one attribute determines the value of another.
  - Example: The value of a Customer_ID attribute determines the corresponding customer's Name and Address.

## Normalization Forms
### 1. First Normal Form (1NF)
- **What**: Ensures that each column in the table contains atomic (indivisible) values.
- **Why**: Avoids repeating groups and ensures data integrity.
- **How**: Splitting multi-valued attributes into separate columns or rows.

      - Don't use row order to convey info.
      - Keep data types consistent.
      - Every row needs a unique identifier (Primary Key).
      - Don't repeat groups of data.

**Example**:

**Incorrect Table (1NF)**:

| Band_Name   | Members              |
|-------------|----------------------|
| Beatles     | Paul, John, George, Ringo |

**Incorrect Table Explanation**: In the incorrect table, the "Members" column violates 1NF by storing multiple member names in a single cell.

**Correct Table (1NF)**:

| Band_Name   | Member       |
|-------------|--------------|
| Beatles     | Paul         |
| Beatles     | John         |
| Beatles     | George       |
| Beatles     | Ringo        |

**Correct Table Explanation (1NF)**: The corrected table splits the multi-valued attribute "Members" into separate rows, ensuring atomic values in each cell.

### 2. Second Normal Form (2NF)
- **What**: Ensures that all non-key attributes are fully functionally dependent on the primary key.
- **Why**: Eliminates partial dependencies and improves data integrity.
- **How**: Splitting tables to remove partial dependencies.

      - Follow 1NF.
      - Have a special key made from more than one part (Composite Primary Key).
      - Everything else should depend fully on that key.

**Example**:

**Incorrect Table (2NF)**:

| Band_Name   | Member       | Role           |
|-------------|--------------|----------------|
| Beatles     | Paul         | Lead Singer    |
| Beatles     | John         | Guitarist      |
| Beatles     | George       | Guitarist      |
| Beatles     | Ringo        | Drummer        |

**Incorrect Table Explanation**: In the incorrect table, the "Role" attribute depends on the "Band_Name," which is part of the composite primary key, creating partial dependencies.

**Correct Tables (2NF)**:

| Band_Name   | Member       |
|-------------|--------------|
| Beatles     | Paul         |
| Beatles     | John         |
| Beatles     | George       |
| Beatles     | Ringo        |

| Member       | Role           |
|--------------|----------------|
| Paul         | Lead Singer    |
| John         | Guitarist      |
| George       | Guitarist      |
| Ringo        | Drummer        |

**Correct Tables Explanation (2NF)**: We split the original table into two separate tables to remove partial dependencies. Each table now has a single primary key, and all non-key attributes are fully functionally dependent on it.

### 3. Third Normal Form (3NF)
- **What**: Ensures that there are no transitive dependencies between non-key attributes.
- **Why**: Removes transitive dependencies and improves data integrity.
- **How**: Further splitting tables to eliminate transitive dependencies.

      - Meet 2NF.
      - No indirect dependencies between non-key items.

**Example**:

**Incorrect Table (3NF)**:

| Member       | Role           | Band_Name   |
|--------------|----------------|-------------|
| Paul         | Lead Singer    | Beatles     |
| John         | Guitarist      | Beatles     |
| George       | Guitarist      | Beatles     |
| Ringo        | Drummer        | Beatles     |

**Incorrect Table Explanation**: In the incorrect table, "Band_Name" depends on "Member," which is not a primary key, creating a transitive dependency.

**Correct Tables (3NF)**:

| Member_ID | Member       | Band_ID |
|-----------|--------------|---------|
| 1         | Paul         | 1       |
| 2         | John         | 1       |
| 3         | George       | 1       |
| 4         | Ringo        | 1       |

| Band_ID | Band_Name   |
|---------|-------------|
| 1       | Beatles     |

| Role_ID | Role         |
|---------|--------------|
| 1       | Lead Singer  |
| 2       | Guitarist    |
| 3       | Drummer      |

**Correct Tables Explanation (3NF)**: We further normalize the data by splitting attributes into multiple tables to remove transitive dependencies. Each table represents a distinct entity, and there are no transitive dependencies between non-key attributes.

### 4. Boyce-Codd Normal Form (BCNF)
- **What**: Ensures that every determinant is a candidate key.
- **Why**: Eliminates non-trivial functional dependencies.
- **How**: Decomposing tables until each satisfies the criteria for BCNF.

      - Satisfy 3NF.
      - Every reason (determinant) for something must be a potential Primary Key (Candidate Key).

**Example**:

**Incorrect Table (BCNF)**:

| Member       | Role           |
|--------------|----------------|
| Paul         | Lead Singer    |
| John         | Guitarist      |
| George       | Guitarist      |
| Ringo        | Drummer        |

**Incorrect Table Explanation**: In the incorrect table, both "Member" and "Role" are candidate keys, but they determine each other, creating non-trivial functional dependencies.

**Correct Tables (BCNF)**:

| Member_ID | Member       | Role_ID |
|-----------|--------------|---------|
| 1         | Paul         | 1       |
| 2         | John         | 2       |
| 3         | George       | 2       |
| 4         | Ringo        | 3       |

| Role_ID | Role         |
|---------|--------------|
| 1       | Lead Singer  |
| 2       | Guitarist    |
| 3       | Drummer      |

**Correct Tables Explanation (BCNF)**: We introduce surrogate keys ("Member_ID" and "Role_ID") to ensure each table has a single candidate key. Now, each determinant uniquely identifies the attributes, adhering to BCNF.

This explanation provides an overview of each normalization form, including examples of incorrect and correct tables for each, along with explanations of what was wrong and how it was corrected.
