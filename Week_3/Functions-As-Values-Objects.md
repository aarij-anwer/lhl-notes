# Functions as Values and Objects

Functions can be assigned to variables, which means they are values! Here's an example of a function being treated like a value.

```
// The function below is being defined and assigned to a variable myFunc!
const myFunc = function() {
  console.log('Hello from myFunc!');
}

// We can now call myFunc() with the () syntax.
myFunc()

// We can also assign that value to other variables!
const anotherVar = myFunc; 

// And call them the same way
anotherVar() // => Same as myFunc()!
```

Since this is the case, they can also be stored as values in objects! For example:

```
const someObject = {
  foo: 1,
  bar: function() {
    console.log("hello!");
  }
}

someObject.bar();
```

Semantically speaking, `bar` is a method on the object `someObject`.