## Implicit return
When you forget to write ```return``` in a function in JavaScript, you get an implicit ```return undefined```.      
**The word implicit here means that it is inferred but not specifically expressed.**(함축적인)    
Meaning that there was no ```return undefined``` but we end up getting ```undefined``` as a result.     

Here are the conditions for implicit return:    
1. Your function should be an arrow function.
2. The function body should be **only one line**. This means you have to remove the curly braces.
3. You have to remove the ```return``` keyword because the function body is one line.
- Only use implicit return when the function body is one line and short. Never sacrifice code readability and clarity in order to use a certain feature.
```
const sum = (a, b) => {
    a + b;
}

sum(1, 3); // undefined
```
to
```
// this works 👍 (implicit return)
const sum = (a, b) => a + b;

sum(1, 3); // 4
```

<br/>

```
const isLegal = (age) => {
    return age >= 18;
}
```
to
```
const isLegal = (age) => age >= 18;
```
then we can drop the parentheses:
```
const isLegal = age => age >= 18;
```

## Applying methods
### .filter()
```
const numbers = [9, 5, 14, 3, 11];

const numbersAboveTen = numbers.filter(function(number) {
    return number >= 10;
});
console.log(numbersAboveTen); // [14, 11]
```
to
```
numbers.filter(number => number >= 10);
```
- how to read: *We filter the ```numbers``` where the ```number``` is bigger than or equals 10.*




