**COSC 310 Final Project Report (The InstaQuiz Iclicker Clone)**

The Best Group 
-Gus Goerzen
-Tanner Dyck
-Sten Korver
-Patrick Ma
-Kiyoon Kim



**Video Walkthrough: (insert link here)**



**General Development:**

1. Our team built a web-based system that enables instructors to engage students in real-time, interactive quizzes during lectures. It is feature complete and running. Instructors have the ability to create course modules, which serve as virtual meeting spaces for their students. Instructors are able to display custom questions to their students, and receive their responses in real time. Students can easily search for and join these courses online. The system operates on a live webpage, reinforced by a secure login system. Students have access to their individual performance metrics (attendance, grades), while instructors have metrics for their entire class.

2. 
| Initial Requirements | Complete (C) / Incomplete (I) / Modified (M) |
|----------------------|-------------------------------|
| **User:**|
| 1. Users can create an InstaQuiz account with instructor, or student privileges using their email address and a custom password. | C |
| 2. Users can login to their InstaQuiz accounts using their email address and password. | C |
| 3. Users can logout by clicking a constantly displayed button in the top right of the web-page. | C |
| 4. Instructors can create a new course module, this automatically enrolls them in the course, as the instructor. | C |
| 5. Instructors can delete any course module they have personally created. | C |
| 6. Users can search for a course module by title or instructor.  | C |
| 7. Users can enroll in any course module that they are not currently enrolled in. | C |
| 8. Instructors and students can unenroll from a course they are currently enrolled in. | C |
| 9. Instructors can start a live course session in any courses they have created. | C |
| 10. If an instructor has any ongoing live sessions, they can end them whenever, as long as no polling windows are active. | C |
| 11. Users can join a live course session, provided that the instructor has started it already. | C |
| 12. Instructors can create a storage bank of custom questions with corresponding multiple choice answer sets. | C |
| 13. Instructors can start a polling window during a live session as long as no other polls are already in progress. | M |
| 14. Instructors can end their live polling window and declare the correct answer to the question. | M |
| 15. Users can answer a question by clicking on the corresponding answer listed beneath the question text. A user can change their answer during the polling window. | C |
| 16. Instructors can choose to display a summary of the question, (correct answer, how many votes each answer got, how many total responses, etc.) or to keep it hidden from the class. Instructors will be able to see this summary regardless after they end a polling window. | I |
| 17. For each course they are enrolled in, students will be able to see their current score, attendance record, and response history throughout previously attended live sessions. | I |
| 18. For each course they have created, instructors will have access to their student’s grades, attendance records, and response history. | I |
| &nbsp; |
| **Interface:** |
| 1. Students have an overview page which displays each course they are enrolled in, and gives them the option to join a class, or unenroll from one. | C |
| 2. Students can access course pages from the overview page where they will then be able to view their course statistics and join live sessions that are currently running. | I |
| 3. During a polling window, the question statistics are displayed and updated in real-time. (How many students have answered/ not answered) | I |
| &nbsp; |
| **Functional:** |
| 1. InstaQuiz will keep record of all the courses that have been created by instructors and store data about them such as their title, name of instructor, and course code made up of the faculty abbreviations and course number (ex COSC 310). | C | 
| 2. InstaQuiz will allow the creation of student and instructor accounts using email/password combinations. | C |
| 3. InstaQuiz will allow student accounts to search for courses by course title and enroll in the courses they search for and select. The system will also display a menu of the courses that a student has enrolled in and offer the ability to edit the courses they are currently enrolled in. | C |
| 4. InstaQuiz will allow the creation of a new live session to all instructors. Students who have enrolled in a course can join the session provided their instructor has started an InsatQuiz session (i.e. class is live). | C |
| 5. For instructor accounts, InstaQuiz will support the creation of custom questions with multiple choice answers and the ability to poll the class with the questions that were created. | C |
| 6. While the poll is live, the system will allow students to choose and change their answer an unlimited amount of times. IQ will also display the number of students that have submitted an answer. | C |
| 7. The system will allow instructors to end the poll at any time and select a correct multiple choice option which will be displayed on screen to the entire class. The system will then display to the students whether they answered correctly or not. | C |
| 8. The system will allow instructors to view the history on how students have answered their questions and the specific distribution of answers. The distribution of answers for a question will also be displayed at the end of each poll for all users to see. | C |
| 9. The system will also store and allow students to access the number of questions they have answered right for a particular course. The total questions asked for the course will also be shown so the student will see a comprehensive score, something like 16/21. | C |
| 10. InstaQuiz will store a comprehensive history for a course which will show all past polls and questions with the corresponding correct answers. | C |
| &nbsp; | 
| **Non-Functional:** |
| 1. Web service must update in real-time, users are given varying time windows to submit responses. We must minimize response times to and from the main client. | C |
| 2. Web service must be able to handle large amounts of traffic. As an international education tool, thousands of academics may be on the site at one time. Live sessions must be able to support over 300 connected clients at a time. | C |
<br>

