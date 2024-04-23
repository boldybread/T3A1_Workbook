# T3A1 - Workbook

## Q1 Provide an overview and description of a standard source control process for a large project

Large projects tend to be worked upon by many developers as well as having many features all being worked on simultaneously that potentially will change other functionality and potentially introduce bugs into the code. Therefore there needs to be a robust system in place that can control versions of the code to enable multiple people working on it at once without disrupting each other as well as offering the option to revert back to a previous version in case of catastrophic errors being introduced.

I will discuss and compare two source control solutions that are typically used on large projects, mono-repo and multi-repo.

### Mono-repo

Mono repo or Monolithic Repository is the process in software development where all components of a project is stored in one repository. This is in contrast to the more traditional approach of having multiple repositories for different components (Multi-repo). Mono-repo setups store all relevant and related code including libraries, modules, applications, etc in one version control system for instance within Git repository. This can include both frontend and backend.

#### Advantages of Mono-repo

- Atomic commit & easier refactoring
Since all developers share the same codebase it is easier to be consistent with the code

- Unified Versioning
All components will be using compatible versions of libraries and dependancies

- Flexible Collaboration
As all developers have access to the same code this allows simplified collaboration promoting knowledge sharing and easier code reviews.

- Easier Integration Test
CI and CD pipelines can be set up more efficiently allowing any changes to any part of codebase to start automated tests and deployments for the entire repo.

### Multi-repo

Transversely Multi-repos (multiple repositories) are the approach of developing each part of a project in a separate repository. Each component uses its own independent version control system. Each repo contains its own codebase meaning frontend applications and backend services as well as libraries, scripts and documentation are all kept in separate repos.

#### Advantages of Multi-repo

- Ease of access
With different components being operated independently it is easy to access the particular code for the relevant feature you are trying to work on. This can promote cleaner codebases and more modular development practices.

- Ownership
The decentralisation allows different individuals or teams to have clear ownership over a certain feature or components which is particularly useful in very large projects.

- Flexibility
It is easy for different teams to employ different languages or technologies in their approach to their project component allowing for innovation and experimentation.

- Scalability
Multi-repo projects are useful for scaling along with the project as the codebase grows as new repos can be added at any point without impacting existing ones.

## Q2 What are the most important aspects of quality software?

To create a high quality application there are several characteristics that are important to aim for to make sure we are delivering robust code to a high standard resulting in a great product and user experience.

### Reliability

Reliability is how well software can run effectively over a period of time without experiencing bugs or degradation of any kind.

### Maintainability

Maintainability is the ease at which software and its code can be maintained during its period of use. This becomes harder and more complex as the code size increases as well as the code increasing in complexity or decreasing in consistency. Maintainability needs to be assessed by automated testing as well as human reviewers therefore it is vital that the code is testable and easy to understand.

### Testability

Which brings us on to testability which is how testable code is.

### Portability

Portability refers to how easily or well the software can be used in different enviroments such as on different platforms etc. Portability can be hard to measure but we can ensure portable code by testing on different platforms throughout the developement cycle, rather than waiting until the end of development. Coding standards help with portability.

### Reusability

Reusability is how easily reused the existing code is.

### Security

Sec

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

An array in JS is a variable that is used to store data types for example:

```js
let arrayName = ["Brad", 2, 37, true];
/* let declares variable - different datatypes allowed */
```

There are many different methods useful for manipulated an array in various ways, we will look at some of the more commonly used ones here. For instance an array can be converted to a string by either the toString() method or the join() depending on whether you want the string to be separated by a comma or something else. We can also use the concat() method to combine two arrays together.

```js
let arrayName = ["Brad", 2, 37, true];

console.log(arrayName.toString()); // Brad,2,37,true
```

```js
let arrayName = ["Brad", 2, 37, true];

console.log(arrayName.join('-')); // Brad-2-37-true
```

