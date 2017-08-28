# OBJECTS AND ARRAYS

## what

- Both Arrays and Objects are Objects

```js
const pokemonArray = ['pikachu', 'eevee'];
const pokemonObject = {
  0: 'pikachu',
  1: 'eevee',
};
```

- They're known as associative arrays, which means that they're things that hold name value pairs.

```js
// you could technically think of pokemon as an object that has a key of indicies
pokemonArray[0] // pikachu
pokemonArray['0'] // oh shoot this works too

// for objects
pokemonArray[1] // eevee
pokemonArray['1'] // ok so what
```

## differences

|               | Arrays           | Objects  |
| ------------- |:----------------:| --------:|
| Syntax        | []               | {}       |
| Order         | Ordered by increasing indexes | Unordered uses properties |
| Methods | Convenience array methods, such as push, pop, shift, and unshift | None really |

## array operations

1) Create a pokemonArray (there are other ways to do this but I like this one the most)

```js
const pokemonArray = [];
```

2) Add some pokemon you like using bracket notation and selecting an index

```js
pokemonArray[0] = 'pichu';
pokemonArray['1'] = 'eevee';
```

3) Add some pokemon you like using as many array methods you can think of

```js
pokemonArray.push('charmader');
pokemonArray.unshift('squirtle');
pokemonArray = pokemonArray.concat(['bulbasaur']);
pokemonArray.splice(1, 0, 'mew', 'mewTwo')
```

4) Access the first pokemon in your array using bracket notation
5) Access the second pokemon in your array  using bracket notation and a string
6) Access the rest of the pokemon in your array with as many array methods you can think of
```js
// pop
// shift
// splice
```

## object operations

1) Create a pokemonObject

```js
const pokemonObject = {};
```

2) Add some pokemon you like using bracket notation

```js
// this looks familiar and it works but we shouldn't do this because they're special characters
// pokemonObject[0] = 'squirtle';
// pokemonObject['1'] = 'charmander';

// instead let's give them property keys
pokemonObject['water'] = 'squirtle';
pokemonObject['fire'] = 'charmander';
```

3) Dot notation

```js
pokemonObject.grass = 'bulbasaur';
```

4) Since objects don't have an order, access `squirtle` using bracket notation passing in a string
5) Access `charmander` using bracket notation without a string
6) Access `bulbasaur` using dot notation
