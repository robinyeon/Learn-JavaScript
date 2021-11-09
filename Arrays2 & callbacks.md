#### Recap: property vs method
Properties are pre-computed values which is why they should not have () after them.   
On the other hand, methods requires the () because they perform an action.    

<br/>

## Array filter
- The ```.filter()``` method returns a new array that contains some of the items from the original array, based on the condition you specify.
- JavaScript will take your callback function and call it for every single item in the array.
- For the ```.filter()``` method, the result of the callback function matters. When it's ```true```, the item will be included in the resulting array. Otherwise, it won't.
- JavaScript cannot make a smart guess that the ```numbers``` array becomes the ```number``` parameter in your callback function. What it does is that it calls your callback function while giving a value for the **first parameter** that you specified.
- Use the **plural -> singular** naming convention when using the ```.filter()``` method.

<br/>

## Array find
The ```.find()``` method returns the first item which matches the condition that you specify. If no items were found, you will get back ```undefined```.

### ```.filter()``` vs ```.find()```
- The ```.filter()``` method **always** returns an array. Even if it matched one item or no items.
- The ```.find()``` method returns the first array item that matches the callback function or ```undefined```.
```
let numbers = [9, 5, 14, 3, 11];

// filter() ALWAYS returns an array
numbers.filter(function(number) {
    return number >= 12;
}); // [14]

// .find() returns the first match or undefined
numbers.find(function(number) {
    return number >= 12;
}); // 14
```
