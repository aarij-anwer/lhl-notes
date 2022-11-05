# Functions

In programming language design, a first-class object, in a given programming language is an entity which supports all the operations generally available to other entities. These operations typically include being passed as an argument, returned from a function, and assigned to a variable.

**One of the distinctive things about JavaScript is that functions are first-class objects.**

This means that:

1. Functions can be stored in variables
2. Functions can be passed as an argument
3. Functions can hold properties

```
const myFn = function() {
  console.log("I am function.");
}

myFn.someAttribute = 42;
console.log(myFn.someAttribute);

function runner(f) {
  f();  //Anytime you see a function with a (), we are invoking it.
}

runner(myFn);
```

## Anonymous Functions

A nameless function defined inline or assigned to a variable. It may or may not be used as a callback function.

```
const lighthouses = ["Gibraltar Point", "Peggy's Point", "Cove Island", "Discovery Island", "Cape Scott", "Point Clark", "Kincardine"];

function returnLenght (element) {
  return element.length;
}

console.log(lighthouses.map((element) => returnLenght(element)));
console.log(lighthouses.map((element) => { return element.length; }));
console.log(lighthouses.map(element => element.length));

```

The output is:

```
[
  15, 13, 11, 16,
  10, 11, 10
]
[
  15, 13, 11, 16,
  10, 11, 10
]
[
  15, 13, 11, 16,
  10, 11, 10
]
```