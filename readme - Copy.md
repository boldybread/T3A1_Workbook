# T2A1-A - Workbook

## Q1 Describe the architecture of a typical Flask application

Web Frameworks provide a simple standardised way of creating and developing web applications. Flask, which is a module of Python, is a popular framework allowing more intuitive development of web applications than simply using Python by itself. Ironically the origin of Flask was an April Fools Joke but the framework became popular amongst Python users and its wide spread adoption saw it become a staple web framework due to it being very simple and beginner friendly compared to other existing frameworks like Django, similar to how Python itself was a great beginner programming language because of its simplicity. Flask has often been referred to as a microframework as it has been made to be simplistic and does not require particular tools to operate.

### Flask Architecture

After installing flask python package on your system the developer is ready to start creating. Now the developer will create a Python file that will make the web application, typically app.py is the name used for the python file. Here the developer will import the class Flask from the flask module, which is then used to create a Flask object and pass the special variable "__name__" which holds the name of the current python module. Below this the developer will then create Flask routes which map URLs to a specific view by passing ```'/'``` to the decorator ```@app.route()```. Views are any callable, like functions, which receive a request and send a response back for that request.

Here is an example of some basic source code from a typical Flask application:

```py
# importing the Flask class from the flask module
from flask import Flask 
  
# Creating the object "app" belonging to the Flask class
app = Flask(__name__) 
  
# Pass the required route to the decorator that is linked to the view 'function()' 
@app.route("/route_name") 
# Define the function that will be called for this route
def function(): 
    return "Hello, welcome to route_name page!"
```

This Flask application is ready to be run and can be done so with the command ```flask run```. This will be run on port 5000 by default, if you go to the URL ```http://localhost:5000``` using your browser you would be able to see ```Hello, welcome to route_name page!```

## Q2 Identify a database management system (DBMS) commonly used in web applications (including Flask) and discuss the pros and cons of this database

PostgreSQL also know as simply postgres, is a widely popular database management system (DBMS) that is open and source and free that was initially released back in 1996. Postgres supports both SQL and JSON querying.

### Pros of using PostgreSQL

- Transactions
Database transactions are single units of work consisting of one or more operations, and it is vital that this work is completed at the same time to avoid errors. PostgreSQL transaction's are atomic and will always succeed or fail completely. This means the programmer doesn't need to add countless error handling code that would be required if you didn't have transactions.

- Code Comments
PostgreSQL allows for code comments. Like in many coding languages Code comments are extremely useful especially when working in a team because they will help you see at a glance the intent and functionality of a particular bit of code. This makes your code more readable allowing for easier maintenance or updating by yourself or others in your team.

- Parameters
Postgres has many adjustable parameters that can be set at different places using different methods. A lot of other database systems require you to set parameters at the whole database level. PostgreSQL allows for users to be able to change parameters exactly when they need to be changed.

- Extensions
Another pro to PostgreSQL is that it isn't fixed, it is highly extensible. Postgres was originally designed to be a simplistic core system to maintain efficiency with a modular design allowing for limitless adaptability with the addition of extensions. The functionality of extensions to add exactly what a user wants really sets Postgres apart from other databases where this is much more difficult. Extensions provide additional features, functions, data types and operators that can allow a user to build a database exactly matching their application's requirements.

- Security
Postgres has built in security features such as user authentication and host-based access control but also the extensions allow for even more enhanced security if required. Postgres offers database file protection, allowing files to be protected from reading by non authenticated users.

- Open Source
Postgres being open source means its code is freely available allowing users the freedom to use and modify it as they need for their application.

### Cons of PostgreSQL

- Database structure
Due to Postgres being a relational database system it can be more complex to set up and use than other DBMS for inexperienced users.

- Open source
Being open source is also a con as it isn't owned by one particular organization but instead is community run. Despite being such an excellent platform compared to many DBMS it has had trouble getting its name out there and it does not come with a warranty and has no liability or indemnity protection unlike other DBMS.

- Slower performance
As Postgres has been designed for compatibility rather than speed users will have to put more work in to optimising their applications for speed improvement. Postgres is slower that other DBMS such as MySQL. PostgreSQL's query process begins with the first row then reads through the entire table to find the relevant data then again with the second row and so on, resulting in slower performance especially with larger databases.

Overall Postgres is a fantastic DBMS that is highly compatible offering many features thanks to its support of extensions with great security that has made it popular with a lot of Python faithful, but its slower performance and complexity for inexperienced users have given some limitations to its use.

## Q3 Discuss the implementation of Agile project management methodology

Where Traditional project management (PM) involved focussing on goals then moving on from the goals without going back, Agile PM involves breaking a project up into smaller phases (known as sprints) and once you meet a goal you can review and improve it many times throughout the rest of the project. Agile PM supports returning to older phases of the project to update and improve features based on new requirements or data. We can think of agile PM like iterations.

### Stand-ups

