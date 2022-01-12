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
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

let makes = ["Ford", "Holden", "Toyota"]
let models = Array.from(new Array(40), (x,i) => i + 1980)

function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

for (model of models) {

  make = makes[randomIntFromInterval(0,makes.length-1)]
  model = models[randomIntFromInterval(0,makes.length-1)]

  mycar = new Model(make, model);
  console.log(mycar.show())
} 
```