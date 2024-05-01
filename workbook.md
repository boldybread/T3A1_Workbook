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

Reliability is how well software can run effectively over a period of time without experiencing bugs or degradation of any kind. Effective code should be both predictable and reliable so that the code produces expected results without producing errors or crashing. Thorough testing allows us to ensure reliability.

### Maintainability

Maintainability is the ease at which software and its code can be maintained during its period of use, it needs to be both functional and supportable over time. This becomes harder and more complex as the code size increases as well as the code increasing in complexity or decreasing in consistency. Maintainability needs to be assessed by automated testing as well as human reviewers therefore it is vital that the code is testable and easy to understand. The more modular code has been written the easier it is to separate and change things without affecting or breaking the rest of the code.

### Testability

Which brings us on to testability which is how testable code is. We need to be able to write automated tests that verify our code is producing expected results without crashing or producing errors. Testing should be an integral part of our development process and should ensure that any issues or potential issues can be quickly identified and rectified.

### Portability

Portability refers to how easily or well the software can be used in different enviroments such as on different platforms etc. Portability can be hard to measure but we can ensure portable code by testing on different platforms throughout the development cycle, rather than waiting until the end of development. Coding standards help with portability.

### Reusability

Reusability is how easily reused the existing code is. If we write code with properly defined interfaces it can be reused in future projects or features. Again modularity in code makes is a preferred practice as this also makes your code more reusable.

### Security

Security even though I have listed it last is potentially the most important aspect of quality software, in this day and age there is more vulnerabilioties than ever so ensuring our users have protected data is critical. Secure coding practices are essential to avoid data breaches and unauthorised access.

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

A team would require the knowledge of whatever the small business' customer base is and what the product is that they are trying to sell. Is the business trying to reach more customers or make it easier/more accessible to acquire their services/product. With this knowledge you can tailor the website to focus around that product or service. How intuitive or interactive does it need to be? Another knowledge condisderation is the values the business has and what image they are trying to project on their website. Will they require a sleek corporate website to impress higher end clientele, will they want a colourful interactive page to attract families?

Other than these customer requirements the important knowledge and skills required for a team of web developers include the following:

### Communication

Perhaps the most important skill required of a developer especially a team of devs is communication skills. This is required specifically when working together on a large project, maybe the individual devs are building separate features but those features need to function with each other therefore it is imperative that the team is communicating and using the same coding standards and practices as well as appropriate testing at each step of the development to ensure seamless results. Of course as discussed previously the first knowledge the team should be discovering is exactly what the client wants built for their company, if the team has poor communication they will struggle to engage the client and learn exactly what they are hoping to be delivered to them at the end.

### Version Control

We have discussed previously version control practices so it is easy to see why this would be essential knowledge and skills for our team of devs. The bigger the team the more separate features that are going to be built across different repos, without appropriate knowledge of how to use version control the development is going to be slow and riddled with compatibility errors. A well organised team will have seamless version control practices allowing a senior dev an easier time monitoring, managing and modifying any new features, codebases or changes to the project. Version control also allows the senior dev the option to reject changes or revert to previous versions so that all work is not lost.

### Software Testing

Software testing will be of key importance to the team of web devs as the client will expect a robust finished product that will work as required over the period of time that it is expected to perform as such. The devs will need to ensure that enough testing is carried out that any potential bugs or errors can be found and rectified before users start using the product as otherwise this can cause damage to the customer's company and therefore the development team's reputation. Good software testing should require a mix of both manual testing and automated testing to really push and test the limits of the product.

### Coding Skills

One obvious fundamental skill set required by any web dev team will be coding skills. Both frontend and backend may be needed for the project so there needs to be a range of those skills in the team either with full stack devs or frontend/backend specialists. All devs should be familiar with which ever tools are used by the team such as VS Code, Git, Github etc, and there needs to be a solid grasp of whichever programming language is required whether that be a frontend one like HTML/JS, or a backend one like Python or Ruby.

### Problem Solving

The team will require solid problem solving skills, any web dev project can be challenging and require the solution of complex problems depending on the complexity and requirement of the website to be built. The devs require an analytical mind to allow for optimizing and debugging the code that they are producing.

### Time Management

Time management is another often overlooked skill that needs to be a core attribute to a web dev team. Usually a ssenior dev will be in charge of the project management to make sure the team is keeping up with timelines as they hit milestones. They will understand the expectations of the client when it comes to completion time of the project. Whilst a overly complex website will take more time there will still be an expectation from a customer to have a completed finished product within a reasonable time.

## Q5 With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges

In my Portfolio project I built a webpage communicating my personality, skills and projects to a prospective client. This required web development skills, in particular HTML and CSS. I would have liked to have some JS experience for this but I didn't have any at the time of the project. HTML skills allowed me to create the structure of the website as well as the content. CSS allowed me to style those pages and change the layout to how I wanted it, CSS also helped me create a webpage with responsive design, it was important to me to create something that could be viewed properly on a desktop, a phone, or a tablet which was a challenge I had to overcome. I had to design and code the website to allow for different screen sizes using CSS media queries to make sure the webpage looked good on any screen.

