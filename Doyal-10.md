# To Do List: Byron
## Class: User
### Attributes
* +First Name
*	+Last Name
*	-username
*	-password
### Methods


## Class: Course
### Attributes
*	+courseNum: string
*	+courseName: string
*	+instructor: String
*	+ta: String
*	+section 
### Methods
*	+chooseCourse

## Class: Assignment
### Attributes
*	+name: String
*	+description: String
*	+course: String
*	+dueDate: String
*	+section: int
*	+filetype: String[]
*	+grade: double
### Methods
*	+<<**constructor**>>Assignment(name: String, description: String, course: String, dueDate: String, section: int, filetype: String[], grade: double)
*	upload
*	submit
*	resubmit

## Class: Student extends User
### Attributes
### Methods
*	+getCourseInfo(Course) – allows you to bring up the courses the student is taking
*	+getAssignment(Assignment) -retrieves the info of a specific assignment
*	submit
*	-addComment – allows the user to add a comment to their submitted work 

## Class: TA extends User
### Attributes
*	+course: Course
*	+section: Section
### Methods
*	-assignCourse(course: Course, section: Section)
*	+readAssigment(name: String): Assignment
*	+viewSubmission(assignment: Assignment, student: Student): Submission
*	+searchStudents(firstName: String, lastName: String): Student

## Class: Instructor extends TA
### Attributes
*	+courses: Course[]
*	+ta: TA[]
*	Roster: Student[]
### Methods
*	+createCourse(courseNum: String, professor: String, taList: TA[]. sections: Section[])
*	removeCourse(course:Course)
*	editCourse(course:Course)
*	+createSection(courseNum:String, professor: String, secTA: TA, section: int, roster:Student[])
*	removeSection(section:Section)
*	editSection(section:Section)
*	addTA
*	removeTA
*	addStudent(name:String)
*	removeStudent(name:String)

## Class: System Administrator extends User
### Attributes
### Methods
*	add/edit/remove Instructors
## Class: Course
### Attributes
*	courseNum: String
*	professor: String
*	taList: TA[]
*	sections: Section[]
### Methods

## Class: Section
### Attributes
*	courseNum: String
*	professor: String
*	secTA: TA
*	section: int
*	roster: Student[]
### Methods
*	<<**constructor**>>Section(course:Course)

