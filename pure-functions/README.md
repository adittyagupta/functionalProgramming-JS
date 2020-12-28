# Pure Functions
As per [wikipedia](https://en.wikipedia.org/wiki/Pure_function
) a function is said to be pure when:
- Its return value is the same for the same arguments.
- Its evaluation has no side effects.

Below are some examples of pure functions:
```
const checkNullOrUndefined = val => {
  return val === null || val === undefined;
};

let a;
// output: true
console.log(checkNullOrUndefined(a));

a = 10;
// output: false
console.log(checkNullOrUndefined(a));

a = null;
// output: true
console.log(checkNullOrUndefined(a));
-----------------------------------------
const fruits = ['Apple', 'Orange', 'Banana', 'Mango'];

// output: 1=  ["Apple", "Orange", "Banana"], fruits=  ["Apple", "Orange", "Banana", "Mango"]
console.log('1= ', fruits.slice(0,3), ', fruits= ', fruits);

// output: 2=  ["Apple", "Orange", "Banana"], fruits=  ["Apple", "Orange", "Banana", "Mango"]
console.log('2= ', fruits.slice(0,3), ', fruits= ', fruits);

// output: 3=  ["Apple", "Orange", "Banana"], fruits=  ["Apple", "Orange", "Banana", "Mango"]
console.log('3= ', fruits.slice(0,3), ', fruits= ', fruits);
```

## What is side effects?
A function is said to have a side effect if it **modifies some state variable value(s) outside its local environment**, that is to say has an observable effect besides returning a value (the main effect) to the invoker of the operation.
Like:
- Changing the DOM is side effect.
- Changing the file system is side effect.
- Inserting a record is side effect.

_Side effects cannot be avoided but with functional programming wants us to keep sepration between pure and impure functions. This helps in maintaining and managing porgram easily._