Stand-ups are a commonly used Agile PM technique used by teams to check in and communicate on progress. They should be short to discuss blockers and progress. Team members can bring up challenges in their work that the team can troubleshoot, or share successes that can inspire other team members or help them to avoid pitfalls in similar work. 

Stand-ups shouldn't be complicated. Atlassian uses 3 simple questions for theirs:

- What did I work on yesterday?

- What am I working on today?

- What issues are blocking me?

These help flag challenges and highlight the teams progress. This can keep the team motivated by sharing the progress and individual successes.

### Kanban

Kanban is another methodology in our agile PM arsenal which allows a team to visualise the project by sharing all tasks to all members. Commonly using columns such as tasks to be started, in progress, completed tasks as well as optionally columns for reviewing or troubleshooting. This method gives a clear focus to the whole team of every aspect of the project allowing everyone to see if there is a backlog of tasks or work that needs reviewing, giving teams greater flexibility and transparency.

### Sprints

Sprints are the iterations that put the agile into agile PM. Sprints need to be clearly defined by ensuring the team all is aware of the sprint duration, making sure the to do list of the sprint is clear and manageable by the team in the given time, and that the members responsible for each task on that to do list are aware of exactly what their role is and how it is to be completed. Sprints can be used in conjunction with kanban boards. Combining these techniques involves a team focusing on just the "in progress" column for each sprint rather than looking at the "to be started" tasks as well as the "in progress" one allowing more focus and better more manageable time management. Another technique is sprint retrospectives, which are similar to stand ups except they only happen at the end of each sprint which improves team cohesion, and again helps avoid pitfalls in future sprints by making everyone aware of certain problems that can be run into.

### User Stories

User stories are a method of talking out the problem you are trying to solve. A developer will put themselves in the shoes of various customers of the project's target audience and answer questions based on certain functionality or abilities that they want the application to be able to do. This can help inform what features might be needed for the best possible application to be built. User stories allow you to make certain assumptions about a user and their needs and wants which will help shape the final product.

### Task Prioritisation

Task prioritisation is really important in agile PM as this is a means to assign an order to tasks or an estimation of time to complete tasks which can be really helpful for keeping the team on track and knowing if they are ahead or behind schedule. This can also separate vital tasks from nice to have tasks in the even that time does run out it is more important that certain tasks have been completed over others.

## Q4 Provide an overview and description of a standard source control workflow

Coders often work as part of small or large teams to build upon code together to create or maintain software. Multiple people updating code at the same time is obviously problematic, and no team wants to start over again if someone's code bugs out the whole application, so this is where source or version control comes in. Coders needed a way of controlling code that was being updated by potentially multiple people simultaneously as well as offer the capability of undoing the damage so to speak and reverting to an older version.

Trunk-based development is one of the most popular version control methods which involves coders working on small parts of an application's code, and merging that frequently with the main branch or "trunk". This continuous integration ensures the project moves along at an optimum pace as it reduces the time developers would be waiting for other coders to complete work, so ultimately the project will be completed quicker and more efficiently.

Due to the small size of the frequent commits trunk-based development is easy to review as senior developers can quickly and efficiently review these small updates to the code, again improving that continuous integration and overall efficiency.

The practice of trunk-based development is built upon frequent consistent commits therefore it is best practice to develop small batches of code and committing them daily to the main branch. These small batches of code also promote a quicker review process as senior developer can easily see the desired effect in a few lines of code and troubleshoot or approve as necessary.

Another standard practice is using feature flags which are if-statements that allow a certain feature to be turned on or off, this reduces the chance of code errors effecting the whole application when many coders are working on a project at once. This again improves the speed and efficiency of the project.

Another practice that has become standard to achieve continuous integration is the implementation of automated testing. Automated testing works smoothly with trunk-based development by checking the small batches of code that have been committed to the main branch and approving or denying them automatically depending on whether there are any issues or not. As you can see this would greatly speed up the process as it doesn't rely on a senior developer having to review and approve every small change to the project. These immediate approvals ensure the developers can move straight on to the next bit of code they want to work on, and that other coders are always working on the most updated code. It also means senior developers are free to focus on optimising the code rather than wasting time fixing up incorrect code.

Best practice in trunk-based development involves deleting branches after a merge has been completed. We want to aim to have three of fewer active branches in the project's repository. If developers are ensuring they are completing daily merges to the main branch there is no reason to keep old branches around that have become inactive.

## Q5 Provide an overview and description of a standard software testing process (e.g. manual testing)

Automated testing has become standard practice for the modern developer team as it promotes continuos integration and efficiency. Automated testing is the process of coding software to automate the process of validation and review of a product being built. Before automated testing everything was manually tested by a team of developers, this process was obviously slow, expensive as you had to employ additional developers and likely to have mistakes due to human error. Automated testing has improved on all those downsides to manual testing, and while there is still a time, place and need for manual testing, generally automated testing makes up the bulk of all reviews of code throughout a project for most modern agile and DevOps projects.

