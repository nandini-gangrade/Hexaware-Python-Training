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

**1. Find all the Toy Story movies:**
```sql
SELECT * FROM Movies WHERE Title LIKE 'Toy Story%';
```
This command selects all movies with titles starting with "Toy Story".

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