```js
let firstArray = [1, 2];
let secondArray = [3, 4, 5];

let combinedArray = firstArray.concat(secondArray);
console.log(combinedArray); // [1, 2, 3, 4, 5]
```

### Adding/Removing Items from an Array

We can push() to add an item to the end of an array or pop() to remove the last item from our array. Using shift() we can remove the first item from a list and return it or with unshift() we can add an item to the start of the array.

```js
let myAnimals = ["bear", "wolf", "dog"];
myAnimals.push("koala", "lion"); // add these two to the end of the array
console.log(myAnimals); // ["bear", "wolf", "dog", "koala", "lion"]

myAnimals.pop(); // "lion" 
/* Removes "lion" and returns it*/
console.log(myAnimals) // ["bear", "wolf", "dog", "koala"]

myAnimals.shift(); // "bear"
/* Removes the first item "bear" from the array and returns it */
console.log(myAnimals) // ["wolf", "dog", "koala"]

myAnimals.unshift("bear");
/* adds "bear" to the start of the array and changes the original array */
console.log(myAnimals) // ["bear", "wolf", "dog", "koala"]
```

Alternatively we can use splice() to change an array by adding, removing or inserting elements. the method slice() will allow a developer to copy and return a section of an array without changing the original array.

```js
let team = ["fred", "gary", "kate", "lucy", "max"];
team.splice(0, 3); // deletes ["fred", "gary", "kate",]
/* 0 represents the index to start removing from, the 3 is how many elements to delete */
console.log(team); // ["lucy", "max"]
```

```js
let team = ["fred", "gary", "kate", "lucy", "max"];
team.splice(5, 0, "Joel", "Ella", "Rose"); // adds "Joel", "Ella", "Rose"
/* 5 represents the index to start from, the 0 is how many elements to delete, because this delete count is 0 we add the following items at index [5] */
console.log(team); // ["fred", "gary", "kate", "lucy", "max", "Joel", "Ella", "Rose"]
```

```js
let nums = [1, 2, 3, 4]
let newNums = nums.slice(0, 3)
/* selects and returns elements between index [0] and [3] not including the [3] index which is the element 4 here to a new variable we have created */
console.log(nums) // [1, 2, 3, 4]
console.log(newNums) // [1, 2, 3]
```

## Q11 Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language

Accessing object properties can be done with either dot notation or bracket notation.

```js
var bands = {
    name: "Spiritbox",
    genre: "Metal",
    country: "Canada",
    members: 4
};

console.log(bands.country); // Canada
/* dot notation - objectName.propertyName*/

console.log(bands['country']); // Canada
/* bracket notation - objectName['propertyName']*/
```

To manipulate objects in JS we use object methods which are properties containing a function definition such as:

### Object.values()

A developer uses object.values() when they need to return an array containing the object's own values.

```js
var bands = {
    name: "Spiritbox",
    genre: "Metal",
    country: "Canada",
    members: 4
};

var vals = Object.values(bands)
console.log(vals); // [ 'Spiritbox', 'Metal', 'Canada', 4 ]
```

### Object.keys()

Object.keys() can be used by a developer when they want to return an array of an objects' own properties.

```js
var bands = {
    name: "Lorna Shore",
    genre: "Deathcore",
    country: "US",
    members: 5
};

var keys = Object.keys(bands)
console.log(keys); // [ 'name', 'genre', 'country', 'members' ]
```

### Object.freeze()

Objects can be frozen with Object.freeze() which prevents any properties being added or removed from them. Object.isFrozen() can be used to see if an object is frozen.

```js
var bands = {
    name: "The Amity Affliction",
    genre: "Metal",
    country: "Australia",
    members: 5
};

Object.freeze(bands);
console.log(Object.isFrozen(bands)); // true
```

### Object.seal()

Similarly to Object.freeze(), Object.seal() will also prevent you from adding or removing properties to an object, however it differs because you can still change the values of an already existing property. Using Object.isSealed() will check to see if the object is currently sealed.

