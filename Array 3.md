## Array to string
Use ```.join()``` to join the array elements into one string.
### Applying it to HTML
e.g.
```
const html = `<ul>
    ${users.map(user => `<li>${user.name}</li>`).join("")}
    </ul>`;
    
console.log(html); // <ul> <li>Sam Doe</li><li>Alex Blue</li> </ul>
```
- What's very important here is the ```.join("")```
- If you forget this, you will get the following HTML: ```<ul><li>Sam Doe</li>,<li>Alex Blue</li></ul>```
  - automattically insert a comma after every array item
  - Instead, you want to convert the array into a string yourself. You can do that by calling .join("") with an empty string as glue.
