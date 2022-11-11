# Object Oriented Concepts - `constructor`

```
class Pizza {

  constructor() {
    this.toppings = ["cheese"];
  }

  addTopping(topping) {
    this.toppings.push(topping);
  }

}

let pizza1 = new Pizza();
```

`Pizza` is the class. `pizza1` is an instance of the class. Instances can be created which have all the properties and methods defined in the class. `addTopping` is a method. 

## `constructor`

`constructor` is a special kind of method that gets executed when an object instance is created from a class. Everything inside the Pizza's constructor method will get run for the new instance of the class when we call new Pizza();
