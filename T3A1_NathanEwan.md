# T3A1 Workbook

## Q1. Provide an overview and description of a standard source control process for a large project <br></br>

The standard source control process for a large team using a source control system such as git will begin by delegating each of the developer teams to different parts of the application such as front-end, back-end, models, views, controllers etc. depending on the context of the project. These teams will then be broken up further to handle more specific tasks like one person from the front-end team handling views for the home page and another person coding the about page. The main developer in charge would then create the central repository on a server. These central repositories can be made using a third-party git hosting service which would handle the initialization and hosting, as well as provide an address to the central repo which can be accessed locally. From then on, each developer clones the central repository to their local system by using the `git clone` command followed by the address. Once developers have begun development, they will focus on making regular commits to their local cloned repository. This is done through the standard process of adding any file changes the developer has made to the code via the `git add` command, which will remain until a commit has been issued. Then once all changes have been added to the staging phase, they can be committed using `git commit -m ‘’`. The changes will then be joined with the main local branch and any comments within the commit statement will be visible so that once pushed other developers will know what was changed. The final step in the process is to push these commits to the main/master branch of the application. This can be done using one of the following commands `git push origin main` or `git push origin master` depending on what system is being used. 

Once these pushes have been made developers may run to issues of merge conflicts. Merge conflicts occur when two or more developers have made changes to the same file or files that directly conflict with on another. Thankfully if local commits conflict with each other git will pause the process and allow for the developers to manually fix these issues. The developer that had originally pushed their changes can come across a merge conflict would fix these issues by first using the command `git pull` to take the changes made by the other developers and integrate them locally. Developers will generally communicate with one another to resolve the issue and often use `git status` to find the source of the problem.

## Q2. What are the most important aspects of quality software?

As a software developer it is crucial that it is understood what separates quality software from inadequate or lackluster code. There are several factors that contribute a developer delivering valuable software however, there are six essential aspects that define this. These are efficiency, reliability, useability, portability, testability, and modifiability. Efficiency is ‘achieving maximum productivity with minimum wasted effort or expense’. One way we can measure efficiency is through the use of ‘Big O Notation’. This refers to the amount of time taken for a function or algorithm to complete and how much that time increases when given larger data sets. So, for a developer to ensure quality software they must understand algorithmic time complexity. The efficiency of a developer’s software also directly ties to how it is received, if an application requires the user to wait long amounts of time between tasks, then it is not good software. 

Next is reliability which describes how dependable a user can be on a programmer’s code. If a piece of software does not function correctly on a consistent basis, then it cannot be considered reliable. To create reliable code a developer should minimize or all together eliminate the occurrence of errors within the code. A user be able to rely on their application to work without inconsistencies. 

When talking about useability it is important that the developer ensures that their application is understandable to the end user. If the layout and flow of the program is not easy to follow, then it has not done its job. The web page or application should be well organized and structured in a manner that indicates very obviously how to navigate and use the app. One way that a developer may be able to achieve this could be through the use standardized/universal tools. For example, generally on a web page there is a navigation bar at the top with all the important links. If a user attempts to diverge from this standard practice in an unconventional way, then this may result in an app that is difficult to understand. This also relates to source code. If the code does not have descriptive comments and a clear layout of files, then it may be harder for another developer to understand. 

Portability is a way to ensure that the software can reach a wider audience and be used on multiple different, devices and operating systems. An example of this would be an application that is made accessible from its original platform such as an android game, which is then made available to Apple device users. This could also include web pages, where a website can be tailored in CSS to fit multiple different screen widths and display information differently depending on the screen. 

Testability is the process of ensuring that code works before it available to the general user base. The testing process works by running code through a piece of code that tests the original software for specific outputs and returns false if it failed or true if it was successful. The process of testing can either be done manually or automatically through the use of third-party software services. 

Finally, modifiability is a method of making code more flexible as new features are added over time. The software should be able to handle new plugins, systems, and software without requiring a large amount of refactoring. The software should require minimal changes or modification to the original code in order to add these new features. This may also mean that code is made so that it is backwards compatible.

##  Q3. Outline a standard high level structure for a MERN stack application and explain the components

The MERN stack is a full stack web development framework consisting of MongoDB, Express JS, React JS, and Node JS. These technologies work together to synthesize front-end, back-end, and database systems together to produce a fully fledged full stack application. 

