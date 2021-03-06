# FUNCTIONS

Self contained logic for doing things. These things should be simple tasks, and ultimately complex function is a collection of simple tasks.

## structure

Functions are composed of a few things:
- `name` or `reference`, allows you to call the function using the declared name or provided reference.
  - If you don't use a `name` then your function is known as an anonymous function.
- `constructor`, functions are created using the `function` constructor.
- `parameter`, when a parameter is set a variable is defined with that parameter reference.
- `argument`, the parameter reference is set as the argument passed in.

| Parts            | Names            |
| ---------------- |------------------|
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

// referenced function (anonymous function)
const pokemonFunc = function(ref) {
  console.log(ref);
};

// what if you wrote a referenced and named function (why do you think this might be weird)

// es6
// these are sweet, they do some conveniences such as a lexically scoped this
const pokemonFunc = (ref) => {
  console.log(ref);
};

// they all can be called this way
pokemonFunc('oh hey'); // 'oh hey'
```

There are many intricacies to writing functions and such, it's a lot to cover but these are it's most pure forms.

## practice

- create a function that adds two numbers together

```js
function add(n1, n2) {

}

add(2, 2) //4
```

- create a function that subtracts two numbers
- create a function that divides two numbers
- create a function that takes the power of two numbers

## object oriented programming and structure

So far we've only been tying primitive values to objects, but you can actually store functions too! JavaScript also supports prototyping and other inheritance patterns. We'll look at those [next](https://github.com/jasonly/JS-what-do-I-do-now/blob/master/03-functions/oop.md).
