# Simple Page Applications / AJAX

## Assignment Specification

In your second assignment, you are expected to perform interaction with a server that informs you with a list of `Students` and their information. You should build a **single page application** that queries this information form the server and displays them on the browser window through a basic interface. The focus is absolutely not on styling of the interface, but better look is always encouraged.

Each student has the following information bound to it:

- First name
- Last name
- Student id
- Student email address
- Student biography
- Profile picture
- List of portfolio links (optional,arbitrary number of links)



### Requirments

Your **single page application** must not get load and fetch students information all at once and at the initial load time of page, whereas, individual student information must get loaded as per requested (when user navigated on a student). Your **single page application** must have right/left or up/down or any other format of controls to navigate through different students. Also, you can use [carousel](), [accordion](), [search box](), or [modal]() user interface elements that we built in [assignment 1](). 

- You are **allowed to use JQuery**. That said, native [XMLHTTPRequest]() or [Fetch API]() is recommended. 
- You are **allowed to use third-party front-end frameworks** like [Bootstrap]()/[Foundation]().
- You **must use gulp task automation** provided here: [https://github.com/web]().
- You can use plain **CSS**. That said, use of **SASS** is encouraged. 



### Bonus Requirements

- Build a **demo page** using [GitHub Project Page]()
- Store students information in **[sessionStorage]()** in order to avoid loading information once they have been loaded once.
- Use **[Service Workers]()** in order to query and load content
- Make it look beautiful! Be proud of your work.



### Assignment Demo 

Here is a **[demo]()** that meets all the requirements. 



------

### Server Information

A NodeJS server is setup, deployed and accessible through this static ip address: `8.8.8.8` on port `8080`. In addition, if you want run the server locally on your personal machine, you need to clone the server code from the this repository [https://github.com/samantehrani/students-api-server](https://github.com/samantehrani/students-api-server) and deploy the server on your machine. For more information, refer to [Server setup walkthrough]().



### API Information

The server provides **RESTful** endpoints. The format of the responses are always `JSON` .The server provides the following API endpoints:

#### Students endpoints

| Verb | URL endpoint                             | Resource description                     | Response structure |
| :--- | ---------------------------------------- | ---------------------------------------- | ------------------ |
| GET  | /students                                | get list of all student names and their ids | [structure]()      |
| GET  | /students/`$student-id`                  | get full information of individual student with id=`$student-id` | [structure]()      |
| GET  | /students/`$student-id`/first-name       | get first name of student with id=`$student-id` | [structure]()      |
| GET  | /students/`$student-id`/last-name        | get last name of student with id=`$student-id` | [structure]()      |
| GET  | /students/`$student-id`/biography        | get biography of student with id=`$student-id` | [structure]()      |
| GET  | /students/`$student-id`/email-address    | get email address of student with id=`$student-id` | [structure]()      |
| GET  | /students/`$student-id`/links            | get list of links of student with id=`$student-id` | [structure]()      |
| GET  | /students/`$student-id`/links/`$link-id` | get link information of with student id=`$student-id` and link id=`$link-id` | [structure]()      |





#### Good Luck :fire::fire::thumbsup: 