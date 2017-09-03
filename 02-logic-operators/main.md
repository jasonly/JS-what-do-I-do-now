# LOGIC OPERATORS

JavaScript will evaluate things using operators. Things will get evaluated to either true or false. Also known as boolean algebra.

|               | Symbol           |
| ------------- |:----------------:|
| and           | &&               |
| or            | &#124;&#124;     |
| not           | !                |
| equality | == |
| identity | === |

When writing functions it's often useful to see if certain conditions evaluate to either true or false. Usually this is handled with an `if` statement.

```js
if (pokemonType === 'lightning' || pokemonType === 'water') {
  // do things for either lightning or water type pokemon
}
```

## things to watch out for

- The use of `==`, could possibly cause unexpected bugs. For example if you're looping through an array of pokemon objects and your logic gate checks for age, someone
- The use of `===`, can be true if both objects that are being checked have the same reference

```js
const pokemonArray = ['pikachu', 'squirtle', 'bubasaur', 'charmander'];
const other = ['pikachu', 'squirtle', 'bubasaur', 'charmander'];
const referencePokemonArray = pokemonArray;

// which of these below return true?
// pokemonArray === other
// pokemonArray === referencePokemonArray;
```
- Anyway there are a lot of quirks and they're real weird but not super useful to know about

## putting some of it together

Don't worry if this seems a little foreign we'll go into writing functions in the next part but for now I wrote out a skeleton and all you really need to do is loop through and use a logical operator.

- `console.log()` for logging things
- `${}` look up and read about es6 template literals

```js
const pokemonData = [
  {
    name: 'pikachu',
    type: 'lightning',
    hp: 100,
    sp: 150,
    moves: [],
  },
  {
    name: 'squirtle',
    type: 'water',
    hp: 101,
    sp: 101,
    moves: [],
  },
  {
    name: 'bulbasaur',
    type: 'lightning',
    hp: 102,
    sp: 101,
    moves: [],
  },
  {
    name: 'charmander',
    type: 'lightning',
    hp: 103,
    sp: 104,
    moves: [],
  }
];

// given an array of Pokemon objects called `pokemonData` loop through and log only bulbasaur object's key value pairs.

// example input:
// logPokemonData(pokemonData, 'bulbasaur');

// expected output:
// name: 'bulbasaur'
// type: 'lightning'
// hp: 102
// sp: 101
// moves: []

let logPokemonData = (pokemonData, name) => {
  // do stuff here

  // loop through pokemonData
  // if the name is equal to bulbasaur then
     // loop through that object
        // log the key value pairs in the object using console.log and template literals
};

// your function call
logPokemonData(pokemonData, 'bulbasaur');
```
