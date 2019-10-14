# To Do List: Samantha

[Design Doc](https://github.com/computationalmystic/project4-group10/blob/production/requirements.md)

## Class: Credentials
### Attributes
* +first: String
* +last: String
* -username: String
* -password: String
* +userType: String
### Methods
* +«constructor»Credentials(username: String, password: String, userType: String)
* getUsername(): String
* login()
* logout()
- checkValid(): Boolean

## Class: User
### Attributes
* -login: Credentials
### Methods
* +«constructor»User(login: Credentials)

## Class: Student extends User
### Attributes
* +course: Course
* +section: Section
* +year: int
* +major: String
### Methods
* +«constructor»Student(login: Credentials)
* +getAssignments(): Assignment[]
* +getAssignment(name: String, class: String): Assignment
* +submit(assignment: Assignment, file: File, comment: String)

## Class: TA extends User
### Attributes
* +course: Course
* +section: Section
### Methods
* +«constructor»User(login: Credentials)
* -assign(course: Course, section: Section)
* +viewAssignment(name: String): Assignment
* +viewAllAssignments(): Assignment[]
* +viewSubmission(assignment: Assignment, student: Student): Submission
* +viewAllSubmissions(assignment: Assignment): Submission[]
* +downloadSubmissions(submissions: Submission[])
* +searchStudents(first: String, last: String): Student


## Class: Instructor extends TA
### Attributes
* +courses: Course[]
* +tas: TA[]
* roster: Student[]
### Methods
* +«constructor»Instructor(login: Credentials)
* +createCourse(courseNum: String)
* +editCourse(course: Course)
* +removeCourse(course: Course)
* +createSection(course: Course)
* +editSection(section: Section)
* +removeSection(section: Section)
* +addTA(assistant: TA, section: Section)
* +removeTA(assistant: TA, section: Section)
* +addStudent(student: Student, section: Section)
* +addStudents(studentListFile: File)
* -createStudents(studentListFile: File): Student[]
* +removeStudent(student: Student, section: Section)
* +createAssignment(name: String, startDate: date, dueDate: date, availableUntil: date)
* +editAssignment(assignment: Assignment)
* +removeAssignment(assignment: Assignment)


## Class: System Administrator extends User
### Attributes
### Methods
* +«constructor»User(login: Credentials, key: int)
* +addInstructor(person: Instructor)
* +deleteInstructor(person: Instructor)
* +modifyInstructor(person: Instructor)
* +disableInstructor(person: Instructor)

## Class: Course
### Attributes
* +courseNum: String
* +teacher: Instructor
* +taList: TA[]
* +sections: Section[]
* +startDate: date
* +endDate: date
### Methods
* +«constructor»Course(courseNum: String, teacher: Instructor, startDate: date, endDate: date)

## Class: Section
### Attributes
* +courseNum: String
* +teacher: Instructor
* +assistant: TA
* +section: int
* +roster: Student[]
### Methods
* +«constructor»Section(course: Course)

## Class: Assignment
### Attributes
* course: Course
* section: Section
* +name: String
* +startDate: date
* +dueDate: date
* +availableUntil: date
* +submissions: Submission[]
### Methods
* +«constructor»Assignment(name: String, startDate: date, dueDate: date, availableUntil: date)

## Class: Submission
### Attributes
* +assignment: Assignment
* +student: Student
* +file: File
* +timeStamp: dateTime
### Methods
* +«constructor»Submission(file: File, assignment: Assignment, timeStamp: dateTime)
* +remove()

## Class: Grade
### Attributes
* +percent: double
* +comment: String
* +timeStamp: dateTime
### Methods
* +«constructor»Grade(submission: Submission, comment: String, timeStamp: dateTime)
