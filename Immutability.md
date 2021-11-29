## How array/object equality works in JavaScript.

```
[] === []; //false
{} === {}; //false
[10] === [10]; //false
{key: "something"} === {key: "something"}; //false
```
- Arrays & Objects are both considered **objects** in JavaScript.
  - When you write `[]`, it's the same as creating a new **instance** of `Array`.
  - When you write `{}`, it's the same as creating a new **instance** of `Object`.

<br/>

```
new Array(); // creates []
new Object(); // creates {}
```
The previous examples with this new syntax:
```
new Array() === new Array(); //false
new Object() === new Object(); //false

const arr1 = new Array();
arr1.push(10);
const arr2 = new Array();
arr2.push(10);
arr1 === arr2; //false

const obj1 = new Object();
obj1.key = "something";
const obj2 = new Object();
obj2.key = "something";
obj1 === obj2; //false
```
- Every time you call `new Array()` you get a new instance, which means `new Array()` is certainly not the same as `new Array()` because they both are different instances.
- As in, we expected `[] === []` to be true because they are both empty arrays, but the way JavaScript works is different as it's checking if they are the same instance.

<br/>

## Object assignment
```
const firstArray = [];
const secondArray = firstArray; // secondArray now points to firstArray
console.log(firstArray); // []
console.log(secondArray); // []

firstArray.push(10);
console.log(firstArray); // [10]
console.log(secondArray); // [10]
```
- Why does `secondArray` also contain `10` now?
- That's because when we created `secondArray = firstArray`, we are **not copying firstArray, but rather only creating a reference to it**.
- This means `firstArray` and `secondArray` are now referring to the same value. Technically we say they are referencing the same place in the memory.
- So whenever you change the value in any of the 2 variables, then both `firstArray`, and `secondArray` will return the same value that has been updated.

<br/>

## Deep Equal
- Triple equal `===` is comparing the references rather than the values. If you'd like to compare by values, then what you're looking for is called **deep equal**.
- Deep equal is too slow to be used in front-end frameworks/libraries, which is why most of them rely on checking equality with `===`.
- An immutable object is an object that cannot be changed. Every update creates a new value, leaving the old one untouched.