```js
var bands = {
    name: "Make Them Suffer",
    genre: "Metalcore",
    country: "Australia",
    members: 5
};

Object.seal(bands);
console.log(Object.isSealed(bands)); // true
```

## Q12 Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language

A developer can manipulate JSON in JS by adding or modifying properties within JS objects by parsing JSON. As discussed in the previous question properties can be modified by either dot or square bracket notation.

```js
var bands = {
    name: "Spiritbox",
    genre: "Metal",
    country: "Canada",
    members: 4
};

/* To access any of this data we can use dot notation*/
console.log(bands.name) //Spiritbox
console.log(bands.members) //4

/* We can also use square bracket notation*/
console.log(bands['name']) //Spiritbox
console.log(bands['members']) //4
```

### JSON.stringify()

One useful function at the disposal of developers is the stringify() function which allows us to convert an object into a JSON string. This enables us to move data from a client to a server in an easy lightweight way.

```js
var bands = {
    name: "Spiritbox",
    genre: "Metal",
    country: "Canada",
    members: 4
};

var bandString = JSON.stringify(bands)
console.log(bandString); //{"name":"Spiritbox","genre":"Metal","country":"Canada","members":4}
```

### JSON.parse()

Suppose we have transported our JSON string and we need to now convert it back into a JSON object, we do that using the JSON.parse() function. Lets look at our example from above again and convert bandString back to a JSON object.

```js
var bandObject = JSON.parse(bandString)
console.log(bandObject); //{ name: 'Spiritbox', genre: 'Metal', country: 'Canada', members: 4 }
```

## Q13 For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes

```js
// Define CAR class
class Car {
    // Constructor to initilise car BRAND
  constructor(brand) {
    this.carname = brand;
  }
  // Method PRESENT returns a string "I have a" combined with the brand of car owner by user
  present() {
    return 'I have a ' + this.carname;
  }
}

// Define MODEL class that extends CAR
class Model extends Car {
    // Constructor to initialise BRAND, MODEL of CAR
  constructor(brand, mod) {
    // Call the constructor of the parent class CAR with the brand parameter
    super(brand);
    this.model = mod;
  }
  // Method to return STR concatnating PRESENT string with "it was made in" + MODEL
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

// declare array of car MAKES
let makes = ["Ford", "Holden", "Toyota"]
// declare array of car MODELS from 1980 to 2019
let models = Array.from(new Array(40), (x,i) => i + 1980)

// Function to generate a random integer between a given range
function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

// Loop through each MODEL in MODELS array
for (model of models) {

// Randomly select a MAKE from the MAKES array
  make = makes[randomIntFromInterval(0,makes.length-1)]
// Randomly select a MODEL from the MODELS array
  model = models[randomIntFromInterval(0,makes.length-1)]

// Create an instance MYCAR using the MODEL class with a random MAKE and MODEL
  mycar = new Model(make, model);
// Display MYCAR
  console.log(mycar.show())
}
```

## References

### Q1
Safari, H 2020, 'How to use version control systems in large & multi-part software projects?', viewed 23 April 2024, https://www.linkedin.com/pulse/how-use-version-control-systems-large-multi-part-software-hadi-safari/

### Q2
Bellairs, R 2019, 'What Is Code Quality? Overview + How to Measure Code Quality', viewed 23 April 2024, https://www.perforce.com/blog/sca/what-code-quality-overview

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

Ayodeji, B 2019, 'How to Manipulate Arrays in JavaScript', viewed 23 April 2024, https://www.freecodecamp.org/news/manipulating-arrays-in-javascript/

### Q11

Codehouse Dev Team, 2022, 'How to use object mainpulation in JavaScript', viewed 23 April 2024, https://www.codehousegroup.com/au/insights/how-to-use-object-manipulation-in-javascript

### Q12

Tagliaferri, L 2022, 'How to use object manipulation in JavaScript', viewed 23 April 2024, https://www.digitalocean.com/community/tutorials/how-to-work-with-json-in-javascript