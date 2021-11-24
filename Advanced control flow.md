## Refactoring if conditions
```
const getPushMessage = status => {
    if (status === "received") {
        return "Restaurant started working on your order.";
    } else if (status === "prepared") {
        return "Driver is picking up your food."
    } else if (status === "en_route") {
        return "Driver is cycling your way!";
    } else if (status === "arrived") {
        return "Enjoy your food!";
    } else {
        return "Unknown status";
    }
}
```
can be refactored as follows: 
```
const getPushMessage = status => {
    const messages = {
        received: "Restaurant started working on your order.",
        prepared: "Driver is picking up your food.",
        en_route: "Driver is cycling your way!",
        arrived: "Enjoy your food!"
    };

    return messages[status] ?? "Unknown status";
}
```

<br/>

## Implicit conversion & [falsy values](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) 
- if문은 boolean값을 판단하는데, string이나 number가 주어진다면?:
```
const name = "Sam";
const number = 0;

if (name) {
    console.log("First condition");
}

if (number) {
    console.log("second condition")
}
```
- The code above will output `First condition` only.

### Implicit conversion
- The `if` statement expects a boolean. However, when you provide it with a value of another type, it will automatically convert it to a boolean. This is called implicit conversion because the conversion is occurring automatically.
### Falsy values
- In JavaScript, the values below will be converted to `false` and everything else will be converted to `true`:
  - false (is already a boolean)
  - null
  - undefined
  - 0
  - NaN
  - "" (empty string)

<br/>

## Logical NOT operator `!`
```
!true; // false
!false; // true
```