Another skill I had to utilise was version control, I used github, this allowed me to commit changes along the way in the project this helped me manage and track the changes I was making in case of introducing bugs or errors. Github also offers another platform to showcase my talents to a would be client. I had to have some knowledge of typography principles to help style fonts on the website. To make my portfolio accessible I needed to host the website, this was a challenge as I had never done this before, but I was able to use Netlify to help me host the portfolio which was simple to use.

Some of the soft skills that were required for this project were:

- Creativity
Coming up with something attention grabbing, unique that showcased my skills.

- Attention to detail
Avoiding typos or other small mistakes, making sure alignment and spacing was correct

- Time management
I had to make sure I was efficient with my time as I only had two weeks to create it so I needed to make sure I worked on different aspects of the website without getting too caught up on one aspect.

- Communication
With communication being such a vital skill in the coding world I needed to make sure that I was communicating my knowledge and skills effectively in my portfolio to attract a potential client.

## Q6 With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature

In my Portfolio project I built a webpage containing my resume and various projects I had completed such as a blog with the aim of showcasing my talents as a developer to a would be client. The website was built using HTML and CSS and at the time those skills were very limited as I was new to coding. If I was to tackle the project now I would be able to better achieve my vision on the website, for instance the image on my home page was designed to change size depending on the screensize viewing the page, but I struggled with keeping the image centered on different screensizes as they changed. Now with my knowledge of CSS I would be able to fix this without issue for instance by using Bootstrap CSS which is a CSS framework designed to help develop in HTML JS & CSS.

Also at the time of working on the portfolio I had no knowledge of JS at all, I really wanted to have a typewriter effect on the homepage and it was difficult for me to do without the JS knowledge and I couldnt get it quite right. With my current JS knowledge I would not only be able to fix this but also improve the interactivity of the website by employing more JS and improving the usability and functionality. I would be able to add animations and effects to my website that wouldn't otherwise be possible. I could dynamically update content on my website without reloading the entire page, this would allow me to create a news feed or chat application rather than the generic contact form which was all I was able to create on my original portfolio without the use of JS.

I hosted my website through Netlify, I now know how to easily host a website through github so I would use that if I was to recreate this project.
Lastly I feel with my current knowledge and skills I could improve the efficiency of my website optimizing performance by using techniques such as efficient selectors, minimising CSS file size and leveraging CSS sprites as well as simply reducing any redundant code.

## Q7 Explain control flow, using an example from the JavaScript programming language

Control flow is how a computer runs code, generally from top to bottom unless it encounters a statement that will change the control flow for instance loops, conditionals or functions. It is essential for a developer to understand how a computer will interpret code and the order in which it will do so to make sure your code is achieving what you want it to.

### Loops

Loops are statements that cause the program to iterate through and keep running until a condition becomes false, or there is nothing left to loop over.

```js
const favouriteFruits = ["Blueberries", "Pears", "Plums", "Peaches"];

let text = "";
for (let i = 0; i < favouriteFruits.length; i++) {
  text += favouriteFruits[i] + " are yum! ";
}

console.log(text)
// Blueberries are yum! Pears are yum! Plums are yum! Peaches are yum! 

```

### Conditionals

Conditional statements such as if, else, else if and switch statements can be used to control the flow in JS. The code will continue running while that condition is met or not met. For instance:

```js
hungry = true
if (hungry == true) {
 console.log('We are hungry! lets eat something!');
}
else {
  console.log('We are full!')
}
// We are hungry! lets eat something!
```

By making variable hungry = true we have controlled the flow forcing the code to produce the desired outcome "We are hungry! lets eat something!"

### Functions

Lastly functions are blocks of code that can be called usually taking in one or more arguments and optionally returning a value.

```js
let sum = myFunction(2, 3);

function myFunction(a, b) {
// Function returns the sum of a and b
  return (a + b);
}
console.log(sum) // 5
```

All of these statements discussed effect control flow because they pause the flow of code execution until the conditions are met.

## Q8 Explain type coercion, using examples from the JavaScript programming language

Type coercion is the automatic conversion of values of a particular data type to a different data type and is vital in programming when handling different data types, when comparing values or when performing operations. Javascript will attempt to make data types compatible by using type coercion in order to complete an operation or comparison.

```js
var num = 9001;
var str = "My power level is " + num; // JavaScript uses type coercion to change number to string
console.log(str); 
// "My power level is 9001"
```

```js
console.log(9001 == "9001"); // JS has used type coercion to convert string to number to enable comparison
// true
```

Javascript follows a set of priorities and rules when performing type coercion:

- Numeric Values that are concatenated with str using "+" operator will be automatically coerced from num to str.

- Str values involved in arithmatic operations will be converted automatically to numerical values

- Comparing values with loose equality/inequality ("==" / "!=") operators JS will attempt to automatically coerce the values to make it comparable. Avoid this by using True equality "===".

- Falsey values include false, 0, null, undefined, NaN and empty str.

