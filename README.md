---
  tags: oop, tdd
  languages: ruby
---

# Domain Model for a School

In this assignment you'll be writing a simple app for a school. You're going to 
Want to get write the models below and get the test suite to pass. 

## Instructions

### Part 1. 

Write a model that stores students along with the grade that they are in so the 
following code would work:

```ruby
school = School.new("Bayside High School")
```

### Part 2. 

If no students have been added, the roster should be empty:

```ruby
school.roster
# => {}
```
### Part 3.

When you add a student, they get added to the correct grade.

```ruby
school.add_student("Zach Morris", 9)
school.roster
# => {9 => ["Zach Morris"]}
``` 

You can, of course, add several students to the same grade, and students to different grades.

```ruby
school.add_student("AC Slater", 9)
school.add_student("Kelly Kapowski", 10)
school.add_student("Screech", 11)
school.roster
# => {9 => ["Zach Morris", "AC Slater"], 10 => ["Kelly Kapowski"], 11 => ["Screech"]}
```

### Part 4. 

Also, you can ask for all the students in a single grade:

```ruby
school.grade(9)
# => ["Zach Morris", "AC Slater"]
```

### Part 5.
 
 You should be able to get a sorted list of all the students. Grades are sorted 
 in descending order numerically, and the students within them are sorted in 
 ascending order alphabetically.

```ruby
school.sort
# => {9 => ["AC Slater", "Zach Morris"], 10 => ["Kelly Kapowski"], 11 => ["Screech"]}
```