# UDB-3
Q1. Display all employee records.
db.employees.find()

Q2. Create an index on emp_id field.
db.employees.createIndex({emp_id: 1})

Q3. Create an index on department field.
db.employees.createIndex({department: 1})

Q4. Create a compound index on department and salary.
db.employees.createIndex({department: 1, salary: 1})

Q5. Find employees working in IT department.
db.employees.find({department: "IT"})

Q6. Display employees whose salary is greater than 60,000.
db.employees.find({salary: {$gt: 60000}})

Q7. Sort employees by salary in descending order.
db.employees.find().sort({salary: -1})

Q8. Display top 3 highest paid employees.
db.employees.find().sort({salary: -1}).limit(3)

Q9. Display employees having experience more than 5 years.
db.employees.find({experience: {$gt: 5}})

Q10. Analyze query performance using explain().
db.employees.find({department: "IT"}).explain("executionStats")
