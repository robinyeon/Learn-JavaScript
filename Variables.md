## let
Variables defined with let, can be re-assigned later on:
```
let language = "C++";
language = "JavaScript";
```

<br/>

## const
Variables defined with const cannot be re-assigned. This means you can use the = sign once when the variable is defined.
```
const language = "C++"; // Cannot be re-assigned anymore
console.log(language); // "C++"

language = "Python" // ❌ Type error: this will break your script 
```
- An important note about ```const``` is that it does **not** create a Constant or an Immutable value. This will be thoroughly explained once we learn about arrays & objects. What you need to know, for now, is that you can only use the equal sign once, but you can still change elements **inside** an array or object.
- The benefit of using ```const``` is that once a variable is an array, it will always be an array (but the elements inside the array might change). This allows you to confidently use array methods on that variable because you know it will always be of type array.

<br/>

## let vs const
- Always go with ```const```, until you realize that you need to be able to re-assign the variable later on, then switch it to ```let```.   
- For example, when you define a variable count (that you expect to increment), you will immediately realize that and use ```let```.

***Avoid using ```var``` when defining variables. Use ```let``` or ```const``` instead.***

<br/>

## [MDN_blcok](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/block)
### Variables declared with ```var``` **do not** have block scope.
Variables introduced within a block are scoped to the containing function or script, and the effects of setting them persis beyond the block itself.
```This logs 2 because the var x statement within the block is in the same scope as the var x statement before the block.
var x = 1;
{
  var x = 2;
}
console.log(x); // logs 2
```
- This logs 2 because the ```var x``` statement within the block is in the same scope as the ```var x``` statement before the block.

### Identifiers declared with ```let``` and ```const``` **do have** block scope.
```
let x = 1;
{
  let x = 2;
}
console.log(x); // logs 1
```
The ```x = 2``` is limited in scope to the block in which it was defined.


```
const c = 1;
{
  const c = 2;
}
console.log(c); // logs 1 and does not throw SyntaxError...
```
- Note that the block-scoped ```const c = 2``` does *not* throw a ```SyntaxError: Identifier 'c' has already been declared``` because it can be declared uniquely within the block.

