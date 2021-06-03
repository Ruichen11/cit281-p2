# CIT281 Project-2

Purpose of this project:
- To gain experience writing and executing non-web server Node.js JS code
- gain experience refactoring JS code 
- gain experience using git using CLI and VSCode source control 


### Project task:

1. Refactoring Project 1 Code:

``` // Returns a random number between min (inclusive) and max (exclusive)
function getRandomInteger(min, max) {
    return Math.floor(Math.random() * (max - min) + min);
}
const alphabet = "abcdefghijklmnopqrstuvwxyz".split("");
let result = "";
for (let i = 0; i < getRandomInteger(10, 21); i++) {
    result += alphabet[getRandomInteger(1, alphabet.length - 1)];
}
console.log(result);
```
2. Create new Function "getRandomLetter() that return a single, random, lowercase letter. 
``` 
// Returns a random lowercase letter
function getRandomLetter() {
    const alphabet = "abcdefghijklmnopqrstuvwxyz".split("");
    // 0 - 26 because of getRandomInteger() max parameter
    return alphabet[getRandomInteger(0, alphabet.length)];
}
``` 
3. Create function "getRandomString(minLength, MaxLength) that will return the random length string. 
``` 
// Return a string of random length comprising random lowercase letters
function getRandomString(minLength, maxLength) {
    let result = "";
    let lengthOfResult = getRandomInteger(minLength, maxLength + 1);
    for (let i = 0; i < lengthOfResult; i++) {
        result += getRandomLetter();
    }
    return result;
}
console.log(getRandomString(10, 20));
``` 

4. Recreate all function using function expressions rather than function defintions:
``` 
// Returns a random number between min (inclusive) and max (exclusive)
const getRandomInteger = function(min, max) {
    return Math.floor(Math.random() * (max - min) + min);
}

// Returns a random lowercase letter
const getRandomLetter = function() {
    const alphabet = "abcdefghijklmnopqrstuvwxyz".split("");
    return alphabet[getRandomInteger(0, alphabet.length-1)];
}

// Return a string of random length comprising random lowercase letters
const getRandomString = function(minLength, maxLength) {
    let result = "";
    let lengthOfResult = getRandomInteger(minLength, maxLength + 1);
    for (let i = 0; i < lengthOfResult; i++) {
        result += getRandomLetter();
    }
    return result;
}

console.log(getRandomString(10, 20));
``` 

### What I learned: 
- Learned to refactor JS code from previous project 
- Use git via VSCode to create a .gitignore file
- Gain experience creating JS code. 