MongoDB is a document-oriented database that operates from a NoSQL database management system. This means that unlike in a traditional relational database where data is stored inside of tables with each entry being a row, the data is instead stored as a collection of documents in binary JSON format. This is done because it allows for faster exchange of data between the client and the server. This also assists in its scalability as it can store a sizeable amount of data. 

Express JS is a back-end web framework for Node JS, and its main purpose is to assist in writing simplified and fast code. Its job as apart of the framework is to serve as the controller of the MVC model. It interacts with the mongoDB database to retrieve data and communicate this information with the React framework. 

React is seen as the ‘views’ of the MVC model and work with the controller to get the data needed to display to the user’s browser. The benefit to having the React framework as apart of the MERN stack is that it allows user to make changes to the page without needing to refresh. 

Node JS is a server environment for JavaScript designed to handle providing server environment for the web app. It is used to run the JavaScript code on the server side of the application. 

## Q4. A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?

There are four main types of skills that would be required for a team of developers to build this project, that being programming skills, communication skills, planning, and knowledge of security. Programming skills would include mostly front-end skills however, backend skills could also come in handy depending on the type of business and their scope. The more specific skills required for the application (assuming it only requires frontend) would be HTML, CSS, and JavaScript. HTML and CSS are important as together they work to create a functioning static website with both structure and styling. While the JavaScript will provide the more functional, customized, and optimized aspects of the website when paired with a web framework such as React or Angular. If the website requires additional backend features, then the team will need skills in a back-end framework and language such as Ruby and Ruby on Rails, as well as a database management system. 

Communication skills are also an important part of developing websites. This means that the team should set up some sort of system where they are able to discuss what they each have been working on and what needs fixing. This could be done through daily meetings and collaboration with team members working on similar features or aspects of the app. Another part of the communication process is to make sure that the stakeholders/business owners are aware of what is happening and that the team’s goals are aligned with the visions of the stakeholders.

Planning can be broken down into five key components, assigning jobs, creating ERDs, creating wireframes, deciding deadlines, keeping track of tasks. The wireframes should be one of the initial parts of the project that must be approved by the stakeholders of the business. From there, the team leader can then begin assigning features of the application to each person in the team and set deadlines for them to complete them. All the while each task to be kept track of by the developers for their own tasks, using a management tracking software such as Trello. Finally, another important part of the planning phase includes generating ERDs (if required). This will be done using a piece of software that uses standardized tools to indicate the relation between data and the entities.

Another crucial part of developing a piece of software for a client is to ensure that they are safe from cyber security attacks. Ensuring that the team has a solid understanding of encryption methods and different ways to ensure the data security of their stakeholder are crucial. This means knowing how to use built in features of the programming languages, frameworks or add-ons when creating the application. 


## Q5. With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges

The rails marketplace application I had developed as part of the term 2 assessment for CoderAcademy required a variety of skills and knowledge to complete. To be more specific I will break these up into three classifications, technical, planning, and soft skill. The tech skills I needed for this project included knowledge of Ruby on Rails, Ruby, HTML and PostgreSQL. To first tackle the Ruby on Rails framework I needed an understanding of the basics of Ruby this meant a solid understanding of classes, functions, objects, and how files interact with one another. This is what allowed me to approach Ruby on Rails, which led me to learning the concept of MVC’s (models, views, and controllers) and how each of these interacted with one another. This allowed further incorporate my skills of HTML when creating views using erb (embedded ruby) to display data from the data base on a web page. An understanding of relational data was also a crucial aspect of this assignment. This meant knowledge of the built-in ruby query methods which allowed for ruby syntax to make SQL requests to the database. As well as understanding how each piece of data and entity was related to one another through primary and foreign keys and many-to-many, one-to-many, and one-to-one relationships. As for Postgres, I required knowledge of how to navigate the data base management system and its available tools. 

For planning skills, I required knowledge and skills in ERDs, project management, documentation, and wireframes. When creating ERDs for my assessment I firstly had to understand what entities were needed, the relationships between each entity and the entries required for them. From there I could focus on the building an ERD that specified the type of data, name of entry, constraints, specifying key type and understanding how to represent each relationship using specific symbols. After I had created my ERD next focus had been to start the project, this meant that both management and documentation of the project would be dealt with as it was being developed. My management skills entailed identifying a general overview of what tasks needed to be done and breaking these jobs into smaller chunks and prioritizing them differently. Tasks were tracked using Trello and were broken up into ‘to do’, ‘doing’, and ‘done’. The documentation of the project also apart of the planning process as it required me to delegate time toward it and update and change parts of the project when reassessing what I had written. Finally, the wireframes required me to use design skills to outline a vision of a functioning app based on what I had proposed as an idea. This played into the skills used in the management of the project which was revaluating ideas and modifying them so that they either made the app look better or function differently. 

