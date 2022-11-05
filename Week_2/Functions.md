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

## High Order Functions and Callbacks

High order functions follows one of these two rules:
1. Accepts one or more functions as arguments
2. Returns one or more functions as a result.

Callback is a function passed into another for later execution, OR is a function passed to a high order function.
