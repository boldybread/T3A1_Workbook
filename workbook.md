# T3A1 - Workbook

## Q1 Provide an overview and description of a standard source control process for a large project

Correct information in the answer, provided in general terms, including some irrelevant info. More specific detail would be good to see, e.g. what steps are involved in a source controle process?

Large projects tend to be worked upon by many developers as well as having many features all being worked on simultaneously that potentially will change other functionality and potentially introduce bugs into the code. Therefore there needs to be a robust system in place that can control versions of the code to enable multiple people working on it at once without disrupting each other as well as offering the option to revert back to a previous version in case of catastrophic errors being introduced.





from T2 workbook A

Trunk-based development is one of the most popular version control methods which involves coders working on small parts of an application's code, and merging that frequently with the main branch or "trunk". This continuous integration ensures the project moves along at an optimum pace as it reduces the time developers would be waiting for other coders to complete work, so ultimately the project will be completed quicker and more efficiently.

Due to the small size of the frequent commits trunk-based development is easy to review as senior developers can quickly and efficiently review these small updates to the code, again improving that continuous integration and overall efficiency.

The practice of trunk-based development is built upon frequent consistent commits therefore it is best practice to develop small batches of code and committing them daily to the main branch. These small batches of code also promote a quicker review process as senior developer can easily see the desired effect in a few lines of code and troubleshoot or approve as necessary.

Another standard practice is using feature flags which are if-statements that allow a certain feature to be turned on or off, this reduces the chance of code errors effecting the whole application when many coders are working on a project at once. This again improves the speed and efficiency of the project.

Another practice that has become standard to achieve continuous integration is the implementation of automated testing. Automated testing works smoothly with trunk-based development by checking the small batches of code that have been committed to the main branch and approving or denying them automatically depending on whether there are any issues or not. As you can see this would greatly speed up the process as it doesn't rely on a senior developer having to review and approve every small change to the project. These immediate approvals ensure the developers can move straight on to the next bit of code they want to work on, and that other coders are always working on the most updated code. It also means senior developers are free to focus on optimising the code rather than wasting time fixing up incorrect code.

Best practice in trunk-based development involves deleting branches after a merge has been completed. We want to aim to have three of fewer active branches in the project's repository. If developers are ensuring they are completing daily merges to the main branch there is no reason to keep old branches around that have become inactive.

## Q2 What are the most important aspects of quality software?

List discuss and demonstrate 6 software quality characteristics

## Q3 Outline a standard high level structure for a MERN stack application and explain the components

MERN stack is a framework including four javascript technologies together, MongoDB, Express, React and Node that together make the acronym MERN. MERN stacks are organised in a way that separates frontend and backend code and follows the Model-View-Controller (MVC) architecture pattern storing frontend code within the client directory and backend code with the server directory. Due to this separation the code becomes more easily maintained and managed. MERN stacks are used for developing Javascript apps as the four technologies making the stack all use JS. MongoDB is a NoSQL database, react is a JS library for building user interfaces based on UI components, Express is a web app framework and Node is a JS runtime enviroment to create servers, web apps and scripts.

### MongoDB - Model Component

MongoDB is a database management system storing data in documents with key-value pairs, similar to JSON objects. A developer is able to use this to create tables, schemas and functions that interact with the database. It utilises JS interface for querying updating and deleting records from the tables/databases. MongoDB is responsible for the managing the business logic and data of the app.

### ReactJS - Visual Component

ReactJS is a Javascript library that allows the development of UI for mobile apps and single page applications. React is the frontend framework of the MERN stack responsible for the data displayed to the users. ReactJS uses a virtual document object model for doing everything and enables users to code in JS and develop user interface components.

### ExpressJS & NodeJS - Controller Component

The backend code of the MERN stack is built with NodeJS and ExpressJS. NodeJS is a JavaScript runtime environment that allows developers to run code on a server. It comes with the node package manager allowing users to select from packages or node modules. NodeJS is open source and allows for fast execution of code. ExpressJS is a NodeJS framework which simplifies writing backend code for a developer. It prevents the need for a developer to create multiple Node modules and offers a range of middleware to keep the code precise. The controller component handles user input and updates the model and view components accordingly. It contains functions to handle HTTP requests and responses within the controller directory.

### Server Directory - Backend code storage

The backend code built by NodeJS and ExpressJS is stored within the server directory. It typically would contain the aforementioned controllers directory as well as the config directory, models directory, routes directory and server.js file which is the entry point of the backend application.

### Client Directory - Frontend code storage

The client directory contains the frontend code of the web application typically containing a public directory for the HTML file displayed in the browser and a src directory containing frontend source code including a components directory for the React components as well as App.js and index.js files.

## Q4 A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?

Effectively describes a range of skills and knowledge required by IT workers to complete a quality web development project

## Q5 With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges

Effectively describes a range of skills and knowledge used to complete a project.

## Q6 With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature

Evaluates effectiveness of knowledge and skills accurately, providing examples, and providing an insightful improvement on each skill

## Q7 Explain control flow, using an example from the JavaScript programming language

Provides a thorough explanation of control flow in programming

## Q8 Explain type coercion, using examples from the JavaScript programming language

Provides a thorough explanation of type coercion in programming

## Q9 Explain data types, using examples from the JavaScript programming language

Provides a thorough explanation of data types in programming

## Q10 Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language

Demonstrates an extensive ability to manipulate arrays

## Q11 Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language

Demonstrates an extensive ability to manipulate objects

## Q12 Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language

Demonstrates an extensive ability to manipulate JSON

## Q13 For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes

Demonstrates an extensive ability to recognise functions, ranges and classes
implied thing in lesson, explain that code, dont do anything else to it

## References

### Q1

### Q2

### Q3

Amankwah, K 2023, 'MERN Stack Project Structure: Best Practices', viewed 6 April 2024, https://dev.to/kingsley/mern-stack-project-structure-best-practices-2adk#:~:text=The%20MERN%20stack%20project%20structure%20is%20organized%20in%20a%20way,application%20into%20three%20main%20components.
Duggal, N 2024, 'What is MERN stack? All you need to know', viewed 6 April 2024, https://www.simplilearn.com/tutorials/mongodb-tutorial/what-is-mern-stack-introduction-and-examples

### Q4

### Q5

### Q6

### Q7

### Q8

### Q9

### Q10

### Q11

### Q12

### Q13

