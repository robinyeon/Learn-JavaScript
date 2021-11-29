## Using array methods
- Calling the `.filter()` method on an array of objects will return an **array** containing the objects that pass the condition you specify in the callback.
- Calling the `.find()` method on an array of objects will return the **first object** that matches the condition you specify in the callback, or `undefined` if no objects satisfy the condition.
- Calling the `.some()` method on an array of objects will return true when **at least one item** in the array satisfies the condition you specified in the callback. Otherwise, it returns `false`.
- Calling the `.every()` method on an array of objects will return true when **every item** in the array satisfies the condition you specified in the callback. Otherwise, it returns `false`.

## Reducing array of objects
`.reduce()` with arrays of objects
- What's important is to do it step by step and add a `console.log(current)` and visualize that variable.
