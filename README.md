Q1. Display all student records from the collection.
db.students_YourRollNo.find()

Q2. Display only the name and department of all students.
db.students_YourRollNo.find({}, {name:1, department:1, _id:0})

Q3. Find students belonging to the CSE department.
db.students_YourRollNo.find({department:"CSE"})

Q4. Find students whose age is greater than 20.
db.students_YourRollNo.find({age:{$gt:20}})

Q5. Find students who scored less than 70 marks.
db.students_YourRollNo.find({marks:{$lt:70}})

Q6. Display students belonging to Kolkata city.
db.students_YourRollNo.find({city:"Kolkata"})

Q7. Sort students by age in ascending order.
db.students_YourRollNo.find().sort({age:1})

Q8. Sort students by marks in descending order.
db.students_YourRollNo.find().sort({marks:-1})

Q9. Display only the first three student records.
db.students_YourRollNo.find().limit(3)

Q10. Update the marks of student Neha to 72.
db.students_YourRollNo.updateOne(
  {name:"Neha"},
  {$set:{marks:72}}
)

Q11. Increase the marks of all students by 5.
db.students_YourRollNo.updateMany(
  {},
  {$inc:{marks:5}}
)

Q12. Delete the student having roll number 5.
db.students_YourRollNo.deleteOne({roll_no:5})

Q13. Find students whose age is between 20 and 22.
db.students_YourRollNo.find({age:{$gte:20,$lte:22}})

Q14. Display students belonging to either CSE or IT department.
db.students_YourRollNo.find({department:{$in:["CSE","IT"]}})
