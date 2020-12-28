# First class functions
As per [wikipedia](https://en.wikipedia.org/wiki/First-class_function
) First class functions can be:
- stored in variable, object or array
- passed to functiona as an argument
- returned by the function

## Storing a function
Function can be stored in another variable ex:
```
const sayHello = name => {
    console.log(`Hello ${name}`);
}

const sayBye = name => {
    console.log(`Bye ${name}`);
}

const functionArray = [sayHello, sayBye];

functionArray.forEach(fn => fn('Functional Programming')
);
```

Above code gives following output on console:
```
Hello Functional Programming
Bye Functional Programming
```

## Passing function as parameter
Function can be passed to another function as parameter. If you have worked on C/C++/C#/Java then you must have have passed function as parameter like in threading in C#/Java.
This concept is known as _callback_ in computer programming.

Following is the simple example of callback in javascript. This code will print _hello world_ after 1 second.
```
setTimeout(console.log, 1000, 'hello world');
```

## Function returned by a function
Function returns another function when invoked.In below example we are creating a myMap method which takes function as input and return another function that takes array as input. Returned function will apply function(input of myMap) in array's map method:
```
const myMap = fn => {
    return aArray => aArry.map(fn);
};

const getX = item => item.x;
const inputArr = [{x:1}, {x:2, y:1}];
console.log('values=', myMap(getX)(inputArr))
```