# Simple Page Applications / AJAX

## Assignment Specification

In your second assignment, you will be expected to perform interactions with a server that provides you with a list of `Students` and their information. You will build a [**single page application**](https://en.wikipedia.org/wiki/Single-page_application) that queries this information from the server and displays it on the browser window through a basic interface. The focus is not on styling the interface, but a better look is always encouraged.

Each `student` entity has the following information bound to it:

- Student id
- First name
- Last name
- Student email address
- Student biography
- Profile picture
- List of portfolio links (optional,arbitrary number of links)

### Requirments

Your **single page application** must not get load and fetch students information all at once or at the initial load of the page. Instead, individual student information must be queried and fetched as requested by the user (when the user navigates to a student). Your **single page application** must have right/left or up/down controls or any other format of controls to navigate through different students. Additionaly, you can use [carousel](https://github.com/samantehrani/simple-carousel), [accordion](https://github.com/samantehrani/simple-accordion), [search box](), or [modal](https://github.com/samantehrani/simple-modal) user interface elements that we built in [assignment 1](https://github.com/web-advanced-fall-2016/assignment-1-spec). Or any other third-party UI Element. You have a list of student information and you want to display them indivudualy; Choose to be creative or not, it's up to you.

- You will be **allowed to use JQuery**. That being said, native [XMLHTTPRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) or [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) is encouraged and recommended. 
- You will be **allowed to use third-party front-end frameworks** like [Bootstrap](http://getbootstrap.com/) / [Foundation](http://foundation.zurb.com/) as well.
- You **must use gulp task automation**. Use this gulpfile setup and structure: [https://github.com/web]().
- You can use plain **CSS**. That being said, the use of **SASS** is encouraged. 

### Bonus Requirements

- Build a **demo page** using [GitHub Project Page](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/)
- Store student information in **[sessionStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage)** to avoid loading information in case they have been loaded once before.
- Use **[Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API)** to query and load the content.
- Make it look beautiful! Be proud of your work. (The most advanced, optimized, modern, or flawless code won't impress much when it is visually unappealing)  

### Submission Details

All the submissions must be done through github to our class organization [@web-advanced-fall-2016](https://github.com/web-advanced-fall-2016). The assignment will be accommodate and distributed using [GitHub Classroom](https://classroom.github.com/). GitHub classroom will automatically create a repository in our organization for each student and will grant the, administrative rights to that repository.    
All students **MUST** visit this url: [Confirmation Link](). There you will be asked to accept and confirm the reception of the *Second Assignment* and consequently a repository will be automatically created for you under our oranization. The name of your repository will follow the following pattern: `assignment-2-${your GitHub username}`.

### Assignment Demo 

Here is a **[demo]()** that meets all the requirements. 

------

## Server Information

A NodeJS server is setup, deployed and accessible through this static ip address: `8.8.8.8` on port `8080`. If you want run the server locally on your personal machine, you will need to clone the server code from the this repository [https://github.com/samantehrani/students-api-server]() and deploy the server on your machine. For more information, refer to [Server setup walkthrough]().

### API Information

The server provides **RESTful** endpoints. The format of the responses are always `JSON` ([http://json.org/](http://json.org)) .The server provides the following API endpoints:

#### Students endpoint

| Verb | URL endpoint                | Resource description                     | Response structure          |
| :--- | --------------------------- | ---------------------------------------- | --------------------------- |
| GET  | /students                   | get list of all student names and their ids | [structure](https://github.com/web-advanced-fall-2016/assignment-2-spec/blob/master/README.md#students) |
| GET  | /students/`$student-id`     | get full information of individual student with id=`$student-id` | [structure](https://github.com/web-advanced-fall-2016/assignment-2-spec/blob/master/README.md#studentsstudent-id)               |
| GET  | /students/`$student-id`/bio | get full biography of student with id=`$student-id` | [structure](https://github.com/web-advanced-fall-2016/assignment-2-spec/blob/master/README.md#studentsstudent-idbio)               |

##### /students

```json
[
  {
    "id": "43123",
    "first_name": "Saman",
    "last_name": "Tehrani"
  },
  {
	"id": "12314",
    "first_name": "Raha",
    "last_name": "Ghasemi"
  },
  ...
]
```

##### /students/`$student-id`

```json
{
  "id": "12314",
  "first_name": "Raha",
  "last_name": "Ghasemi",
  "email": "ghasemi@gmail.com",
  "excerpt": "MFA Design & Technology Candidate, Class of 2017",
  "profile_picture": "/assets/img/rahaghasemi.png",
  "links": [
	{
	  "url": "https://github.com/rahaghasemi",
      "name":"GitHub",
  	  "id": "23425",
      "icon": "/assets/img/github.png"
    },{
      "url": "http://rahaghasemi.com",
      "name":"Personal Portfolio",
  	  "id": "62355"
    },
    ...
  ]
}
```

##### /students/`$student-id`/bio

```json
{
  "id": "12314",
  "full_bio": "Brisket swine fatback meatloaf salami. Tri-tip porchetta turkey short ribs meatloaf. Flank pastrami andouille frankfurter biltong chuck. Pork loin meatball bresaola ham fatback swine, porchetta ground round shank t-bone beef spare ribs chuck salami hamburger.",
  "excerpt": "MFA Design & Technology Candidate, Class of 2017"
}
```



#### Good Luck :fire::fire::thumbsup: 
