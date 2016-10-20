# Simple Page Applications / AJAX

## Assignment Specification

In your second assignment, you are expected to perform interaction with a server that informs you with a list of `Students` and their information. You should build a **single page application** that queries this information form the server and displays them on the browser window through a basic interface. The focus is absolutely not on styling of the interface, but better look is always encouraged.

The server provides **RESTful** endpoints. The server provides the following API endpoints:

| Verb | URL endpoint                            | Resource description / Response structure |
| :--- | --------------------------------------- | ---------------------------------------- |
| GET  | /students                               | get list of all student names and IDs / [structure]() |
| GET  | /student/`$student-id`                  | get full information of individual student with id=`$student-id` / [structure]() |
| GET  | /student/`$student-id`/first-name       | get first name of student with id=`$student-id` / [structure]() |
| GET  | /student/`$student-id`/last-name        | get last name of student with id=`$student-id` / [structure]() |
| GET  | /student/`$student-id`/biography        | get biography of student with id=`$student-id` / [structure]() |
| GET  | /student/`$student-id`/email-address    | get email address of student with id=`$student-id` / [structure]() |
| GET  | /student/`$student-id`/links            | get list of links of student with id=`$student-id` / [structure]() |
| GET  | /student/`$student-id`/links/`$link-id` | get link information of with student id=`$student-id` and link id=`$link-id` / [structure]() |

