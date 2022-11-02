# Objects

Anything not in that list (for example, a `Date`) is an Object. Objects are not primitive data types.

Objects, arrays, and functions are all objects!

## Key-Value Pair

Objects:

* Contain key-value pairs; each key maps to a value
* Contain keys which are always strings (or symbols, but it's less common and not important right now)
* Have unique keys; the same key cannot appear twice in an object
* Have their keys point to values which can be of any type

## Acessing Objects

```
const person = { firstName: "Khurram" };
person["firstName"];  //works
```

```
person.firstName;  //works
```

```
const person = { firstName: "Khurram" };
person[firstName];   // ReferenceError: firstName is not defined
```

If that variable name instead points to a string, then that can be an interesting way of accessing a key:

```
const person = { firstName: "Khurram" };
const propertyName = "firstName";
const firstName = person[propertyName]; // interpreted as person["firstName"], and therefore works fine :)
```

Object.keys() will return an array of the keys on an object

```
const person = {
  name: 'Paul',
  address: { street: '310 W 95th', city: 'New York', zipCode: 10027 },
  phoneNumbers: [ 123, 25421, 2141, 1251 ],
  dislikes: { food: 'spam', 'e-mail': 'spam' }
}
Object.keys(person) // [ 'name', 'address', 'phoneNumbers', 'dislikes' ]
```

Need to use a for-in loop to access values in object

```
for (var key in person) {
  if (person.hasOwnProperty(key)) {
    console.log('Key: ' + key + ' Value: ' + person[key]);
  }
}
```

## Using a Key Where the Object Doesn't Exist

It will return `undefined`. 

``` 
person["foo"];   //undefined
```

## Examples of Objects

Will create a new property/key-value pair:

```
const mary = { name: "Mary Sue" };
mary["name"] = "Mary Jane";
mary["age"]  = 22;
```

Objects within objects:

```
const person = {
  name: "Paul",
  address: {
    street: "310 W 95th",
    city: "New York",
    zipCode: 10027
  }
};
```
Keys with hypenated names need "":

```
person["dislikes"] = { food: "spam", "e-mail": "spam" };
```