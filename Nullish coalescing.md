## Nullish coalescing `??`
- The nullish coalescing `??` operator is a new operator introduced in JavaScript that allows you to *default* to a certain value when the left-hand side is a nullish value.
- A nullish value is a value that is either `null` or `undefined`.
```
const getName = name => {
    return name ?? "N/A";
}

console.log(getName("Sam")); // "Sam"
console.log(getName(undefined)); // "N/A"
console.log(getName(null)); // "N/A"
```
- This operator is useful to avoid showing `undefined` or `null` to the User Interface, which are often signs of bugs.

### Short circuit
- The nullish coalescing operator will short-circuit if the left-hand side returns a non-nullish value. This means that it will **not** execute the right-hand side.
- short circuit 작동시o -> `??`오른편은 작동x
```
const getPlaceholder = () => {
    console.log("getPlaceholder called");
    return "N/A";
}

const sayHello = name => {
    return `Hello ${name ?? getPlaceholder()}`;
}

console.log(sayHello("Sam")); // "Hello Sam"
```

### Variable must be defined
- You can only use nullish coalescing when the variable is defined.

<br/>

## Nullish coalescing (advanced)
- Nullish coalescing can be used with optional chaining. The main usage here is to safely access a property that could be nullish while also being able to default to a certain value.
```
let name = undefined;
if (user.details && user.details.name && user.details.name.firstName) {
    name = user.details.name.firstName;
} else {
    name = "N/A";
}
```
can be refactored as follows:
```
const name = user.details?.name?.firstName ?? "N/A";
```

<br/>

## null vs undefined
- `undefined` means that the value has not been defined yet.
- Whereas, `null` means that the value has been defined but is empty.
- In most scenarios, this distinction does not matter.
```
const user = {
    id: 1,
    name: "Sam",
    age: null
}

console.log(user.age); // null
console.log(user.birthday); // undefined
```
- We used `null` here to mean that the `age` property has been defined, but does not have a value yet.
- The `birthday` property has not been defined yet, which is why it returns `undefined`.
- Remember though, that the need to have this distinction is not very common.
