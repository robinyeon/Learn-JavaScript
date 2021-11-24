## Optional chaining
- Optional chaining allows you to access a property deep within an object without risking an error if one of the properties is `null` or `undefined`.
- 있으면 값 보이고 없으면 `undefined`
- In case one of the properties is `null` or `undefined`, then the `?.` will short-circuit to `undefined`
```
const user = {
    details: {
        name: {
            firstName: "Sam"
        }
    },
    data: null
}

user.details?.name?.firstName; // "Sam"
user.data?.id; // undefined
user.children?.names; // undefined
user.details?.parent?.firstName; // undefined
```
- You **cannot** use optional chaining on an object that may not exist. The object **has** to exist. Optional chaining is only used to access a property that may or may not exist.
  - In case you're not sure whether `user` is an object, then you write `user?.details?.name`.
  - However, you still have to make sure that there is a **variable** `user` defined, or else you will get an error.

<br/>

## Optional chaining (advanced)

### Optional chaining can be used for arrays. The syntax is `?.[index]`
```
const data = {
    temperatures: [-3, 14, 4]
}

let firstValue = undefined;
if (data.temperatures) {
    firstValue = data.temperatures[0];
}
```
can refactor into:
```
const firstValue = data.temperature?.[0];
```

### Optional chaining can be used for funcitons. The syntax is `?.functionName()`
```
const person = {
    age: 43,
    name: "Sam"
};

let upperCasedName = person.name; // might be undefined
if (person.name) {
    upperCasedName = person.name.toUpperCase();
}
```
can refactor into: 
```
const upperCasedName = person.name?.toUpperCase();
```
- Optional chaining 없이는 *Cannot read property 'toUpperCase' of undefined.* 같은 에러가 나왔겠지만, optional chaining helps you avoid these errors by returning `undefined`.

### No optional chaining for assignment
- Optional chaining is *only* used for **reading**.
- It **cannot** be used for assignment.
```
// invalid
// ❌ Syntax Error 
settings?.theme = "dark";
```

### Do not overuse optional chaining
> *그럼 **dot notation** 대신 매번 써도 되는것 아닌가?*
- Over-using it may lead to unexpected bugs and poor code quality
- When `?.` in the code, it means that there's a moderate chance that the value returns `undefined`.
- In turn, this means that we should be handling the case when it returns `undefined`.







