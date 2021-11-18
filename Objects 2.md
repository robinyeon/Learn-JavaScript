## Reading dynamic property

```
const user = {
    id: 1,
    name: "Sam Green"
};

user.id; // 1
```
What if the property that you wanted to read was stored in a variable. For example:
```
const key = "id"; // the name of the property that we want to access on the user object

// ❌ this does NOT work
user.key; // undefined 
```
We cannot use the dot syntax here because the property is dynamic.    
When you write `user.key`, JavaScript will then look for a property called key which is not the case here.    
Instead, we need to get the value of the variable `key`, which is "id".     

For that, you have to use the square brckets as following:
```
const user = {
    id: 1,
    name: "Sam Green",
    age: 20
};

const key = "id";
user[key]; // 1
```

This works because `[key]` will **evaluate** the expression inside the square brackets.   
In this case, `key` that **evaluates** to `"id"`.     
So we end up reading the property `id` which returns 1 (because `user.id` is 1).    
헷갈린다면 `무엇을 평가하는가`로 구분해보기

### sample usage
```
const getValue = (user, keyToRead) => {
    return user[keyToRead];
}

// Sample usage
getValue({id: 2, name: "Sam"}, "name"); // "Sam"
getValue({id: 2, name: "Sam"}, "id"); // 2
```

<br/>

## Object.keys(obj)
- The `Object.keys(obj)` method returns an **array** of all the keys in the obj that you provide.
- 여기서의 `Object`는 `Number.parseInt()`의 `Number`와 같은 경우
  - The `Object` global variable contains methods that are relevant to objects.
```
const user = {
    id: 1,
    name: "Sam Green",
    age: 20
};

const keys = Object.keys(user);
console.log(keys); // ["id", "name", "age"]
```

<br/>

## Putting dynamic property & Object.key() together
```
const settings = {
    theme: "Dark",
    version: "2.4.1",
    beta: false
};

const keys = Object.keys(settings);
console.log(keys); // ["theme", "version", "beta"]
keys.forEach(key => {
    // log the value of every key dynamically
    console.log(settings[key]);
});
```
and follwing in the console:
```
"Dark"
"2.4.1"
false
```

<br/>

## Object methods

### `Object.values(obj)`
Returns an array of the values of an object.

### `Object entries(obj)`
Returns an array of arrays representing every key/value pair.
```
const user = {
    id: 1,
    name: "Sam Green",
    age: 20
};

const entries = Object.entries(user);
```
The entries variable will return the following array of arrays:
```
[
    ["id", 1],
    ["name", "Sam Green"],
    ["age", 20]
]
```













