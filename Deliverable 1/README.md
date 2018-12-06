# Deliverable 1 - Use Cases, Quality Attribute Scenarios, CMS

## Figure 1: Uses Cases

| ID      | Uses Case                                 | Description  |
| --------|:-----------------------------------------:| ------------:|
| UC-1	  | Manage Courses                            | The system should allow the user to view, add, upload and duplicate content to a course. User restrictions to do so should also be allowed. |
| UC-2    | Manage Grading                            |  Appropriate users should be allowed to view, upload, delete or change the grades of a student.  |
| UC-3    | Manage Mailing                            | Appropriate users should be allowed to access and use the mailing system. |
| UC-4		| Manage Static Course Information          | The system shall allow the appropriate users to view, add, or edit static course information. |
| UC-5		| Mange Enrolment Policies                  | The system shall allow the appropriate users to view, add, or edit the enrolment policies.|
| UC-6		| Manage Dynamic Course Information         | The system shall allow the appropriate users to view, add, or edit static course information.|
| UC-7		| Manage Student Teams                      | The system shall allow the appropriate users to view, add, or edit student teams.|
| UC-8		| Manage Archives                           | Users should be able to view, use, duplicate a course/ system archive.|
| UC-9		| Retrieve Course/Student Information       | Appropriate users should be able to view course information or the information of a student in that course.|
| UC-10		| Attendance History                        | The system should allow the user to check the attendance history of a student.|
| UC-11		| Subscribe/Unsubscribe Courses             | The system should allow students to subscribe/unsubscribe to a course.|
| UC-12		| Submit Content                            | The system should allow a user to submit course content online.|
| UC-13		| Send Messages                             | The system should allow a user to send messages to another user.|
| UC-14		| Edit Student Information                  | The system should allow appropriate users to edit the student information for a course.|
| UC-15		| View Notifications                        | The system should allow all users to view course/system notifications.|
| UC-16		| Create/Restore Backups                    | The system should allow the maintainer to create backups and restore system if needed using previous backups.|
| UC-17		| Limit System/File sizes                   | The system should allow the maintainer to limit file sizes being uplaoded by the lecturers or students.|
| UC-18		| Appoint Lecturers/Assistant               | The system should allow the appropriate users to appoint lecturers/assistant lecturers for a course.|
| UC-19		| Retrieve Educational/Personal Information | The system should allow the retrieval of education or personal information of any user.|
| UC-20		| Restrict change of Information            | The system should allow the appropriate users to restrict the information that can be changed by any other uses.|
| UC-21		| Login                                     | The system should allow all users to securely login in to the system and be able to use all the features they are allowed.|
## Figure 2: Quality Attribute Scenarios

| ID    | Quality Attribute      | Scenario                                  | Associated Use Cases  |
| ----- | :---------------------:|:-----------------------------------------:| ---------------------:|
| QA-1  | Performance	     | Sometimes huge file loads are sent to the system at peak load. The system processes the file size and limits the uploading size and time. | UC-17 |
| QA-2  | Modifiability    | A lecturer can upload courses and content for it in realtime or scheduled.                                                   | UC-1 |
| QA-3  | Availability     | The system should always be up for all users, restricting access depending on user type. If the system goes down it should come back up in a few hours. $hours/month downtime allowed.                            | UC-16 |
| QA-4  | Usability		     | A user logs in to the system and can pick from a list of options to view, edit, update or upload information.                             | UC-9 - UC-15, UC-18, UC-21 |
| QA-5  | Security	       | The system keeps tracks of changes done by every user and only allows user to change the information they have access to.                 | UC-20 |


## Figure 3: Constraints

| ID    | Constraint             |
| ----- | :---------------------:|
| CON-1  | Limit Downtime to 4h/month. Announce downtime at least 48 hours in advance. Downtime only during low-intensity hours     |
| CON-2  | Must be user friendly. Support Dutch and English. Max 3 clicks to reach any content. Single login to access all content. Consistent UI   |
| CON-3  | All content must be accessible by disabled users    |
| CON-4  | Allow to import calendar and other data		     |
| CON-5  | Must work and synchronize with secondary universities	       |
