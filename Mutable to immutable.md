- When immutability is required (because of a front-end framework/library or because you don't want to update the original array/object), you will need to make a copy of it with the **`...` operator**.     
- This copy is called *shallow* copy because it only goes 1 level deep.       
- This means that for an array of objects if you make an update to the objects in the new array, the objects in the old array will still be updated.

## Immutable arrays
```
/**
 * @param {string[]} apps
 */
const cloneApps = apps => {
    return [...apps];
}

const originalApps = ["Calculator", "Phone"];
const copiedApps = cloneApps(originalApps);
console.log(copiedApps); // should be ["Calculator", "Phone"]
console.log(copiedApps === originalApps); // should be false (because it's a copy/clone)

```

<br/>

## Immutable objects
### Immutable update
```
const user = {
    id: 1,
    age: 23
};
const clonedUser = {
    ...user,
    age: user.age + 1
};
console.log(clonedUser); // {id: 1, age: 24} (new object not related to 'user')
```
- Notice how the `age : user.age + 1` overrides the previous value of the `age` property.

### Immutable delete
```
const book = {
    id: 1,
    title: "Harry Potter",
    year: 2017,
    rating: 4.5
}

// GOOD: immutable
const {year, ...rest} = book;
console.log(rest); // { id: 1, title: "Harry Potter", rating: 4.5}
```
- Notice how we ask JavaScript to destructure the rest of the object with `...rest`.
- This means combining all the other key/values in a new object called `rest`.
- So we end up with `rest` which is an immutable copy of `book` excluding the `year` property.
