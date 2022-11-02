# Five Rules for Functions

1. Give your functions precise verb/action based names
2. Use `camelCasedNames` (like this one)
3. Properly indent the function code
4. Functions should focus on a single task: returning a value or causing a side effect. _Break your function into additional smaller functions if you find it doing two or more things_
  - One single task could be to compute and return a value (eg: zeroPad)
  - Another single task could be to perform a side effect such as logging a message to the screen (eg: printFarmInventory)
5. Data needed by Functions should be passed in as parameters/arguments (i.e. local scope) instead of being accessed directly