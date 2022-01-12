# T3A1 Workbook

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

  make = makes[randomIntFromInterval(0,makes.length-1)] //
  model = models[randomIntFromInterval(0,makes.length-1)]

  mycar = new Model(make, model);
  console.log(mycar.show())
} 
```