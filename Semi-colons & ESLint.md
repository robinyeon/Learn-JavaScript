## Code style
- Code style is the set of rules and guidelines that a certain team/person/company uses while developing a project.
- Having a code style can make your code less prone to bugs, prevent some bugs ahead of tiem, all while making your code more homogeneous.
- Having homogeneous code in a big team is important to improve the long-term maintenance of the project.

### ESLint
- The most popular tool for enforcing/recommending certain code styles in JavaScript is called [ESlint](https://eslint.org/)

### Setup ESLint for VSCode
1. Open VSCode, click on the Extensions tab and then search for ESLint and click on the first result "ESLint".
2. Click on the Install button.
3. At the root of your project, create a file called `.eslintrc.json` (don't forget the leading dot character)
4. Write the below inside this file and save it
```
{
  "extends": "eslint:recommended",
  "parserOptions": {
    "ecmaVersion": 2021
  }
}
```
- This uses the recommended ESLint rules which you can find on the [rules](https://eslint.org/docs/rules/) page. All the ones marked with a check `v` are included in the `eslint:recommended` configuration.

## ASI (Automatic Semi-colon Insertion)
- Some specific statements in JavaScript **need** to end with a semi-colon. So, if the programmer left them out, the JavaScript engine will **automatically place a semi-colon*.
- Only applies in very specific cases. 
  - `let/const` variable declarations
  - `import/export` statements
  - `return`
- The most common example of ASI is with the `return` keyword (mostly while writing React code with JSX).
```
function App() {
    return ; // similar to return undefined
        <div>
            Hello
        </div>
}
```
- The solution would be to have the return on one line: `return <div>` and then the rest can go on the different lines.
- or you can solve it by opening a parenthesis after the `return` keyword.
```
function App() {
    return (
        <div>
            Hello
        </div>
    )
}
```
