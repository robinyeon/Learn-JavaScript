## Object shorthand
```
const age = 18;
const person = {
    name: "John",
    age: age
}
```
->
```
const age = 18;
const person = {
    name: "John",
    age
}
```
Because the property name is the same as the name of the variable used as its value, then you can drop the `: age` so you're left only with `age`.

```
const isAdmin = false;
const darkMode = true;

const settings = {
    isAdmin,
    darkMode
};

console.log(settings); //{isAdmin: false, darkMode: true}
```

<br/>

## Debugging tip
There are several `console.log` calls because we are trying to debug our code.    
However, it will be tough for us to map on the console which value corresponds to which `console.log` call.

To fix that, you can wrap every variable inside the console.log call with {} so that the code becomes as follows:
```
const sum = (a, b) => {
    console.log({a}); // {a: 1}
    console.log({b}); // {b: 3}
    let total = a + b;
    console.log({total}); // {total: 4}
    return total;
}

// Sample usage
sum(1, 3);
```
You will be able to see the name of the variable that you were trying to log, alongside its value.
The benefit here is that, instead of logging `a`, you are logging `{a: a}`.

<br/>

## [Destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#object_destructuring) & Concatenation
- Destructuring with **default value** `=`
- Destructure and **rename** `:`

<br/>

## Concatenate objects
```
const firstPerson = {
    name: "Sam",
    age: 18
}

const secondPerson = {
    age: 25,
    type: "admin"
}

const mergedObjects = {...firstPerson, ...secondPerson};
console.log(mergedObjects); // {name: "Sam", age: 25, type: "admin"}
```
- Regarding the `age`, since it exists in both objects, only the 2nd one persisted.
- This is why the order of the objects when spreading them matters.