As opposed to type coercion which is the automatic conversion of values by JS, there is also type conversion which is the explicit converting of value's data types. In other words the developer is intentionally forcing the data type to change by using inbuilt functions or operators of JS. Both type conversion and type coercion have a place in coding and it is important for a developer to understand how their code will react once run. Will there be an implicit conversion that takes place automatically? Will the code not run due to different data types so we might need to force the change explicitly? This is crucial for writing efficient and predictable code that performs operations accurately and as expected.

## Q9 Explain data types, using examples from the JavaScript programming language

There are 8 different data types used in JavaScript programming language which I will discuss below:

- String
Strings or str are simply a series of one or more characters created by using single or double quotes at the beginning and end of the str. The quotes need to match, and if a quotation mark exists in the str then the other sort of quotes must be used.

```js
let strExample = "String using double quotes";
let strExample2 = 'String using single quotes with a "quotation mark" included';
```

- Number
Numbers in JavaScript are stored as decimal numbers and can be written either with or without decimals

```js
let numExample = 7;
let numExample2 = 7.00;
```

- Bigint
JS numbers are stored in 64 bit floating point format which means that certain very large numbers are simply to big to be represented by a normal JS number, so thats where Bigint comes in. BigInt enables very large numbers to be stored in JS. BigInt cannot contain decimals.

```js
let hugeNumber = BigInt("123456789012345678901234567890");
```

- Boolean
Booleans are either true or false, that is their only 2 values.

```js
let coolAnimal = "Wolf";
let favAnimal = "Wolf";
let petAnimal = "Dog";
console.log(coolAnimal == favAnimal)       // true
console.log(coolAnimal == petAnimal)       // false
```

- Undefined
Any variable without a value in JS is undefined as a data type and has the value undefined. Setting the value of a variable to undefined will empty that variable.

```js
let thinkOfSomethingWitty; // This is undefined as we haven't given a value to variable
console.log(typeof thinkOfSomethingWitty);
// undefined

let somethingElseWitty = "Witty!"; // Variable has value
somethingElseWitty = undefined // We then empty variable by setting value to undefined
console.log(typeof somethingElseWitty);
// undefined
```

- Null
Where undefined is a variable or object that has not been defined, null represents a value that has been intentionally given a null value. It is often used to indicate that an object does not exist or that a variable has no value.

```js
let firstName = "Brad"
let middleName = null
let lastName = "Archbold"
```

- Symbol
Symbols are used to add unique property keys to an object and they are immutable. Symbol() will return a unique symbol every time.

```js
let symbolEx1 = Symbol();
let symbolEx2 = Symbol();
let symbolEx3 = Symbol();
// These 3 variables will all contain unique symbols
```

- Object
Objects are written with {} and are written as name:value pairs

```js
const person = {firstName:"Brad", lastName:"Archbold", age:36, eyeColor:"blue"};
console.log(person) //{ firstName: 'Brad', lastName: 'Archbold', age: 36, eyeColor: 'blue' }
```

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
Javaid, N 2023, 'The Key Qualities of Good Programming Code', viewed 23 April 2024, https://www.linkedin.com/pulse/key-qualities-good-programming-code-nabeel-javaid/

### Q3

Amankwah, K 2023, 'MERN Stack Project Structure: Best Practices', viewed 6 April 2024, https://dev.to/kingsley/mern-stack-project-structure-best-practices-2adk#:~:text=The%20MERN%20stack%20project%20structure%20is%20organized%20in%20a%20way,application%20into%20three%20main%20components.
Duggal, N 2024, 'What is MERN stack? All you need to know', viewed 6 April 2024, https://www.simplilearn.com/tutorials/mongodb-tutorial/what-is-mern-stack-introduction-and-examples

### Q4

LinkedIn 2024, 'You're a web developer and you want to be successful. What skills do you need to have?', viewed 24 April 2024, https://www.linkedin.com/advice/1/youre-web-developer-you-want-successful-what-skills-xxnfe

### Q7

Cleary, R 2020, 'Control Flow in JavaScript', viewed 1 May 2024, https://medium.com/@rianna.cleary/control-flow-in-javascript-9c63d0c98bb9#:~:text=Control%20flow%20in%20JavaScript%20is,loops%2C%20conditionals%2C%20or%20functions.

### Q8

Jha, A 2023, 'Understanding JavaScript: Type Coercion & Type Conversion', viewed 1 May 2024, https://medium.com/@atuljha2402/understanding-javascript-type-coercion-type-conversion-a2ce84c00331#:~:text=Type%20coercion%20refers%20to%20the,complete%20the%20operation%20or%20comparison.

### Q9

W3 Schools, 'JavaScript Data Types', viewed 1 May 2024, https://www.w3schools.com/js/js_datatypes.asp

### Q10

Ayodeji, B 2019, 'How to Manipulate Arrays in JavaScript', viewed 23 April 2024, https://www.freecodecamp.org/news/manipulating-arrays-in-javascript/

### Q11

Codehouse Dev Team, 2022, 'How to use object mainpulation in JavaScript', viewed 23 April 2024, https://www.codehousegroup.com/au/insights/how-to-use-object-manipulation-in-javascript

### Q12

Tagliaferri, L 2022, 'How to use object manipulation in JavaScript', viewed 23 April 2024, https://www.digitalocean.com/community/tutorials/how-to-work-with-json-in-javascript