## Arrays
Name arrays in the plural as they can contain more than one item. This will prove to be especially useful once we need to iterate over an array.    

### .length property
Note that **.length** is a property (pre-computed value) and not a function. That's why you should not have ```()``` after it.    

### Array.push()
- ```Array.push()``` returns the new **length** of the array.
- ```.push()``` will add an item to the array but also return the new length of the array.
```
const animals = ['pigs', 'goats', 'sheep'];

const count = animals.push('cows');
console.log(count);
// expected output: 4
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows"]

animals.push('chickens', 'cats', 'dogs');
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows", "chickens", "cats", "dogs"]
``` 

<br/>

## Arrays & const
```
const numbers = []; // start with empty array
numbers.push(10); // returns 1 (new length of array)
console.log(numbers); // [10] (still an array but content changed)
numbers.push(20); // returns 2 (new length of array)
console.log(numbers); // [10, 20] (still an array but content changed)
```
Even though the variable ```numbers``` was defined with ```const```, we were able to push new data into it.       
That's because ```const``` means you can only **assign the variable once** when it's defined. But it doesn't mean the variable is immutable. Its content can change.      

### What's the benefit of declaring it as a const?
The benefit is that once you define it as an array, it will always stay as an array which means you can safely call array methods on it.    
However, the array content can change.  

<br/>

## Array forEach
```
const grades = [10, 8, 13];

grades.forEach(function(grade) {
    // do something with individual grade
    console.log(grade);
});
```
- Always start with a ```console.log()``` inside your ```.forEach``` so that you can visualize the shift from array to array item.

### How does it know that it's "grade"
How does JavaScript know that ```grades``` becomes ```grade``` in the callback parameter. The answer is, it doesn't.    
JavaScript doesn't really care what you call your variables, it will always (in the case of ```.forEach```) look for the **first parameter** you define in your callback function and pass to it the correct value.   
But you should always give clear variable names.    

<br/>

## Return confusion
### Naming variables
Thus, it's always a good idea to use the plural for the array and singular for the item of the array.   
- grades => item is grade
- people => item is person


























