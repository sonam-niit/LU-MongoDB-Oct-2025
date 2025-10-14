# CRUD Operations

- C - Create data
- R - Retrieve Data
- U - Update Data
- D - Delete Data

- Retrieval Data 

```bash
db.employee.find() # find all data

# find Employee whose name is Neha Verma
db.employee.findOne({ name: "Neha Verma"})

# Find All Employees from Department "IT"
db.employee.find({ department: "IT"})

# Find all employees whose salary is greater than 60,000
db.employee.find({ salary: { $gt: 60000}})

# find only selected fields
db.employee.find({name:"Ravi Patel"},{name:1,department:1})

db.employee.find({name:"Ravi Patel"},{name:1,department:1,designation:1})

# by default _id field will come in selected Retrieval
# to not get that value use _id:0
db.employee.find(
    {name:"Ravi Patel"},
    {name:1,department:1,designation:1,_id:0}
)
```

## Update Data

```bash
# update Ravi patel Salary to 60000

db.employee.updateOne(
    { name: "Ravi Patel"},
    { $set: {salary: 60000}}
)

# Update Many records

# Let's Give Salary hike of 10% to all Employees in IT Department

db.employee.updateMany(
    { department: "IT" },
    { $mul: {salary: 1.1 }}
)

# Add New Field For Update

db.employee.updateMany(
    {},
    { $set: {status: "active"}}
)

```

## Remove Documents (DELETE)

```bash

# delete employee whose name is Neha verma
db.employee.deleteOne({
    name: "Neha Verma"
})

# delete all emplyees from Sales Department
db.employee.deleteMany({
    department: "Sales"
})

# Drop entire collections
db.employee.drop()
```

## Find Duplicates using Aggregation

```bash
db.employee.aggregate([
    {
        $group: {
            _id: { name: "$name", department:"$department"},
            count: {$sum: 1},
            docs: { $push: "$_id"}
        }
    },
    {
        $match: {
            count: {$gt: 1}
        }
    }
])
```