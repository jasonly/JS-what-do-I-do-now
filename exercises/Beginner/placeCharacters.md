# Place character between X number of characters in a string

- Simple implementation

```js
let string = 'String';

function placeCharacters(str, amount) {
    let newString = '';
    let ourAmount = 0;
    
    for(let i = 0; i < str.length; i++) {
        if(ourAmount < amount) {
            newString += str[i];
            ourAmount++;
        } else {
            ourAmount = 1;
            newString += '?';
            newString += str[i];
        }
    }
    
    return newString;
}


console.log(placeCharacters(string, 2)); // St?ri?ng