Lastly are the soft skills, which include problem solving, time management, and critical thinking, these skills were what enabled me to maintain speed and efficiency through the project. Problem solving has always been a crucial part of programming and I have had to apply it multiple times in the lifecycle of the project. When my code produced errors, wasn’t working or gave the wrong output I needed to analyse and evaluate the code I had written to determine the issue. This also played into soft skills such as perseverance as at times I had to refactor a lot of code or research to find out what had caused the issue. Time management played a big roll as it assisted in delegating energy and time to more crucial aspects of the project or parts I was struggling on. This prevented me from wasting time on unnecessary tasks.

## Q6. With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature

The specific project I will be discussing is my T2A1 terminal application. For this project I was required to have a solid foundational understanding of the Ruby programming language with more specific knowledge of classes, functions, and modules. This base knowledge of Ruby had served me well, as it was a contributing factor that demonstrated an aptitude and good understanding of these fundamentals. As a part of this project, I had also been required to demonstrate skills in using ruby gems and how to effectively interrogate them into the application. I believe this has shown my skill in being able to adapt to new syntax and plugins as this is an important skill for a programmer to have, as we are required to easily adapt to different languages, frameworks, and add-ons. My documentation was what allowed me show that I am capable of communicating ideas and concepts to other people whether it be through PowerPoints or written documentation. 

Where I feel I have been unsuccessful in demonstrating the skills used throughout the project was within the management process of the application. To be more specific I am referring to the infrequent use of planning and tracking tasks through the project with Trello (the progress tracking application used). Though I did contribute to the Trello board I did not do so enough to show my thinking process and how I was managing tasks. To fix this issue in future projects I aim to frequently and consistently update the Trello board, but also provide notes and sub notes that are comprehensive but not overly bloated. I would begin by setting out the main goals and adding details to them as each task is being complete and setting new ones once I have committed the change to the repository.

One of the other places I feel as if I could have contributed more to was comments in my code. Though I had enough comments some were wasting space explaining a singular line of code that was not as crucial to the program or could have been brought up in other sections of code. The comments were also lacking in substance and could have focused more on how each function or line of code may have contributed to the code as a whole rather than explaining what they do in isolation of one another. 

Finally, due to my over emphasis on implementing classes and other concepts I had been learning it had resulted in me needing to refactor code. This was because I had been using classes for functions or loops that did not require their own classes to be created. I had treated classes to design every aspect of my application which was a mistake. Next time I will focus on treating new programming concepts as tools to create code for specific contexts rather than treating them as a way to fix every single type of task. 


## Q7. Explain control flow, using an example from the JavaScript programming language

The model of control flow (also known as the flow of control) is one that is featured in all high-level programming languages. It refers to the sequential order in which each instruction, statement and line of code is executed. The code will execute each line of code in order starting from the first line until it arrives at the last line unless it reaches a conditional statement or a loop. A conditional statement is used to commit a particular sequence of code only once the condition/conditions for that statement are true. Otherwise, it will be ignored and instead commit the ‘else’ part of the conditional. If there is no ‘else’ statement, then the code will simply continue from the preceding line of code where the conditional ended. There are different types of loops in JavaScript, two of which will be explained, for loops and while loops. A for loop works by iterating over each element within a given variable (such as an array, object, or string) and uses an index/counter to determine when that loop will end. The index will be increased after each iteration until it reaches a specified number. As for the while loop, it operates by executing the code given to it while a condition is true and ends once it is made false within that while loop. Functions/methods are also executed differently from regular code. In control flow a JavaScript function is not executed unless it has been called upon. This means that even if a function containing a block of code is at the top of a JavaScript file it will not be executed unless the name of that function is used to execute it.

Below is a snippet of JavaScript code that will be used to demonstrate the concept of control flow within the language. 

