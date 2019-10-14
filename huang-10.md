# To Do List: Michelle
## Abstract Class: User
### Variables
- -pawprint: String
- -password: String
- -email: String
### Methods
- +«constructor» User(username: String, password: String)
- +checkUsername(username: String): Boolean - compare username to existing usernames in database
- +checkPassword(password: String): Boolean - compare password to existing password in database
- +forgotPassword(email: String): Boolean - prompts user to enter email address if password is forgotten
- +resetPassword(username: String)
## Class: Course
### Variables
- +courseNumber: String
- +section: int
- +courseName: String
- +instructor: String
- +ta: String
- +assignmentWeight: double
### Methods
- +«constructor» Course(courseNumber: String, section: int, courseName: String, instructor: String, ta: String, +assignmentWeight: double)
- +selectCourse - return page with course number, section number, course name, instructor, TA, and assignment weights
## Class: Assignment
### Variables
- +name: String
- +description: String
- +course: String
- +section: int
- +assignmentType: String
- +fileTypes: String[] - array of accepted file types
- +due: datetime
- +submitted: datetime
- +grade: double
- +latePolicy: double
### Methods
- +«constructor» Assignment(name: String, description: String, course: String, section: int, assignmentType: String, fileTypes: String[], fileName: String, due: datetime, submitted: datetime, grade: double, latePolicy: double, comments: String)
- +- selectAssignment - return page with assignment name, description, course, section, assignment type, file types, file name, due date/time, submission date/time, grade, late policy, and comment history
## Class: Student extends User
### Variables
- -grade: double
### Methods
- Select assignment
- Upload file - set file path
- Comment on submission - append to comments
- Submit/resubmit file - reset file path, record submission date/time
## Class: TA extends User
### Variables
### Methods
- View submission
- Search student - if student is not enrolled in course, prompt "Student not found"
- Download file
## Class: Instructor extends TA
### Variables
- active: Boolean - true if active, false if inactive
### Methods
- Create/edit/remove courses and sections
- Add/remove TAs
- Add/remove Students
- Create/edit/remove assignments
## Class: Admin extends User
### Variables
### Methods
- Add/edit/remove/disable Instructors