Some of the intital requirements were modififed as the system was developed. However, this was expected. User requirements #13 was modified to allow for multiple polls to be open at one time. User requirements #14 was modified to allow for instructors to declare the correct answer during the creation of the question rather than during the closing of a poll. Besides these modifications (we see as improvements), our team was able to deliver everything that was outlined in the initial requirements. The requirements sufficiently captured all of the necessary details. As a result, the system is feature complete and operating as expected. 



3. The InstaQuiz system uses a client-server architecture for easy management and scalability. The system was built with a combination HTML, CSS, JavaScript, and PHP. Live sessions are implemented with AJAX, which enables real-time communication between the client and server. The system is containerized using Docker which allows the app to run consistently accross different environments.

- Client: The client-side InstaQuiz application runs in a web browser and is responsible for providing an interactive interface for both instructors and students. The instructor UI includes various tools for managing quizzes, such as setting up courses, creating questions, starting live sessions, and retrieving quiz metrics. On the other hand, the student UI allows students to join live seesions, participate in the quizzes, and view their grades. The client-side of the system is also responsible for communicating with the sever in order to operate all of the interactive features.

- Server: The server-side application interacts with the database and sends updates to the client-side application in response to requests from the client-side application. The server handles user requests for registration, login, password reset, course creation/deletion, course enrollment/unenrollment, session start/end, question start/end, etc.

- Database: A database is used to store relevant information for user accounts, courses, questions, and scores, which is accessed by the server-side application.

4. Many components were reused accross both student and instructor accounts as they have similar requirements. Database connections, authentication processes, and form validation functions.  

5. How many tasks are left in the backlog?: There are **N** tasks left in the backlog



**CI/CD:**

1. What testing strategies did you implement?  Comment on their degree of automation and the tools used.    Would you (as a team) deal with testing differently in the future?  Make sure to ensure that your testing report is updated to reflect what's actually been done. 

2. How did your branching workflow work for the team?  Were you successful in properly reviewing the code before merging as a team?

The branching workflow worked great for our team. Every large component of the system was completed in a seperate branch e.g. PHP files, live sessions, CICD, and testing. As a team we always worked on a couple different branches at a time and had everyone everyone verify the code before any merges.

3. How would your project be deployed?  Is it docker ready and tested?  Provide a brief description of the level of dockerization you have implemented and what would be required to deploy.

answer here



**Reflections:**

1. How did your project management work for the team?  What was the hardest thing and what would you do the same/differently the next time you plan to complete a project like this?

We found it difficult to

2. Do you feel that your initial requirements were sufficiently detailed for this project?  Which requirements did you miss or overlook?

Yes, completing our requirements resulted in a operational quiz system.

3. What did you miss in your initial planning for the project (beyond just the requirements)?

answer here

4. What process did you use (ie Scrum, Kanabn..), how was it managed, and what was observed?

The Kanban process was used for our project. It was managed through the project table in GitHub. Large features were broken into smaller tasks and each team member self assigned themselves to complete said tasks. The Kanban board was consistently updated thoughout the development process. We also had frequent meetings to discuss new tasks and solutions, aswell as meetings where we coded together. Our approach to the project evolved several times but the Kanban porcess kept every member up to date.  

5. As a team, did you encounter issues with different team members developing with different IDEs?  In the future, would the team change anything in regard to the uniformity of development environments?

As a team we all agreed to develop in VS Code and use Docker to run the system. We would not change anything in regards to the uniformity of the development environment,

6. If you were to estimate the efforts required for this project again, what would you consider?  (Really I am asking the team to reflect on the difference between what you thought it would take to complete the project vs what it actually took to deliver it).  

answer here

7. What did your team do that you feel is unique or something that the team is especially proud of (was there a big learning moment that the team had in terms of gaining knowledge of a new concept/process that was implemented).

answer here

