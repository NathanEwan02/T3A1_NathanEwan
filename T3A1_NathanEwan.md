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



## Q13. 
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