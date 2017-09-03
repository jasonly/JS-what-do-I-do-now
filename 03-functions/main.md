# FUNCTIONS

Self contained logic for doing things. These things should be simple tasks, and ultimately a complex function is most likely made up of multiple simple tasks.

Functions are made up of a few things:
- `name` or `reference`, allows you to call the function using the declared name or provided reference.
  - if you don't use a `name` then your function is known as an anonymous function
- `constructor`, functions are created using the `function` constructor.
- `parameter`, when a parameter is set a variable is defined with that parameter reference.
- `argument`, the parameter reference is set as the argument passed in.

# structure

| Parts            | Names            |
| ---------------- |-----------------:|
| name / reference | pokemonFunc      |
| constructor      | function         |
| parameter        | ref              |
| argument         | 'oh hey'         |
| operations       | console.log(ref) |

```js
// es5
// named function
function pokemonFunc(ref) {
  console.log(ref);
};

// referenced function
const pokemonFunc = function(ref) {
  console.log(ref);
};


// es6
// these are sweet, they do some conveniences such as a lexically scoped this
const pokemonFunc = (ref) => {
  console.log(ref);
};

// they all can be called this way
pokemonFunc('oh hey'); // 'oh hey'
```
