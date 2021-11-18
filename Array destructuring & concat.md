## Array destructuring
```
const dimensions = [20, 5]

// create variables
const width = dimensions[0];
const height = dimensions[1];

// log them
console.log(width); //20
console.log(height); //5
```
The above code can be rewritten using the new array destructuring syntax as follows:
```
const dimensions = [20, 5]

// create variables
const [width, height] = dimensions;

// log them
console.log(width); //20
console.log(height); //5
```

- Array destructuring is syntactic sugar (meaning that it makes your code look easier to read)
- The order in the `[]` matters for array destructuring as the first variable will correspond to the first item in the array(index 0), the second variable name will correspond to the second item in the array (index 1), and so on.
- You can identify array destructuring when you see the square bracket`[]` on the left side of the equal sign`=`.

<br/>

## Array concatenation 
- You can concatenate/merge several arrays into a new array using the `...` concatenation syntax.
