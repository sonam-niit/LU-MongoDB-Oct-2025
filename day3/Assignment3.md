# Mini Project: Library Database Analysis

## Objective
Learn MongoDB CRUD and query operations using a real-world dataset — a library database that manages books, authors, and members.

---

## Database & Collection
**Database name:** `libraryDB`  
**Collection name:** `books`

---

##  Sample Data
Insert the following documents into your collection:

```js
db.books.insertMany([
  {
    _id: 1,
    title: "The Alchemist",
    author: "Paulo Coelho",
    genre: "Fiction",
    published_year: 1988,
    copies_available: 5,
    ratings: [4, 5, 4, 3, 5]
  },
  {
    _id: 2,
    title: "Atomic Habits",
    author: "James Clear",
    genre: "Self-Help",
    published_year: 2018,
    copies_available: 2,
    ratings: [5, 4, 5, 5, 4]
  },
  {
    _id: 3,
    title: "Sapiens: A Brief History of Humankind",
    author: "Yuval Noah Harari",
    genre: "History",
    published_year: 2011,
    copies_available: 3,
    ratings: [5, 5, 5, 4, 5]
  },
  {
    _id: 4,
    title: "Clean Code",
    author: "Robert C. Martin",
    genre: "Programming",
    published_year: 2008,
    copies_available: 1,
    ratings: [5, 4, 5, 3, 5]
  },
  {
    _id: 5,
    title: "The Pragmatic Programmer",
    author: "Andrew Hunt",
    genre: "Programming",
    published_year: 1999,
    copies_available: 4,
    ratings: [5, 5, 5, 5, 4]
  },
  {
    _id: 6,
    title: "Think and Grow Rich",
    author: "Napoleon Hill",
    genre: "Self-Help",
    published_year: 1937,
    copies_available: 6,
    ratings: [4, 5, 5, 4, 5]
  },
  {
    _id: 7,
    title: "Deep Work",
    author: "Cal Newport",
    genre: "Self-Help",
    published_year: 2016,
    copies_available: 3,
    ratings: [5, 5, 4, 4, 5]
  },
  {
    _id: 8,
    title: "Introduction to Algorithms",
    author: "Thomas H. Cormen",
    genre: "Programming",
    published_year: 2009,
    copies_available: 2,
    ratings: [5, 5, 5, 5, 5]
  },
  {
    _id: 9,
    title: "The Power of Now",
    author: "Eckhart Tolle",
    genre: "Spirituality",
    published_year: 1997,
    copies_available: 5,
    ratings: [4, 4, 5, 4, 5]
  },
  {
    _id: 10,
    title: "Educated",
    author: "Tara Westover",
    genre: "Memoir",
    published_year: 2018,
    copies_available: 2,
    ratings: [5, 4, 4, 5, 4]
  }
])
```

---

## Assignment Tasks

### Basic Queries
1. Retrieve all books from the collection.  
2. Find all books where the genre is `"Programming"`.  
3. Find books published after the year 2010.  
4. Display only `title` and `author` of all books.  
5. Find the book with the title `"Clean Code"`.  

---

### Intermediate Queries
6. Find all books that have more than 3 copies available.  
7. Count the number of books in each genre. *(Hint: use `$group`)*  
8. Calculate the **average rating** of each book. *(Hint: use `$avg` on the `ratings` array)*  
9. Find the **top 3 most recently published** books. *(Hint: sort by `published_year`)*  
10. Find all authors who have written books before the year 2000. *(Hint: use `$lt` with `published_year`)*  

---

### Advanced Queries
- Add a new field `"borrowed_count"` and update it for each book.  
- Write a query to find the **most borrowed book**.  

---

### Submissions
- MongoDB query commands (screenshots needed).  
- Submit screenshots (in PDF or doc) with the filename: YourName_MongoDB_Assignment3.pdf
