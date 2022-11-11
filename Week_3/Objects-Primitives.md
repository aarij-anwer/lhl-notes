# Objects and Primitives

Each primitive (excluding symbol which has weird rules) has a corresponding object constructor; you can see this clearly in the following example:

```
typeof(true); 
// "boolean" 
typeof(Boolean(true)); 
// => "boolean" 
typeof(new Boolean(true));
```

## Operations on Primitives

Here are some examples of calling String object properties, on a primitive string:

```
// some examples of String properties: 
const someString = "Lighthouse Labs"; 

console.log(someString.toUpperCase()); 
// => 'LIGHTHOUSE LABS'

console.log(someString.toLowerCase()); 
// => 'lighthouse labs'

console.log(someString.split("")); 
// => [ 'L', 'i', 'g', 'h', 't', 'h', 'o', 'u', 's', 'e', ' ', 'L', 'a', 'b', 's' ]
```

The primitive `someString` is type coerced into a String object, which then allows us to call the methods `toUpperCase()`, etc.