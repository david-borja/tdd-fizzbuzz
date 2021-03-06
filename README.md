TDD FizzBuzz Challenge done following [this video](https://www.youtube.com/watch?v=I27ZJU2_-Og) by Carlos Azaustre.

Install dependencies

```
npm i
```

Initial terminal scripts:

```
npm init -y
```

```
npm i -D jest
```

```
npx jest --init
```

- ✔ Would you like to use Jest when running "test" script in "package.json"? … yes
- ✔ Would you like to use Typescript for the configuration file? … no
- ✔ Choose the test environment that will be used for testing › node
- ✔ Do you want Jest to add coverage reports? … yes
- ✔ Which provider should be used to instrument code for coverage? › v8
- ✔ Automatically clear mock calls and instances between every test? … yes

In order to avoid running npm test each time, we can add the following to the scripts in the package.json:

```
"scripts": {
  "test:watch": "jest --watchAll"
}
```

After that, we do:

```
npm run test:watch
```

(Remember to have autoSave 'off' on VSCode)

We didn't add Babel to understand ES6 modules, so in order to link files we have to use this syntax:

```js
module.exports = fizzbuzz;
const fizzbuzz = require("./fizzbuzz");
```

instead of this one:

```js
export default fizzbuzz;
import fizzbuzz from "./fizzbuzz";
```
