# Group 10
### Samantha, Michelle, Byron

## Commonalities
## Class: User
### Variables
- username: String
- password: String
### Methods
- +«constructor» User(username: String, password: String)
## Class: Student extends User
### Variables
- -course: Course
- -section: Section
### Methods
- +«constructor» Student(username: String, password: String)
## Class: TA extends User
### Variables
- -course: Course
- -section: Section
### Methods
- +«constructor» TA(username: String, password: String)
- searchStudent(name): Student
## Class: Instructor extends User
### Variables
- tas: TA[]
- students: Student[]
### Methods
- «constructor» Instructor(username: String, password: String)
- addCourse(courseNumber: String)
- editCourse(course: Course)
- removeCourse(course: Course)
- addSection(course: Course)
- editSection(section: Section)
- removeSection(section: Section)
- addTA(ta: TA, course: Course)
- removeTA(ta: TA)
- addAssignment(name: String, course: String, section: int, due: datetime, submitted: datetime)
- editAssignment(assignment: Assignment)
- removeAssignment(assignment: Assignment)
## Class: System Administrator extends User
### Variables
### Methods
- +«constructor» SystemAdmin(username: String, password: String)
- +addInstructor(instructor: Instructor)
- +editInstructor(instructor: Instructor)
- +removeInstructor(instructor: Instructor)
## Class: Course
### Variables
- +courseNumber: String
- +instructor: Instructor
- +tas: TA[]
- +sections: Section[]
### Methods
- +«constructor» Course
## Class: Section
### Variables
- +courseNumber: String
- +instructor: Instructor
- +tas: TA[]
- +section: int
### Methods
- +«constructor» Section(course: Course)
## Class: Assignment
### Variables
- +name: String
- +course: String
- +section: int
- +due: datetime
- +submitted: datetime - keeps last submitted timestamp
### Methods
- +«constructor» Assignment
## Class: Submission
### Variables
- file: File
- comments: String
### Methods


## Next Steps
First, we will create a master list of tasks where we can track their progression and components.  After, we will prioritize the tasks based on importance and topological order.  We will divide the first tasks among our group members, giving each member an equal amount of work that alligns to their abilities.  We will decide a due date for the first tasks, upon which we will meet and evaluate everyone's progress.  If a task is complete, we will update it's status on our masterlist and assign that person the next necessary task.  If it isn't complete, we will discuss and try to resolve any blockers and decide if the task should be transfered to someone else.  Any new tasks that have arisen will be added to our list in a sensible position.  This process will repeat until all the tasks are done.