```
function Multiplication(a, b) { // This function is ignored by the code as it has not yet been called on
    return a * b 
}

function Addition(a, b) { // This function is also ignored by control flow
    return a + b
}

let count = 0 // This is the first line of code that is read
let num1 = 5 // Second line of code that is read
let num2 = 10 // Third line of code that is read

while (count < 5) { //This while loop will reamin true until count is equal to or greater than five
    if (num1 < 25) { //This conditional stament is run only if num1 is less than 25
        num1 = Addition(num1, num2) // The second function is called upon and can now be run
        count ++ // The count variable is incremented by one so that the loop will eventually end when it hits five
    } else { // Once the first conditional is deemed to be false it will run the code bellow
        num2 = Multiplication(num1, num2) 
        count ++
    }
}

console.log(num1) // The value of num1 is printed when the count reaches 5 and loop ends
console.log(num2) // This is the next line of code executed
```

## Q8. Explain type coercion, using examples from the JavaScript programming language

Type coercion is the implicit transformation from one data type to a different data type. This can include float to integer, integer to float, integer to string, string to integer and so on. It is important to note that type coercion and type conversion are separate, type coercion is always implicit whereas type conversion is explicit. These changes will occur depending on the type operating performed on them. For example, when adding a string with numeric values and an integer JavaScript will assume that the operation being performed is a string concatenation and implicitly convert the integer into a string. Whereas for the opposite (string to integer coercion) a multiplication, subtraction or division operation must be used on these two values. In the case of changing Boolean values to numeric ones, the Boolean is converted to an integer, 0 for false and 1 for true. 

Below are some examples of this in JavaScript.

```
const string = '50' // Initialising a string 
const int = 10 // Initialising an integer
const bool = true // Initialising a boolean

console.log(`This is integer to string coersion ${string + int}`)
console.log(`This is string to int coersion, ${string * int}`)
console.log(`This is boolean to integer coersion ${bool + int}`)
```

## Q9. Explain data types, using examples from the JavaScript programming language

Put simply, a data type is a method of classification used to distinguish between different types of data. This is done so that data can be used in various contexts for a particular task or to obtain a specific output. The JavaScript language uses many data types including, integers, strings, arrays, objects, Booleans, and floats. Integers are whole numbers that can be positive, negative and zero. Mathematical operations can be performed on integers including the basic operations multiplication, division, addition, and subtraction. This also goes for floats (floating point numbers) which are integers followed by decimals which can provide a more precise numeric value for the developer. Strings simply refers to a string of characters be it numbers, letters, or symbols. This data type can perform functions such as string concatenation and can be iterated through using a loop. Arrays can be thought of as a list/collection of values which can be either, integers, strings, floats, Booleans and even objects. Arrays can be iterated through using loops such as for loops and while loops and holds a numbered index value for each element of the array starting at zero. Objects are a collection of key/value pairs that can either be represented as symbols (using ‘:’) or as strings. The key value pairs within the object are not ordered and are accessed by their key. Finally, there are Booleans which are data types that can only have two possibly values, most often represented as true or false. 

## Q10. Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language

There are many ways in which an array can be manipulated, this includes iteration, finding an element or checking if an element exists. JavaScript provides developers with many built in methods to simplify achieving these things. Each of these methods either falls into the category of an ‘non mutable’ method or a ‘mutable’ method. This means that mutable methods will be able to change the contents of the array, whereas a non-mutable method cannot. An example of some of the methods that are non-mutable include: 

-	Array.find(), returns the item in the array with the given conditions
-	 Array.findIndex(), is used to find the element in the array with the corresponding index
-	Array.includes(), will check if the given value exists in the array
-	Array.indexOf(), returns the index of the value in the brackets
-	Array.length, will return the length (number of elements) of the array
-	Array.isArray, return true if the given value is an array, and false if it isn’t
-	Array.concat(), merges two arrays or a value to the end of an existing array
-	Array.slice(), works by breaking up the given array by the array index that was provided. For example, in an array of integer elements from 1 to 5, array.slice(2) will return [3, 4, 5]. Meaning it returns an array of every element form array index 2 and above.

The following list is an example of a few array methods that are mutable:

-	Array.shift(), removes the element from index zero (beginning of array)
-	Array.unshift(), inserts an element at the beginning of the array
-	Array.pop(), deletes item from the end of the array
-	Array.push(), adds item to the end of the array
-	Array.splice, the splice method takes an integer as the first parameter to indicate the position in the array that the splice method will modify. The second parameter is also an integer and indicates the number of elements that will be removed if its is array.splice(2, 2) then the method will remove the element in the array at index 2 and the element the + 1 index over. The method can also take additional parameters like strings or integers, that will replace or add those elements.

