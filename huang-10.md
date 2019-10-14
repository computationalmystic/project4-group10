# To Do List: Michelle
## Abstract Class: User
### Variables
- -pawprint: String
- -password: String
### Methods
- +«constructor» User(username: String, password: String)
- +checkUsername(username: String): Boolean
- +checkPassword(password: String): Boolean
- +forgotPassword(): Boolean
- +resetPassword(username: String)
## Class: Course
### Variables
- +courseNumber: String
- +courseName: String
- +instructor: String
- +ta: String
- +section: int
### Methods
- +selectCourse
## Class: Assignment
### Variables
- +name: String
- +description: String
- +course: String
- +section: int
- +assignmentType: String
- +fileTypes: String[]
- +due: datetime
- +submitted: datetime
- +grade: double
- +latePolicy: double
### Methods
- +«constructor» Assignment(name: String, description: String, course: String, section: int, assignmentType: String, fileTypes: String[], fileName: String, due: datetime, submitted: datetime, grade: double, latePolicy: double, comments: String)
- upload
- submit
- resubmit
## Class: Student extends User
### Variables
### Methods
- getCourseData(Course)
  Select course
- getAssignmentData(Assignment) - retrive assignment name, description, course, section, assignment type, file types, file name, due date/time, submission date/time, grade, late policy, and comments
- Select assignment
- Upload file - set file path
- Comment on submission - set comments
- Submit/resubmit file - reset file path, record submission date/time
## Class: TA extends User
### Variables
### Methods
- Select course
- View assignment
- View submission
- Search student
- Download file
## Class: Instructor extends TA
### Variables
- active: Boolean
### Methods
- Create/edit/remove courses and sections
- Add/remove TAs
- Add/remove Students
- Create/edit/remove assignments
## Class: Admin extends User
### Variables
### Methods
- Add/edit/remove/disable Instructors
## Class: Assignment
### Variables
- +name: String
- +course: String
- +section: int
- +file-types: String
- +grade: double
- +due: Date
- +submitted: Date
### Methods