Automated testing means there is no need to have a team of developers hired for testing, or a senior developer wasting their time looking for errors in code when instead their time can now be spent optimising that code or on other more important things. As the standard for modern developers is Continuous Delivery (CD) which is about providing a fast and consistent way for code to be delivered, automated testing is critical to achieving this. A program can check for errors in code almost instantly and approve or deny a merge request which greatly speeds up the process without wasting human hours on this task.

Most tests that can be automated should be automated due to the gain in human time saved and increase in speed and productivity. Types of testing that are usually automated include End to End (E2E) tests, unit tests, integration tests and performance tests. E2E tests are designed to simulate a human user accessing the application such as logging in and making a transaction then logging out. The purpose of this is to ensure that potential users are having a smooth experience without encountering bugs. If the team is doing daily commits automating these tests is highly efficient as after every single commit we can see if we have introduced any errors or bugs. Unit tests are for testing individual functions ensuring that a specific function is producing a specific result, with these automated it is both fast and inexpensive to run multiple times and record the results.

Integration tests are designed to see how well the application works with a third party that may not have access to all of our code, and performance tests are to measure the responsiveness and speed of the code when it is performing various functions. Automating these processes again improves efficiency and saves in human time.

## Q6 Discuss and analyse requirements related to information system security and how they relate to the project