The next list will be examples of different ways to iterate through an array, some of these being built in methods and others being loops that can be used to manipulate an array. This will also include both mutable and immutable ways to iterate through arrays.

-	Array.forEach(), The forEach method uses a callback function which is applied to the element in the array. However, the forEach method is immutable and will return ‘undefined’ if you attempt to return the values.
-	Array.map(), creates a new array meaning it is immutable. The map method can be used to implement a function for each of the elements in the given array. However, unlike the forEach method it creates a new array using the values returned from the function. 
-	Array.filter(), works similarly to the previous methods because it also uses a function, and iterates through each element to apply the function. Unlike the other methods though, this only returns the values where the callback function returns ‘true’. 
-	The for loop is a way of iterating through an array without using a built-in method. This way of iteration requires an argument to be given which needs a variable to be assigned that declares what index the loop starts on, the end index of the loop, and how much the variable will be increased after each element. 

Below is an example of multiple different ways in which an array can be manipulated in JavaScript code. 

```

```

## Q11. Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language

A JavaScript object is an unordered collection of properties, with each property consisting of a key-value pair. The key-value pair refers to the association between a given key (which can be represented as either a string or symbol) and the value of the key. An object can either be declared by assigning a variable with `new Object()` or by using curly braces such as, `const person  = {}`. To talk about data manipulation of objects in JavaScript, the first concept to understand is creating/adding new properties to an existing object. In JavaScript this can be done by using the name given to the object followed by a period (.) and the name of the new or existing key. This is then followed by assigning a new value using the equals sign (=) and the new value itself. For example, `person.name = ‘David’`. Since our person object does not yet have any properties a new key value pair will be created as a result of this. If the key already exists, then this declaration will reassign the original value of that key to the new one. 

There are also several built-in methods that can be used on objects to manipulate and retrieve data. An example of a few of these methods include Object.entries, Object.keys, Object.values, Object.freeze and Object.seal. The entries method is a way of retrieving all the key value pairs within an array. The method generates an array of arrays and within each array there is the value and the pair. Object.keys works by returning only the keys of a given object which are all stored together in an array. It is important to note that it will not provide any nested keys that might be in the object. The values method works in a similar matter however, instead of returning the keys of an object, it will return the values of these keys. The freeze method is used as a way of preventing an object form being altered. This means that once an object has been frozen properties cannot be added or removed and the values of existing object cannot be changed either. This is useful for when developers need objects with read only privileges. The seal method like the freeze method also prevents the adding or deleting of properties but allows the values of keys to be changed.

When using objects in JavaScript is often the case that developers will come across an array of objects, so it is equally important that it is known how to manipulate objects within an array. One of the ways of doing this is through a for loop. As an example, let’s propose that you have an array of objects, and you want to access every value of a specific key. This can be done by setting a for loop that starts at index zero and increase by one until it reaches the end of the array. The next step is to simply return the following line of code `obj[index].key` where ‘obj’ is the name of the array of objects, ‘index’ is the current index that the for loop is on, and ‘key is the name of the keys the developer wants the value of.

Lastly, there are also ways of incorporating functions into objects through the use of the ‘set’ and ‘get’ key words. Set is used to create function within an object that are used to set/change the existing value of a property. Get on the other hand is used to retrieve one or multiple properties and log them to the console or display them in some way. 

Below are a few examples in JavaScript code of how objects can be manipulated.

```
const person = {
    name: 'James',
    age: 42,
    score: 0,
    set updateScore(num) {
        this.score += num;
    }
}

Object.values(person) // returns ['James', 42, 0, undefined]
Object.keys(person) // returns ['name', 'age', 'score', 'setScore']
Object.entries(person) // returns [['name', 'James'], ['age', 42], ['score', 0], ['setScore', undefined]]
person.updateScore = 4 // updates the score by + 4
person.updateScore = 6 // score is now at 10
Object.seal(person) // prevents objects from being deleted
delete person.score // does not work
person.name = 'Joe' // still works because object is not frozen
Object.freeze(person) // freezes object
person.age = 43 // does not change age because object is frozen


const people = [{
    name: 'David', age: 24, address: {city: "Brisbane", state: "Queensland"}
}, {
    name: 'Jain', age: 31, address: {city: "Melbourne", state: "Victoria"}
}, {
    name: 'Mason', age: 19, address: {city: "Brisbane", state: "Queensland"}
}]

for (let i = 0; i < people.length; i++) {
    if (people[i].address.city == 'Brisbane') { //finds each person that lives in brisbane
        console.log(people[i]) // prints the object that have a city == brisbane to the console
    }
}
```

