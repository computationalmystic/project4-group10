# Design Assignment: This is the standard REQUIREMENT ANALYSIS FOR AN ASSIGNMENT SUBMISSION SYSTEM
## Introduction 

**Note:** This requirements analysis provides one possible interpretation of the requirements. It is a simple example that sticks very close to the problem description. Items may possibly be missing, inconsistent, or incorrect although overall it is very good.

Data in this particular analysis has been mostly limited to entities, with few attributes specified and no primary keys or data constraints given. 

## SYSTEM CONSTRAINTS 
1. Web server software
2. Database management system (DBMS)
3. File server for submitted files
4. Physical or virtual server(s) with compatible OS installed to host the web server, DBMS, and file server, with network and internet connectivity
5. Backup and recovery system
6. Client computers with web browser and Internet access


## USERS/ ACTIVITIES / RELEVANT DATA / CONSTRAINTS

### STUDENTS
1. Login/Logout
  - relevant data: credential data (username & password)
  - constraints: Students can use the system and access their courses and only their courses when they input correct username and matched password.
2. Student is able to read assignment instructions
  - relevant data: assignment data
  - constraints: Students can only access assignments of the courses that they are enrolled in.
3. Student can select assignment they want to submit
  - relevant data: course data, assignment data
  - constraints: Students can only choose the assignment from the classes that they enrolled. Students can only submit assignments that are open.
4. Student can upload files 
  - relevant data: course data, assignment data, submission data
  - constraints: System should allow only correct file types for uploading. 
5. Student can provide a comment along with a file submission
  - relevant data: course data, assignment data, submission data
  - constraints: System should allow a maximum number of characters and not allow sql injection.
6. Student can submit/re-submit uploaded file 
  - relevant data: course data, assignment data, submission data
  - constraints: Students can only choose the assignment from the classes that they enrolled. Students can only submit assignments that are open.

### TEACHER ASSISTANTS (TA)
1. Login/Logout
  - relevant data: credential data (username & password)
  - constraints: TAs can use the system and access their course sections and only their course sections when they input correct username and matched password.
2. TA can view course assignments.
  - relevant data: assignment data
  - constraints: TAs can only access assignments of the course sections that they are assigned to.
3. TA can view student submissions for an assignment.
  - relevant data: student data, assignment data, submission data
  - constraints: TAs can only access assignments of the course sections that they are assigned to.
4. TA can search students in a course
  - relevant data: student data, course data
  - constraints: TAs can search only the students who are in the course sections that they are assigned to manage.
5. TA can collect assignments by downloading students' submission files
  - relevant data: course data, assignment data, submission data
  - constraints: The system will show only the assignments from the course sections for which they are listed as a TA.

### INSTRUCTOR
1. Login/Logout
	  - relevant data: credential data (username & password)
	  - constraints: Instructors can use the system functions except student and system administrator functions, when they input correct username and matched password.
2. Instructors can perform all functions TAs can perform.
	  - Constraints: instructors can only access courses they have created.
3. Instructor can create/edit/remove courses and sections
	  - relevant data: student data, course data (including start and end dates), section data
	  - constraints: Instructors can only manage courses they have created, but cannot remove or access the other instructors' courses.
4. Instructor can add /remove TAs for the course sections
	  - relevant data: TA data, course data
	  - constraints: Instructors can only add or remove TAs from their own course sections. 
5. Instructor can add/remove students in the course sections
	  - relevant data: course data, student data
	  - constraints: Instructors can only manage their course. Instructors should be able to upload students in bulk from a file.
6. Instructor can create/edit/remove assignments of each course
	  - relevant data: course data, assignment data (including start dates, due dates, and availability-end dates)
	  - constraints: Instructors can only manage in their course. Assignments cannot be deleted between when a submission has occurred and the course end date.

### SYSTEM ADMINISTRATOR
1. Admin can add/edit/remove/disable instructors
	  - relevant data: instructor data
	  - constraints: Admin can manage only instructors; the system should check the type of user to be added is instructors. Instructors cannot be deleted if they have courses. Instructors cannot be disabled (have privileges revoked) if they have an active course.
