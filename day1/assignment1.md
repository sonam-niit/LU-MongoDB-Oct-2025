# MongoDB Compass Practice Assignment – Day 1

## Objective
- To practice creating a MongoDB database, collections, and inserting JSON documents using MongoDB Compass.

### Assignment Instructions

1. Create a New Database
    - Database name: schoolDB
    - Collection name: students
    - Insert at least 3 student documents
    - Each document must include the following fields:
        1. name (string)
        2. age (number)
        3. city (string)
        4. courses (array of strings)
        5. marks (object with subject → score key–value pairs)
    - Example
```json

{
  "name": "Sonam Soni",
  "age": 25,
  "city": "Delhi",
  "courses": ["Math", "Science"],
  "marks": {
    "Math": 88,
    "Science": 92
  }
}
```

2. Insert at least one document with a new field
    - Example: add "hobbies": ["Cricket", "Music"] or "email": "ravi@example.com"

3. Explore Data in Compass

    - Edit one student’s marks
    - Add a new student directly from the UI

### Submission

- Take screenshots of:
- The database and collection list in Compass
- The inserted documents

- Submit screenshots (in PDF or ZIP) with the filename: YourName_MongoDB_Assignment1.pdf