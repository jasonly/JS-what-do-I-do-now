# Object Oriented

Objects can have more than primitive values attached to them.

```js
let calculator = {};

calculator.add = function(n1, n2){
  return n1 + n2;
};

// give it a shot with subtraction, division, and power.
```


## new



When a function is called with the new keyword, returns a new object with the `this` value pointing to it. These are also known as constructors.

```js
function Calculator() { // side note constructors are generally capitalized
  this.add = function(n1, n2){
    return n1 + n2;
  }

  this.subtract = function(){};
  this.divide = function(){};
  this.power = function(){};
}

var ti83ReeaaaalLite = new Calculator();
```

Interestingly `Calculator` can also be written in this way.

What is the difference between `ti83ReeaaaalLite.constructor.prototype` and `Calculator.prototype`?

Every function gets a a `prototype` property which points to the `constructor`'s function. Nearly everything is inherited, let me ask you this.

Why do arrays have methods such as `push` and `pop`?

```js
function Calculator() {};

Calculator.prototype.add = function(n1, n2){
  return n1 + n2;
}
Calculator.prototype.subtract = function(){};
Calculator.prototype.divide = function(){};
Calculator.prototype.power = function(){};

var ti83ReeaaaalLite = new Calculator();
```

You could even write it  using es6 conventions.

```js
class Calculator {
  constructor(){}
};

Calculator.prototype.add = function(n1, n2){
  return n1 + n2;
}
Calculator.prototype.subtract = function(){};
Calculator.prototype.divide = function(){};
Calculator.prototype.power = function(){};


var ti83ReeaaaalLite = new Calculator();
```

They all pretty much accomplish the same thing, which is great!

## practice

Complete the rest of the methods for the `Calculator` constructor.

## this

OK OK, I was trying to avoid `this`, it's important but not super important right now. But think of `this` as the object that you're currently looking at or holding on to.

For example

```js
class Calculator {
  constructor(){
    this.save = 0; // is something that can be altered throughout your functional calls
  }
};

Calculator.prototype.add = function(n1, n2){
  return n1 + n2;
}
Calculator.prototype.subtract = function(){};
Calculator.prototype.divide = function(){};
Calculator.prototype.power = function(){};

Calculator.prototype.changeSave = function(n){
  this.save = n;
}

var ti83ReeaaaalLite = new Calculator();
```

`this.save` is set to zero on `ti83ReeaaaalLite` when the `Calculator` is created. The context `ti83ReeaaaalLite` holds on to is the new instance which is itself, which is basically what was going on here at the example above.

```js
function Calculator() { // side note constructors are generally capitalized
  this.add = function(n1, n2){
    return n1 + n2;
  }

  this.subtract = function(){};
  this.divide = function(){};
  this.power = function(){};
}

var ti83ReeaaaalLite = new Calculator();
```
