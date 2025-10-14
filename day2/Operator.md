# Operators in MongoDB

## Comparison Operators

- $eq: Equals to : { age: {$eq: 40 }}
- $ne: Not Equals to
- $gt: gretaer than
- $gte: gretaer than or equals to
- $lt: Less than
- $lte: less than or equals to
- $in: Values in Array 
- $nin: Values not in Array 

```bash
# Find all employees from HR and IT Department
db.employee.find({ department: { $in: ["IT", "HR"]}})
```

## Logical operator

- Combine more than 1 condition

- $and : Returns docs that match all conditions

```bash
db.employee.find({
    $and: [
        { age: {$gt: 18}},
        { designation: "Software Engineer"}
    ]
})
# Find all employees having salary between 60k to 1L
db.employee.find({
    $and: [
        { salary: {$gte: 60000}},
        { salary: {$lte: 100000}}
    ]
})
```

- $or : returns docs that match any condition
- $not : inverts condition
- $nor: Returns the docts that fails all condition 








