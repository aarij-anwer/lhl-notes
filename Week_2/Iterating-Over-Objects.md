# Iterating Over Objects

The `for-in` loop is used to loop through the properties of an object. More specifically, it loops through each key.

The syntax for the for-in loop is:

```
for (let key in object) {
  // statement or block to execute for each key
}
```
In each repetition, one property from the object is associated to the variable (named key above), and the loop is continued until all of the properties of the object are depleted.

```
const object = { a: 1, b: 2, c: 3 };

for (const key in object) {
  console.log(`${key}: ${object[key]}`);
}

// expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```