# Objects and the Spread Operator

Objects are created as references, just like in Java.

```
const carObjectOne = { color: “red”, type: “automatic” };
carObjectTwo = carObjectOne;
carObjectTwo.color = “green”; //will change carObjectOne
```

To fix this, use spread operator:

```
CarObjectTwo = {…carObjectOne};
```

## What else can … do?

The … spread operator is useful for many different routine tasks in JavaScript, including the following:
- Copying an array
- Concatenating or combining arrays
- Using Math functions
- Using an array as arguments
- Adding an item to a list
- Adding to state in React
- Combining objects
- Converting NodeList to an array
