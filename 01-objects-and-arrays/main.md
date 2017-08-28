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