## Q12. Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language

JSON (JavaScript object notation) is a standard way of representing structured data in text-based format. Its most common use is for transmitting data to be displayed in web apps. As the name suggests it is very similar to how JavaScript objects are represented that being curly braces ({}). Manipulating the data within JSON objects is also similar to how it is done in vanilla JavaScript with some differences. To demonstrate how JSON can be manipulated I will explain how to create, delete, and parse JSON data. Creating JSON data can be done by ensuring that the keys are stings and the structure begins with curly braces as an object should. Next, we take a variable that holds the object we want to pass to the JSON file and use the method `JSON.stringify()`. This method uses the object as a parameter and converts the keys to strings making it much mor simple for it be implemented into a JSON file. When deleting a JSON element it can either be done manually or by using various built-in methods, for example if you have identified the position of the object and the json is stored in an array you could use a splice method. Finally, the most common way of manipulating JSON day is by calling from a file so that it can be used in some way in a program. This is done by using the JSON built in function called `parse()` which retrieves the JSON object and returns it in standard JavaScript object format. This can then be stored in a variable where further data manipulation can be used. 

```
let pets = {a: 'Cat', b: 'Dog', c: 'Bird'}
JSON.stringify(pets) // The pets object has changed to '{"a": "Cat", "b": "Dog", "c": "Bird"}'
console.log(pets.a) // Logs "Cat" to the console
console.log(pets["b"]) // Logs "Dog" to the console

const jsonPerson =  '{"name": "Daniel", "email": "danielj@gexample.com", "age": 22}'; // Creating a json object
const person = JSON.parse(jsonPerson); // This consverts the JSON notation to a standard javascript object
person.age // This will return 22
```

## Q13. For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes

``` 
class Car { // Intitalising a class named Car
  constructor(brand) { // Initialisation of a constructor method which is used to establish the properties/attributes of the class and is called upon creation of a class instance.
    this.carname = brand; //These are the attributes of the class. The carname variable is assigned the value of brand. The 'this' is called a object scope and is what enables the attribute to be used within class methods.
  }
  present() { // A method accessible only by the Car class
    return 'I have a ' + this.carname; // a return statment that will return 'I have a ' and the value of this.carname.
  } // End of function.
} // End of class 'Car'

class Model extends Car { // Creates a class called 'Model' and uses the key word 'extends' to inherit from the Car class.
  constructor(brand, mod) { // The initialisation of the brand and mod attributes.
    super(brand); // The 'super' is used to access the brand attribute from the Car class as well as any additional methods or attributes.
    this.model = mod; // This creates a paramater called 'thid.mod' that is accesable within the Model class.
  }
  show() { // A method accessable in the Model class.
    return this.present() + ', it was made in ' + this.model; // This calls on the 'present' method within the Car class and concatinates this with a string and the this.model attribute, and then returns it.
  }
} // End of Model class

let makes = ["Ford", "Holden", "Toyota"] // defines an array called 'makes' which holds the different names of car brands. This declaration uses lets which allows for the array modified later on.
let models = Array.from(new Array(40), (x,i) => i + 1980) // Creates an array of 40 elements. It then iterates through the array with x being the iterator and i being each element. It starts at the first index and will set a value of 1980 and incease each time by one. 

function randomIntFromInterval(min,max) { // min and max included, a new function with two parameters, min and max.
    return Math.floor(Math.random()*(max-min+1)+min); // A rounded down random number that uses the equation min - max + 1 + min. Math.random will then return a value from the sum of the equation provided.
}

for (model of models) { // This is for loop that will iterate through each model (40 models) within the models array.

  make = makes[randomIntFromInterval(0,makes.length-1)] // A variable called make that uses the randomInt with the parameters of 0 and the length of the makes array - 1 to retrieve a random make from makes array.
  model = models[randomIntFromInterval(0,makes.length-1)] // Does the same thing as the previous varibale however, it uses the models array to retrieve its data.

  mycar = new Model(make, model); // creates a new varaible 'mycar' to create a new instance of the Model object using the attributes of the make and model variables above.
  console.log(mycar.show()) // logs the result of the mycar instance using the show method within the model class. This prints to the console 'I have a make, it was made in model.' This will be repeated 40 times in total, as that is the number of elements within the array.
} 
```
# References

