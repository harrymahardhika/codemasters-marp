**Exercise 1: Create Tables**

Create two tables, "authors" and "books," with appropriate columns for each. Ensure that the "authors" table has a primary key, and the "books" table has a foreign key relationship with the "authors" table.

**Solution 1: Create Tables**

```sql
-- Create the "authors" table
CREATE TABLE authors (
    author_id INT PRIMARY KEY,
    author_name VARCHAR(100) NOT NULL
);

-- Create the "books" table with a foreign key relationship
CREATE TABLE books (
    book_id INT PRIMARY KEY,
    book_title VARCHAR(200) NOT NULL,
    author_id INT,
    FOREIGN KEY (author_id) REFERENCES authors(author_id)
);
```

**Exercise 2: Insert Data**

Insert at least three records into the "authors" table and five records into the "books" table. Ensure that the books are related to the authors in the "authors" table.

**Solution 2: Insert Data**

```sql
-- Insert data into the "authors" table
INSERT INTO authors (author_id, author_name) VALUES
    (1, 'J.K. Rowling'),
    (2, 'George Orwell'),
    (3, 'Harper Lee');

-- Insert data into the "books" table
INSERT INTO books (book_id, book_title, author_id) VALUES
    (1, 'Harry Potter and the Sorcerer''s Stone', 1),
    (2, '1984', 2),
    (3, 'To Kill a Mockingbird', 3),
    (4, 'Harry Potter and the Chamber of Secrets', 1),
    (5, 'Animal Farm', 2);
```

**Exercise 3: Update Data**

Change the name of one of the authors in the "authors" table and update the title of one of the books in the "books" table.

**Solution 3: Update Data**

```sql
-- Update an author's name
UPDATE authors
SET author_name = 'Joanne Rowling'
WHERE author_id = 1;

-- Update a book's title
UPDATE books
SET book_title = 'Nineteen Eighty-Four'
WHERE book_id = 2;
```

**Exercise 4: Delete Data**

Delete one of the authors from the "authors" table and one of the books from the "books" table. Ensure that the deletion cascades correctly if necessary.

**Solution 4: Delete Data**

```sql
-- Delete an author (cascading delete will remove associated books)
DELETE FROM authors
WHERE author_id = 3;

-- Delete a book
DELETE FROM books
WHERE book_id = 4;
```

**Exercise 5: Query Data**
Write a query to retrieve the names of all authors and the titles of their books.

**Solution 5: Query Data**

```sql
SELECT a.author_name, b.book_title
FROM authors AS a
JOIN books AS b ON a.author_id = b.author_id;
```
