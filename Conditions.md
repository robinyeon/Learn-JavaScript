## Advanced if
- Using an **if** condition, you can run a piece of code when the condition evaluates to ```true```.
- The syntax is ```if (condition)``` and then curly braces ```{}``` wrap the lines of code that correspond to this condition.
- The **else** keyword can be used to perform some other code based on all the other conditions not satisfied with the ```if```.
- When you have an ```if/else``` condition that returns two different results, it is possible to drop the ```else``` keyword.
- Always use triple equals (===) when comparing 2 values in JavaScript.

<br/>

## Returning booleans
```
function isPassing(grade) {
    if (grade >= 10) {
        return true;
    } else {
        return false;
    }
}

isPassing(12);
```
This is redundant because grade >= 10 on its own, evaluates to true or false depending on the grade. This means you don't need to wrap it with an if/else statement.    

That's why you can refactor it like this:
```
function isPassing(grade) {
    return grade >= 10;
}
```
**Refactoring is intended to improve the design, structure, and/or implementation of the software, while preserving its functionality.*
