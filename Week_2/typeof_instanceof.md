# `typeof` and `instanceof` to Check Object Types

```
const person = {
  name: "Paul",
  address: {
    street: "310 W 95th",
    city: "New York",
    zipCode: 10027
  },
  phoneNumbers: [123, 25421, 2141, 1251]
};
```

`typeof` will return whether it's an object or not. Yes, arrays are objects too.

```
typeof person["phoneNumbers"]; //returns object 
```

`instanceof` is more specific to differentiate between objects, arrays and primitives. 

```
person["phoneNumbers"] instanceof Object //true
person["phoneNumbers"] instanceof Array //true
person["phoneNumbers"] instanceof String //false
```

