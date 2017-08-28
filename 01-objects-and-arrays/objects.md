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

## loops
You can loop through arrays using a for or while loop.

```js
const pokemonArray = {
  lightning: 'pikachu',
  water: 'squirtle',
  grass: 'bubasaur',
  fire: 'charmander',
};

// for loop
for (let key in pokemonArray) {
  console.log(pokemonArray[key]);
}
```
