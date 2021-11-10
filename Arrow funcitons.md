### Recap
A **parameter** is a variable in a function definition.     
When a function is called, the **arguments** are the data you pass into the method's parameters.

<br/>

## Default parameters
- When you call a function without providing a value for an expected argument, it will default to ```undefined```.
- The ```number``` parameter will receive a value of ```undefined``` so the function will return ```undefined + 1``` which results in ```NaN```.
```
function addOne(number) {
    return number + 1;
}

addOne(2); // 3
addOne(5); // 6
addOne(); // undefined
```

- Default parameters allow you to give a default value for one or more parameters that have not been provided when the function is called.
```
function addOne(number = 0) {
    return number + 1;
}

addOne(2); // 3
addOne(5); // 6
addOne(); // 1
```

<br/>

## Introductiokn to arrow functions
### 3 main benefits
1. It's shorter to write.
2. It uses lexical scope.
3. It can benefit from implicit return.

### From function to arrow function
normal function:
```
function sum(a, b) {
  return a+b;
}
```
then,
```
const sum = function(a,b) {
  return a+b;
}
```
convert that function into an arrow function in 2 steps:
1. remove the function keyword
2. add an arrow (```=``` and ```>```) btw the parameters ```(a, b)``` and the opening curly brace ```{```
```
const sum = (a, b) => {
  return a+b;
}
```

<br/>

## Revisiting rray methods
### forEach()
```
const grades = [1, 2, 3];

grades.forEach(function(grade){
  console.log(grade);
});
```
can be rewritten using arrow functions as following:
```
grade.forEach((grade) => {
  console.log(grade);
});
```
- Also, because the arrow function has **one** parameter, you are allowed to drop the parentheses ```()``` surrounding the parameter:
- This is only the case when you have **one** parameter. Multiple parameters have to be wrapped in parentheses ```()```.

### filter()
```
let numbers = [9, 5, 14, 3, 11];

let numbersAboveTen = numbers.filter(function(number) {
    return number >= 10;
});
console.log(numbersAboveTen); // [14, 11]
```
can be rewritten as:
```
let numbersAboveTen = numbers.filter((number) => {
  return number >= 10;
})
```


























