# `this`

`this` is a special keyword within javascript. It has different values depending on where it is used.

`this` wants to refer to an owner object.

If this is used in a method then it is happy and can refer to the object that the method exists in. 

```
const obj = { 
  thing: 1, 
  myFunc: function () { 
    console.log(this); 
  }, 
}; // this refers to obj We can also call upon properties

obj.myFunc(); //{ thing: 1, myFunc: [Function: myFunc] }
```

```
const dog = {
  age: 2,
  breed: "Labrador",
  furColor: "Grey",
  size: "Medium",
  howOldIsThisDog: function(){
    console.log(this.age)
  }
}
dog.howOldIsThisDog() //2
```