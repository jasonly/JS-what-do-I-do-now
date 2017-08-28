# arrays

## operations

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

## interesting things
Since Arrays are objects, you can add properties to it and it wouldn't count towards the length of the array. Don't make the mistake of thinking you're adding to the array when you're adding a property.

```js
pokemonArray.grass = 'bulbasaur';
```

Inspecting the array will make it clear that `bubasaur` is part of the array but can't be accessed using any of the conventional methods.

## loops
You can loop through arrays using a for or while loop.

```js
const pokemonArray = ['pikachu', 'squirtle', 'bubasaur', 'charmander'];

// for loop
for (let i = 0; i < pokemonArray.length; i++) {
  console.log(pokemonArray[i]);
}

// while loop
while (pokemonArray.length) {
  let pokmans = pokemonArray.pop(); // or whatever methods
  consolelog(pokmans);
}
```