This project is a web application that will hold personal data of users as well as other information that would be enticing for potential malicious groups or other cyber threats therefore we must discuss information system security requirements to prevent breaches and unauthorised access to our software. We must first decide what data we will be storing on our web application to decide what security measures will be in place. Security will be a key part of the development process from the very beginning of the build allowing us to check for threats and vulnerabilities at every step of the build. According to Cyber Security Specialists: 'Risk Optics' the essential component of information security management is to "protect the integrity, confidentiality, and availability of your IT assets." (June 29, 2023, https://reciprocity.com/resources/what-are-information-security-controls/)

### Confidentiality

Our first priority is to maintain user's confidentiality, any sensitive data that they provide for our web application is to only be accessed by any authorised users. Depending on the more sensitive the data, the more likely cyber threats are, but regardless there has to be systems in place to protect that user's information. Access controls making sure that all users have assigned certain level of privileges and data can only be accessed if you have the appropriate privileges for the appropriate circumstance. Encryption will also be useful in protecting the data by converting the information into cipher text using modern cryptographic processes, this will work hand in hand with the access controls as only those authorised users will be able to decipher and access the plain text information. We will design the application to deny access by default and validate permissions on every request as well as regularly review permissions to decrease the risk of a breach. Regular security audits during the build of the application will help test these access controls and encryption for instance with End to End automated testing mimicking potential users as well as potential threat actors trying to access that information. We will enforce complexity requirements for passwords and also require sign in with Multi Factor Authentication to further increase security as passwords are often a potential vulnerability in many software systems. Passwords will be stored cryptographically rather than as plain text, we will also disable access after multiple incorrect login attempts. 

### Integrity

We must make sure the data in our application also stays accurate and unaltered unless requiring modification. Preventing unauthorised access should mostly take care of this, but we will also need to ensure that we have appropriate backups of the data as well as secure storage to protect from any unauthorised changes or from data corruption. Also depending on the type of data we are holding will dictate whether we have any legal requirements to follow or regulation compliance. Our data type will help shape our security policy. Again automated testing will help monitor for integrity vulnerabilities as well as good coding practices such as appropriate error handling and logging to minimize bugs with the potential to create vulnerabilities in the application and also threat modelling to search for potential areas that are susceptible to cyber attack. 

### Availability

Finally we must make sure that our data is always accessible by any authorised users as it is needed. Secure backup and recovery solutions will be pivotal in the reliability and availability of our data ensuring that our data is encrypted during transmission between different components of the application. We will utilise protocols like HTTPS to utilise its encryption between the web server and user's browser. Using automated testing will reduce the chance of human error which lowers our risk of disruptions, failures or unauthorised attacks that might deny our service.

## Q7 Discuss common methods of protecting information and data and how you would apply them to the project

We will use certain information security controls to protect data and information in this project. Access controls will prevent access to unauthorised users ensuring only users with a requirement to access information will be able to do so. We will apply a password system enforcing complexity and utilising multi factor authentication to further protect that access control. Passwords will be stored cryptographically rather than as plain text.

Encryption will be utilised for the transfer of all information within our project's application, as well as for storing backups of the information. This will protect the data in the case our access controls fail. Utilising automated testing will help minimize vulnerabilities by reducing human error and fixing bugs in the code to prevent coding errors with the potential to be exploited by attackers. Appropriate error handling and logging will further discover bugs with the potential to create vulnerabilities before they cause a significant issue.

Using the principle of least privilege is a method that will also help protect our data. We will validate permissions each time a request is made, review permissions periodically as well as create tests to validate permissions and by default deny access to the data in the application.

We will also utilise tools such as Static Application Security Testing (SAST) to analyse our source code for security. Static code analysers search for both vulnerabilities as well as for compliance with coding standards. The earlier in the development phase of the web application that we find these vulnerabilities the more time we will have to fix and secure the application.

## Q8 Research what your legal obligations are in relation to handling user data and how they can be met for the project

The Privacy Act 1988 is the legislation in Australia that protects individual's personal data inclusive of collection and disclosure as well as use and storage of that information. Part of this act is the notifiable data breaches scheme where in an entity responsible for a breach must inform the individual whose data has been affected that the breach has taken place. As an individual you have the right to know why personal data is being collected, as well as who it will be disclosed to and what it will be used for. Individuals also have the option of being anonymous as well as the right to ask for their personal data, or to ask for incorrect data to be corrected. Businesses with an annual turnover of more than $3 Million AUD are bound by the Privacy Act 1988, as well as small businesses such as health providers, credit reporting body, residential tenancy, or a business that buys or sells personal information.

To meet these obligations we first must decide what personal information we will be collecting, personal information can be names, details such as address or telephone number, medical records, bank details, photos, or IP Addresses to name a few of the main ones. If we are collecting any of that information for our project we must take steps to ensure we are handling them in compliance with Privacy Act 1988 and if there was to be a breach we must notify the individual. Steps to ensure compliance include making sure users are aware of our privacy policy and we need to be clear in that exactly what we will use the information for. We must also make sure that access to that information remains open to the user, as well as giving them the opportunity to correct any personal information about them.

The 'Consumer Data Right' is part of the Competition and Consumer Act 2010 and this gives businesses strict requirements on collecting and handling your personal information with 13 legally binding safeguards. Businesses have to be accredited under the Australian Competition and Consumer Commission (ACCC) to handle an individual's data. Data security obligations are built into this If user information is no longer needed we must securely delete that information, or de-identify the user depending on the type of data we are collecting if it does need to be stored rather than deleted we must then make sure we maintain it in secure storage such as stored cryptographically.

By following access control like we have previously discussed this will help us ensure we are meeting the requirements for this legislation, preventing access by any user without the appropriate privilege, enforcing strict password complexity and MFA, as well as good coding practices such as the principle of least privilege and by default deny access. This along with transferring and storing data with encryption should ensure a breach of compliance is very unlikely, and we will have a security first mindset during the development phase, and utilising automated testing as well as good error handling and logging we will be more likely to protect individual's personal data by finding and fixing bugs that might cause vulnerabilities that could be exploited.

## Q9 Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure.

Relational databases are collections of information or data in one or more tables made up of columns and rows that stores information and provides access to different data points that are related to one another. Rows hold records and each row contains a unique key to identify that row, these keys can be used in other tables to link the tables together where the key becomes known as a foreign key. Columns contain attributes.

The usual Application Program Interface (API) that is used by relational databases is Structured Query Language (SQL). SQL is used to add, update or remove rows of data from your relational database.

### Data structure and relations

Tables, sometimes known as a relation, are used to store the data and generally each table contains information about one type of data for instance a university database may have one table for students, one table for course subjects, and one table for teachers. These tables would then be linked together by using the primary key from the teacher table as a foreign key in the subjects table for example. The subjects table might also be linked with the students table by sharing its primary key as a foreign key within students table. These relationships between primary and foreign keys are how the tables relate to each other and is what makes it a relational database.

A very simple example of our table might look like this:

Teachers table

| teacher_id  | f_name      | subject_id  |
| ----------- | ----------- | ----------- |
| 1           | Jairo       | 4           |
| 2           | Simon       | 2           |
| 3           | Iryna       | 3           |
| 4           | Matt        | 1           |

Here in the 'Teachers' table teacher_id is the primary key and it has been linked to 'subjects' table by subject_id being used as the foreign key. Below in the 'subjects' table the opposite has happened, subject_id is the primary key and teacher_id is the foreign key.

Subjects Table

| subject_id  | subject_name| teacher_id  |
| ----------- | ----------- | ----------- |
| 1           | Maths       | 4           |
| 2           | English     | 2           |
| 3           | Science     | 3           |
| 4           | IT          | 1           |

## Q10 Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database

Relational database models include integrity constraints which a logical statements which control what values are allowed or not as an attribute and in what format they take. For instance DOB column being in format 01/01/1990 or that teacher_id column has to be a unique number. The advantage of using a relational database with these integrity constraints is that it helps ensure the data in the database is valid, accurate and consistent.

### Domain Constraints

Domain integrity constraints are user defined columns that restrict the type of data that is allowed by an attribute, for instance int, str, DateTime etc. This is specifically called a 'Data type' constraint. If the wrong input is detected it will result in an error to the user. One type of domain constraint is 'Not Null', by default columns will allow a null value, but we can set the column to not allow a null value. Another domain constraint is 'Check', this is a condition that will not allow a value in a column to be different to the parameters that we set, for instance if a number entered is between a certain range.

We can enforce these integrity constraints by following good coding practices such as implementing user-defined data types for our tables, forcing a user to enter a certain type of input such as DateTime or integer otherwise the user cannot successfully input it. This will reduce the likelihood of errors or incorrect information in our database. We can also utilise Check domain constraints to enforce certain rules on the data if required depending on the data we will be using in our database, for instance age column input must be above 18.

### Entity Integrity Constraints

Any data entered into a table in a database is an entity, and each table must have a primary key column to identify each row. Because this primary key is an identifier it must be unique. Entity Integrity Constraints force a primary key to be unique and that no primary key can be set to null. This can be enforced by following good coding practices and always creating primary keys for each table to help identify each row.

### Referential Integrity Constraints

Referential Integrity refers to relation between tables, each table must have a primary key, and that primary key can be used in another table to link them together where in the new table it becomes a foreign key. Referential Integrity is the dependency of that foreign key on the primary key and therefore requires that every value in a foreign key column is also found in the primary key of another table which it is linked to. If a user tries to delete a primary key that is used as a foreign key elsewhere the database server will stop you from doing so with an error. This is referential integrity. We can enforce this in our project by not allowing changes to the primary key.

### Key Constraints

Finally key constraints are rules in a relational database used to ensure consistency and accuracy by defining how a table's values are related to another table's values, thus making sure the information remains correct.

## Q11 Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database

Structured Query Language (SQL) is the language most commonly used to create, analyse and manipulate databases. SQL data manipulation language or DML uses command statements to query and manipulate data within a database such as SELECT, INSERT, UPDATE and DELETE.

### SELECT

SELECT command statement allows the developer to choose specifically which data to extract from a table. For instance SELECT f_name or SELECT * meaning select all data, this is followed by the command FROM designating the table/s to be used to grab the data from. SELECT statements can be combined with other criteria to narrow down the data we are selecting from for instance WHERE, LIKE statements:

```sql
SELECT student_name
FROM students
WHERE f_name LIKE 'S%';
```

This example would search for students whose first names begin with 'S' from the 'students' table. SELECT can also be combined with ORDER BY clause which will determine the order in which the results are displayed for the user. This can be done in descending order by adding 'DESC' after the criteria to be ordered by.

```sql
SELECT *
FROM students
ORDER BY dob DESC;
```

SELECT can also be used with GROUP BY clause which will group rows that have the same values for the selected columns. We can also utilise functions such as COUNT (total number of all items in a container), AVG (average value of a group), MIN (lowest value will be displayed), MAX (highest value will be displayed) and SUM (sum of all items in a container) to give us a specific result in our query. HAVING clause can also be used to restrict the rows retrieved, similar to WHERE except HAVING can include the aggregate function.

```sql
SELECT AVG(grades)
FROM subjects
GROUP BY lesson
HAVING COUNT(lesson) > 1;
```

This would find the average grade from the 'subjects' table of students who have more than one lesson and group them by 'lesson'. SELECT can also be used with the DISTINCT statement to only return unique values.

```sql
SELECT Country -- This would return every student's country including any duplicates which can be unwanted.
FROM students; 
```

```sql
SELECT DISTINCT Country -- By using DISTINCT we would not see duplicate countries. 
FROM students;
```

### INSERT

The INSERT INTO statement is used to add rows to a table in a database. The developer chooses the table the data will be inserted into, VALUES is used to specify the attributes that will be inserted with the row. If you are adding values to all columns you don't need to specify the column names, however if you want to only add values in some columns you will need to include the column names after the table name. If we are specifying only some values the columns without values will either be given a default value if there is a DEFAULT constraint, a NULL if the column allows NULLs and no DEFAULT constraint exists or an error message will be displayed if neither default value exists and the the column is defined as NOT NULL.

```sql
INSERT INTO eating_contest (f_name, hotdogs_eaten, ...)
VALUES (Brad, 72, ...);
```

Multiple rows can be updated at once by separating the values with a comma before closing the whole statement off with a semicolon. For instance:

```sql
INSERT INTO eating_contest (f_name, hotdogs_eaten, ...)
VALUES 
(Joel, 17, ...),
(Ellie, 32, ...),
(Bill, 24, ...),
;
```

### UPDATE

The UPDATE statement modifies data in existing rows by either adding new or changing existing data. UPDATE specifies the table to be updated, and SET designates the values required and for which columns. The WHERE clause is important as without it all rows will be updated with the new information!

```sql
UPDATE bigfoot_sightings
SET date = 01/04/23, location = 'Tasmania', ...
WHERE sighting_id = 7;  -- This would update just the row with id 7
```

To update multiple rows the WHERE clause has to be something that will allow for multiple fields to be changed.

```sql
UPDATE bigfoot_sightings
SET date = 01/04/23, location = 'Tasmania', ...
WHERE Country = 'Australia'; -- This would update all rows where the country is 'Australia'
```

### DELETE

The DELETE statement is used to remove existing rows from a table. DELETE names the table that we are targetting to remove rows from. Like with UPDATE it is critical to use WHERE with DELETE otherwise all rows will be deleted! This will keep the table however; if you want to remove the whole table use DROP TABLE statement.  

```sql
DELETE FROM bigfoot_sightings -- This will delete all of our records from the table, but not delete the table itself. 
```

```sql
DELETE FROM bigfoot_sightings
WHERE Country = 'Australia'; -- This would delete all rows where the country is 'Australia'
```

```sql
DROP TABLE bigfoot_sightings -- This will delete the whole table. 
```

## Q12 Conduct research into a web application (app) and answer the following parts

Chosen web application: Instagram which is a photo sharing platform owned by Meta that allows users to upload photos or videos, edit them such as commonly by applying filters to them, and then share them to either friends or the public. A profile of a user on Instagram may contain a profile picture and display name, a character description, highlights, links and email along with all the photos and videos that user has uploaded. Since its inception in 2010 Instagram has undergone many changes in its application in particular in 2014 when it was bought out by Facebook, resulting in many variation in its exact hardware and software that it has used over the past 14 years. I will focus on the main technologies that Instagram has used over the years in its front and backend.

### a. List and describe the software used by the app

Instagram primarily uses Python and Django for its backend, handling database interactions and application logic, and primarily uses JavaScript (JS) and React for its frontend to create the user interface. Instagram also makes use of cloud technologies such as Amazon Web Services (AWS) for storage, scaling and caching.

Python as we know is a popular programming language widely used thanks to its user friendly and easy to read code and it simply being a robust, general purpose high level programming language. Therefore its no surprise to see Instagram was built utilising Python code. With currently over 2.4 billion monthly active users and over 500 million users accessing Instagram every day it is no surprise that the code used needed to be efficient and a strong focus needed to be on detecting and diagnosing performance regressions.

Instagram developers created static sort checkers, which automate the process of checking that scripts are written correctly, using Python and Pyre to monitor its servers. Another advantage for Instagram using Python is its fast iterations which allow speedy testing of new features as those iterations take only a moment to restart after the test.

Instagram also makes use of the python high level web framework Django which removes much of the hassle from web development by providing security features, scalability and rapid development and implementation of code. Django has allowed Instagram engineers to make speed and efficiency their top priority. Instagram makes use of Sentry which is an open source Django application for automatic reporting of exceptions and errors as well as performance monitoring. With the sheer volume of users security is paramount with so much personal data being stored the site is definitely a target for malicious actors. Django Object Relational Model has proven secure and scalable in dealing with the tremendous volume of Instagram users by following its MVT (Model-View-Template) architecture which has a robust authentication system.

Instagram's frontend, or user interface is written in React Native which is a User Interface (UI) software framework developed by Meta and was created because Facebook CEO Mark Zuckerberg found the use of HTML5 to result in an unstable version of Facebook mobile app so his team worked on a way to create UI elements from a background JS thread which eventually became React Native. This background thread interprets the JS written by the engineers results in a much more stable mobile platform for the User interface.

Instagram also makes use of the widely popular PostgreSQL to handle its database storage system including data like user profiles, images, videos etc.

### b. Describe the hardware used to host the app

Instagram initially was using AWS to host its app before moving to facebook data centers in 2014. The move took 3 weeks and is one of the largest and fastest migrations to date between Amazon's EC2 (Elastic Compute Cloud) and their virtual private cloud. Data centers are physical locations to store computers and related hardware. Facebook has data centers across the US and Europe which has allowed Instagram to which continues to grow exponentially to not run out of space as its user's increase. The added bonus to European servers means the latency is also reduced for users in Europe.

Infrastructure can be separated into Stateless and Stateful service.

- Stateless service is something which has no knowledge or memory of previous requests or calls, they don't save client session data on the server instead relying on externalised state data. One such example used by Instagram is Django web server.

- Stateful service is a call or request that does have knowledge or memory of a previous call or request by saving client session data, which provides faster processing and historical context. Examples of this used by Instagram are Cassandra and TAO.

Stateless services are easy to deploy and scale, but stateful services are needed to store user data, which obviously Instagram has in abundance. Instagram uses Cassandra to store key-values to support user's direct messages and photo feed as well as for fraud detection. Instagram uses Facebook's TAO data store for graphical data and is used to cache user related data such as profiles, friends and other user specific information. Instagram also makes use of Postgres for handling some user and media data.

### c. Describe the interaction of technologies within the app

With billions of photos and videos uploaded to Instagram as you can imagine there is a complex process to store and search through that media to display content to a user that is relevant for them, I will break down the process as simple as I can. The engineers at Instagram decided to shard the data that is sent on their application which means placing the data into many smaller buckets each holding part of the data, similar to how packets work when sending information on the internet. This ensured efficient and fast access of data as well as making sure that data fits into memory.

Instagram allows users to create a profile and post media to the public or to friends by accessing its frontend user interface. users can interact with other users and their media through likes, comments, shares, messages and various other interactions. Instagram uses a suite of algorithms and processes to personalise a user's experience by curating and showing more content that the application thinks would interest the user based on previous experiences, interactions and activity.

This media is then stored via a distributed storage system which stores data across multiple servers in different parts of the world. PostgreSQL is the main database used by Instagram storing most of the user's data and media.

Not only will Instagram offer curated content to the user but there is also a search function allowing a user to find particular media or person of interest to follow or view. Instagram has a denormalised store of all searchable entities, whether that is hashtags, users etc. These entities are all grouped together and encoded into set operations by Instagram's backend. These are then queried by efficient set operations such as AND, OR and NOT, then the results are ranked and trimmed leaving only the most relevant results. When a user sends a search a POST request is made and sent to Instagram's server.

Here that request does two things, firstly it is archived in the Hive Metastore which is a PostgreSQL database with the purpose of being data scraped in the future. Secondly that request needs to go through to find the results. To solve the denormalisation problem Instagram uses a process called Slipstream where events on Instagram such as likes or follows are encoded into a large structure, binary serialised then sent over an asynchronous channel that Meta called the Firehose. Sending the information asynchronously keeps the data clean and solves denormalisation. Once the request is passed through Firehose it is sent off to various search indexes such as hashtag, location, user and media search as well as to the hive.

### d. Describe the way data is structured within the app

The backend of Instagram runs Django framework with PostgreSQL as the primary database, but also leverages Cassandra and Redis which are NoSQL databases. Cassandra stores metrics and analytics and is used because of its flexibility and write speed making it useful for metric data. Redis is used for caching, it stores temporary data like stories and other content that need low latency access which reduces load on the backend and makes the application more efficient.

Combining the speed and scaling capabilities of Redis and Cassandra with the relational model of Postgres Instagram is able to optimise for performance and reduced complexity as well as scalability. Whilst conventionally a developer might use a database's primary key feature to identify data that wasn't going to work for Instagram's application which contains multiple databases that might need data inserted at the same time. Instagram's solution was sharding as we have previously talked about, and to generate a unique 64 bit ID for the data they started a timer and then at the time of creation of an entity such as a post or a comment that time was stored as 41 bit, 13 bits to represent the shards, and 10 bits to represent the incremental IDs in Postgres, making 64 bits. The generated IDs are sortable by time, and the 64 bits allow better storage in systems like Redis and smaller indexes.

### e. Identify entities which must be tracked by the app

Identified entities:
User Profile - name, bio etc
Comments
Media Posts - Likes, Hashtags, Locations
Follows
Direct Messages

Instagram has many different entities as previously discussed such as likes, media posts, follows, comments. There are also users each with their own profile that also must be tracked. All these are tracked by the app using its sharding and generation of unique 64 bit IDs as explained in d. The ID is made up of 41 bits for time in milliseconds, 13 bits to represent shard ID, and 10 bits to represent the incremental IDs in PostgreSQL.

Instagram also stores data from the user in the Hive which it can use for future searches. Instagram also makes use of Unicorn which is a social graph aware search engine that was created by Facebook. Unicorn is able to search through the trillions of entities allowing the application to save information such as users, locations, hashtags etc and more importantly the relationship between those entities.

### f. Identify the relationships and associations between the entities you have identified in part (e)

Identified entities:
User Profile - name, bio etc
Comments
Media Posts - Likes, Hashtags, Locations
Follows
Direct Messages

User Profile would be linked to Follows, Media Posts and Direct Messages. Media Posts and comments would be linked together. I have decided to focus on some main entities for one user, obviously with Instagram being such a large application the relationships and associations could end up being massive.

### g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model)

![Instagram_ERD](Instagram_ERD.jpg)

## References

### Q1

Garcia, M 2020, 'Use a Flask Blueprint to Architect Your Applications', viewed 31 January 2024, https://realpython.com/flask-blueprint/

### Q2

Dhruv, S 2024, 'PostgreSQL Advantages and Disadvantages', viewed 31 January 2024, https://www.aalpha.net/blog/pros-and-cons-of-using-postgresql-for-application-development/

PostgreSQL docs 2024, 'Chapter 28. Security', viewed 31 January 2024, https://www.postgresql.org/docs/7.0/security.htm

### Q3

Ed Lesson, 'Core Agile Concepts', viewed 30 January 2024, https://edstem.org/au/courses/13988/lessons/43328/slides/296985

Ed Lesson, 'Stand-Ups', viewed 30 January 2024, https://edstem.org/au/courses/13988/lessons/43328/slides/296986

Radigan, D 2024, 'What is a stand up meeting & tips to run one', viewed 31 January 2024, https://www.atlassian.com/agile/scrum/standups

Ed Lesson, 'Kanban', viewed 30 January 2024, https://edstem.org/au/courses/13988/lessons/43328/slides/296988

Ed Lesson, 'User Stories', viewed 30 January 2024, https://edstem.org/au/courses/13988/lessons/43328/slides/296987

Ed Lesson, 'Sprints', viewed 30 January 2024, https://edstem.org/au/courses/13988/lessons/43328/slides/296989

Ed Lesson, 'Sprint Retrospectives', viewed 30 January 2024, https://edstem.org/au/courses/13988/lessons/43328/slides/296990

Ed Lesson, 'Task Prioritisation', viewed 30 January 2024, https://edstem.org/au/courses/13988/lessons/43328/slides/296991

### Q4

Garcia, M 2020, 'Use a Flask Blueprint to Architect Your Applications', viewed 31 January 2024, https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development

### Q5

Zettler, K 2024, 'Use a Flask Blueprint to Architect Your Applications', viewed 1 February 2024, https://www.atlassian.com/continuous-delivery/software-testing/automated-testing

### Q6

Risk Optics, 2023 'What are Information Security Controls?', viewed 31 January 2024, https://reciprocity.com/resources/what-are-information-security-controls/

Thurmond, T 2023, '8 Best Secure Coding Practices', viewed 31 January 2024, https://kirkpatrickprice.com/blog/secure-coding-best-practices/

Haas, L 2021, 'What You Need to Know About Code Risk Management', viewed 31 January 2024, https://www.mend.io/blog/risk-management-of-code/

McCarvill, A 2023, 'Best Practices for Secure Coding in Web Applications', viewed 31 January 2024, https://brightsec.com/blog/best-practices-for-secure-coding/

### Q7

Risk Optics, 2023 'What are Information Security Controls?', viewed 31 January 2024, https://reciprocity.com/resources/what-are-information-security-controls/

McCarvill, A 2023, 'Best Practices for Secure Coding in Web Applications', viewed 31 January 2024, https://brightsec.com/blog/best-practices-for-secure-coding/

Cortex, 2023, 'Different types of code security practices', viewed 31 January 2024, https://www.cortex.io/post/different-types-of-code-security-practices

### Q8

NSW GOV 2024, 'Privacy Act 1988', viewed 31 January 2024, https://www.legislation.gov.au/C2004A03712/latest/text

Office of the Australian Information Commissioner 2024, 'Consumer Data Right privacy and security', viewed 2 February 2024, https://www.oaic.gov.au/consumer-data-right/information-for-consumers/consumer-data-right-privacy-and-security

Office of the Australian Information Commissioner 2024, 'Rights and responsibilities', viewed 2 February 2024, https://www.oaic.gov.au/privacy/privacy-legislation/the-privacy-act/rights-and-responsibilities

Office of the Australian Information Commissioner 2024, 'Australian Privacy Principles quick reference', viewed 2 February 2024, https://www.oaic.gov.au/privacy/australian-privacy-principles/australian-privacy-principles-quick-reference

### Q9

Lutkevich, B 2024 'relational database', viewed 31 January 2024, https://www.techtarget.com/searchdatamanagement/definition/relational-database

### Q10

Watt, A. and N. Eng. (2014). Database Design – 2nd Edition. Victoria, B.C.: BCcampus. Chapter 9 - https://opentextbc.ca/dbdesign01/chapter/chapter-9-integrity-rules-and-constraints/, viewed 31 January 2024

Mullens, C 2020, 'The Importance of Database-Enforced Integrity', viewed 31 January 2024, https://www.dbta.com/Columns/DBA-Corner/The-Importance-of-Database-Enforced-Integrity-139858.aspx

### Q11

Watt, A. and N. Eng. (2014). Database Design – 2nd Edition. Victoria, B.C.: BCcampus. Chapter 16 - https://opentextbc.ca/dbdesign01/chapter/chapter-sql-dml/, viewed 6 February 2024

### Q12

Page, M 2017, 'Profiling CPython at Instagram', viewed 6 February 2024, https://instagram-engineering.com/profiling-cpython-at-instagram-89d4cbeeb898

Shewale, R 2024, 'Instagram Statistics – Global Demographics & Trends (2024)', viewed 6 February 2024, https://www.demandsage.com/instagram-statistics/

Xiao, S 2018, 'How Instagram is scaling its infrastructure across the ocean', viewed 6 February 2024, https://opensource.com/article/18/10/instagram-scaled-infrastructure

Mosseri, A 2023, 'Instagram Ranking Explained', viewed 6 February 2024, https://about.instagram.com/blog/announcements/instagram-ranking-explained/

Instagram Engineering 2015, 'Search Architecture', viewed 6 February 2024, https://instagram-engineering.com/search-architecture-eeb34a936d3a

Shivang, S 2024, 'Instagram architecture & database – How does it store & search billions of images', viewed 6 February 2024, https://scaleyourapp.com/instagram-architecture-how-does-it-store-search-billions-of-images/