## Array to string
Use ```.join()``` to join the array elements into one string.

### Applying it to HTML
e.g.
```
const html = `<ul>
    ${users.map(user => `<li>${user.name}</li>`).join("")}
    </ul>`;
    
console.log(html); // <ul> <li>Sam Doe</li><li>Alex Blue</li> </ul>
```
- What's very important here is the ```.join("")```
- If you forget this, you will get the following HTML: ```<ul><li>Sam Doe</li>,<li>Alex Blue</li></ul>```
  - automattically insert a comma after every array item
  - Instead, you want to convert the array into a string yourself. You can do that by calling .join("") with an empty string as glue. (without comma```,```)

<br/>

## Array.every(callback)
The Array ```.every(callback)``` method returns ```true``` when **every** item in the array satisfies the condition provided in the callback.
```
const numbers = [15, 10, 20];

const allAbove10 = numbers.every(number => number >= 10); // true
const allAbove15 = numbers.every(number => number >= 15); // false
```

<br/>

## Array.some(callback)
The Array ```.some(callback)``` method returns ```true``` when **at least one** item in the array satisfies the condition provided in the callback.
```
const numbers = [15, 10, 20];

const someOver18 = numbers.some(number => number >= 18); // true
const someUnder10 = numbers.some(number => number < 10); // false
```

<br/>

## Deleting items
### 1. set the array's length to 0:
```
const items = ["Pen", "Paper"];
items.length = 0;

console.log(items); // []
```

### 2. Array.splice()
fyi)        
- ```str.split(seperator[, limit])```     
- ```arr.slice(begin[, end])```       
- ```.splice(start[, deleteCount])``` removes items from the array from the ```start``` index. The number of items it will remove is specified by ```deleteCount```.
- If you omit ```deleteCount```, it will remove all the items as of the ```start``` index.
```
const items = ["Pen", "Paper", "Staples"];
const deletedItem = items.splice(0, 1); // removes one element at index 0
console.log(deletedItem); // ["Pen"]

console.log(items); // ["Paper", "Staples"]
```













