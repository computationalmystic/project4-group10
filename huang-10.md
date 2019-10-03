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
## Class: Student extends User
### Variables
### Methods
- Select course
- Read assignment
- Select assignment
- Upload file
- Comment on submission
- Submit/resubmit file
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