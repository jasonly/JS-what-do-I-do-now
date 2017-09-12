# Iterate through array of objects and convert to one-dimensional array

- Naive implementation

```js
let data = [
  {state: "CA"},
  {state: "CA"},
  {state: "IL"},
  {state: "MI"},
  {state: "al"},
  {state: "AZ"},
  {state: "AZ"}
];

// Iterate over keys of objects

function iterateKeys(set) {
    let arr = [];
    
    set.forEach((item) => {
        arr.push(Object.keys(item))
    });
    
    return arr;
}

console.log(iterateKeys(data));

// Iterate over values of objects

function iterateValues(set) {
    
    return set.map((item) => {
        for(let i in item) {
            if(item.hasOwnProperty(i)) {
                return item[i];
            }
        }
    });
}

console.log(iterateValues(data))
```
