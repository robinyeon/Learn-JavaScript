- String ```.trim()``` removes all leading and trailing space characters.
- String ```.startsWith(substring)``` returns ```true``` when the ```substring``` is found at the **beginning** of the string, and ```false``` otherwise.
- String ```.endsWith(substring)``` works the same but for the **end** of the string.
- String ```.includes(substring)``` returns ```true``` when the ```substrin```g can be found anywhere in the string, and ```false``` otherwise.

<br/>

### String.split(seperator)
The ```.split(separator)``` method divides the **string into an array** by splitting it with the ```separator``` you provide. For example:
```
let apps = "Calculator,Phone,Contacts";
let appsArray = apps.split(",");
console.log(appsArray); // ["Calculator", "Phone", "Contacts"]
```
- Reminder that the opposite of ```String.split(separator)``` would be ```Array.join(glue)```.

### String.replace(search,replace)
The ```.replace(search, replace)``` method returns a new string where the **first** occurrence of the ```search``` parameter you provide is replaced by the ```replace``` parameter, for example:
```
const message = "You are welcome.";
message.replace(" ", "_"); // "You_are welcome";
console.log(message); // "You are welcome" (original string is not changed)
```

### String.replaceAll(search, replace)
This method works like the one above, except that it will replace **all occurrences**.
```
const message = "You are welcome.";
message.replaceAll(" ", "_"); // "You_are_welcome";
console.log(message); // "You are welcome" (original string is not changed)
```

<br/>

## slug
In computer science, a *slug* is a string used to identify a certain item. Oftentimes, this slug is used in the URL for Search Engine Optimization and better user experience.  

Let's say you've got a product called: ```"Easy assembly dining table"```. We cannot use this name in the URL bar because it contains spaces (it won't look nice, for example ```https://example.com/item/Easy assembly dining table```).     

This is why we use a slug that looks like this:     
```easy-assembly-dining-table``` so the URL becomes: ```https://example.com/item/easy-assembly-dining-table```.
