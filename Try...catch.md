## Try...catch
- When a function call might fail, it's recommended that you wrap it with a `try...catch` block.
- This will allow you to recover from errors.     

```
console.log("Step 1");
nonExistentFunction(); // ❌ Uncaught ReferenceError: nonExistentFunction is not defined
console.log("Step 2");
```
- Notice that `"Step 2"` never gets logged to the console because there was an error and so the code stops executing.


### Things that might fail
```
console.log("Step 1");
try {
    nonExistentFunction();
} catch (error) {
    console.error(error); // Uncaught ReferenceError: nonExistentFunction is not defined
}
console.log("Step 2");
```
the code above will log the following to the console:
```
"Step 1"
Uncaught ReferenceError: nonExistentFunction is not defined
"Step 2"
```
- `console.error` is a function similar to `console.log` but instead, it has a severity level of **error**.
- If you end up filtering your logs in the console, you can distinguish between normal logs and the ones that have the level "error".

### What to do in the `catch` block?
- You can do whatever you want in the `catch` block.
