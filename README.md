

# JavaScript most important and frequently asked interview questions:

## Here is the list of questions:

[1-What is Javascript Exactly?](#q1)
<a name="top1" />

[2-What is single thread meaning?](#q2)

[3-What are primitives in JavaScript?](#q3)

[4-What are non-primitives in JavaScript?](#q4)

[5-What '&&' operator does in JavaScript?](#q5)

[6-What '||' operator does in JavaScript?](#q6)

[7-What is difference between undefined and null in JavaScript?](#q7)

[8-What is difference between == and === in JavaScript?](#q8)

[9-reduce vs map vs find vs filter methods in JavaScript?](#q9)

[10-What are falsy values in JavaScript?](#q10)

[11-What are the ways of creating an object in JavaScript?](#q11)

[12-What is a closure in JavaScript?](#q12)

[13-Name Scopes in JavaScript? Can you explain them?](#q13)

[14-What is a Promise in JavaScript?](#q14)

[15-What are the main states of a Promise?](#q15)

[16-What is Promise chaining in JavaScript?](#q16)

[17-`Promise.all()` vs `Promise.race()`](#q17)

[18-What is a pure function in JavaScript?](#q18)

[19-What is a HOF (Higher-Order Function) in JavaScript?](#q19)

[20-What are benefits and use cases of HOF (Higher-Order Function) in JavaScript?](#q20)

[21-What is memoization in JavaScript?](#q21)

[22-What is Hoisting in JavaScript?](#q22)

[23-Explain `var` , `let` and `const` hoisting in JavaScript?](#q22)


## 1-What is Javascript Exactly? <a name="q1"/>
JavaScript is a High-level single thread dynamic language for creating dynamic and interactive web content. It is one of the core technologies of the World Wide Web, along with HTML and CSS.


## 2-What is single thread meaning?<a name="q2"/>
JavaScript, when running in a web browser, is a single-threaded language, meaning that it can only execute one task at a time. This is because the browser's JavaScript engine uses a single call stack and event loop to manage the execution of code.


## 3-what are primitives in JavaScript? <a name="q3"/>
In JavaScript, primitives are simple values that are not objects. There are six primitive data types in JavaScript:

* Boolean: Represents a logical value of true or false.

* Null: Represents an intentional absence of any object value.

* Undefined: Represents a value that is not yet defined or has no value.

* Number: Represents both integer and floating-point numbers.

* String: Represents a sequence of characters, enclosed in single or double quotes.

* Symbol: Represents a unique identifier that is not equal to any other value.


## 4-What are non-primitives in JavaScript? <a name="q4"/>

 non-primitives are complex values that are made up of multiple values, and are usually objects or functions
 
 Non-primitive data types in JavaScript include:

* Object: An object is a collection of key-value pairs, where the keys are strings and the values can be any type of value, including other objects or functions. Objects can also have methods, which are functions that are associated with the object.

* Function: A function is a block of code that can be invoked with arguments, and can also return a value. Functions are also objects, which means they can have properties and methods.

* Array: An array is a collection of values, stored in a single variable. Arrays are also objects, and they have built-in methods for manipulating their contents.

* Date: The Date object represents a specific point in time, and provides methods for working with dates and times.

* RegExp: The RegExp object represents a regular expression, which is a pattern that can be used to match text in strings.

* Map: A Map is a collection of key-value pairs, similar to an object, but with some important differences. Maps can have any type of value as a key, and they maintain the order of their keys.

* Set: A Set is a collection of unique values, similar to an array, but with no duplicates.

* Promise: A Promise is an object that represents the eventual completion (or failure) of an asynchronous operation, and provides a way to handle its result.

* Error: The Error object represents an error that occurred during the execution of JavaScript code.


## 5-What `&&` operator does in JavaScript? <a name="q5"/>

The `&&` operator represents the logical AND operation. It returns true if both operands are truthy, and false if either operand is falsy. In simple looking for the first truthy value. For example:

```javascript
const a = true;
const b = false;

console.log(a && b); // false
console.log(a && true); // true
console.log(false && b); // false

true && true && true; // true
true && true && false; // false
null && false && undefined; // null

"Hans" && "Alex" && "Ali"; // "Ali"
true && true && "Ali"; // "Ali"
```

In the first example, `a && b` returns false because b is falsy. In the second example, a && true returns true because both operands are truthy. In the third example, `false && b` returns false because the first operand is falsy.


## 6-What `||` operator does in JavaScript? <a name="q6"/>

The `||` operator represents the logical OR operation. It returns true if either operand is truthy, and false if both operands are falsy. In simple looking for the first truthy value. For example:

```javascript
const a = true;
const b = false;

console.log(a || b); // true
console.log(a || true); // true
console.log(false || b); // false

console.log(null || "Oh you again!" || undefined); // Oh you again!
console.log(false || false || "Yaaay!"); // Yaaay!

```

In the first example, `a || b` returns true because a is `truthy`. In the second example, `a || true` returns true because the first operand is truthy. In the third example, `false || b` returns `false` because both operands are `falsy`.


## 7-What is difference between `undefined` and `null` in JavaScript? <a name="q7"/>

In JavaScript, `null` and `undefined` are both values that represent the absence of a value. `undefined` is used when a variable has not been initialized or a function has no return value, while `null` is used when you want to explicitly indicate that a variable has no value.



## 8-What is difference between `==` and `===` in JavaScript? <a name="q8"/>
In JavaScript, == and === are both comparison operators that are used to compare values.

The == operator is the equality operator, and it compares two values for equality after converting their types. If the values are of different types, JavaScript will attempt to convert one or both of the values to a common type. For example:

```javascript
console.log(1 == '1'); // true
console.log(null == undefined); // true
console.log(0 == false); // true

```

The === operator is the strict equality operator, and it compares two values for equality without type conversion. If the types of the values being compared are different, the result is always false. For example:

```javascript
console.log(1 === '1'); // false
console.log(null === undefined); // false
console.log(0 === false); // false

```



## 9-reduce vs map vs find vs filter methods in JavaScript? <a name="q9"/>
In JavaScript, reduce, map, find, and filter are all methods that operate on arrays and can be used to manipulate and transform data.

* reduce: The reduce method is used to reduce an array of values down to a single value. It takes a callback function as its argument, which is applied to each element of the array to accumulate a single value. For example:

```javascript
const arr = [1, 2, 3, 4];
const sum = arr.reduce((acc, val) => acc + val, 0); // 10
```
In this example, the reduce method is used to calculate the sum of all the values in the arr array.

* map: The map method is used to create a new array with the same length as the original array, but with each element transformed according to a callback function. For example:
```javascript
const arr = [1, 2, 3, 4];
const doubled = arr.map(val => val * 2); // [2, 4, 6, 8]

```
In this example, the map method is used to create a new array doubled with each element of the original array arr multiplied by 2.

* find: The find method is used to find the first element in an array that satisfies a given condition. It takes a callback function as its argument, which is applied to each element of the array until a matching element is found. For example:
```javascript
const arr = [1, 2, 3, 4];
const firstEven = arr.find(val => val % 2 === 0); // 2

```
In this example, the find method is used to find the first even number in the arr array.

* filter: The filter method is used to create a new array containing all the elements of the original array that satisfy a given condition. It takes a callback function as its argument, which is applied to each element of the array to determine whether to include it in the new array. For example:

```javascript
const arr = [1, 2, 3, 4];
const evenNumbers = arr.filter(val => val % 2 === 0); // [2, 4]

```
In this example, the filter method is used to create a new array evenNumbers containing all the even numbers in the arr array.


## 10-What are falsy values in JavaScript? <a name="q10"/>

In JavaScript, a value is considered "falsy" if it's treated as false when evaluated in a Boolean context. The following values are considered falsy in JavaScript:

* false: The boolean value false.
* null: A special value that represents "no value" or "absence of a value".
* undefined: A value that has not been defined.
* 0: The number zero (0).
* -0: Negative zero (-0).
* NaN: A special value that represents "Not-A-Number".
* '': An empty string.
* "": Another empty string.
* ``: An empty template string.
* document.all: A legacy property that used to return a collection of all HTML elements in a document.

In a Boolean context, these values are all considered equivalent to false. Any other value that's not on this list is considered "truthy" and will evaluate to true in a Boolean context.


## 11-What are the ways of creating an object in JavaScript? <a name="q11"/>

* Object Literal: The easiest and most common way to create an object is by using object literals. Object literals are a list of key-value pairs, enclosed in curly braces.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

```

* Constructor Function: Constructor functions are used to create objects with a set of properties and methods. To create an object with a constructor function, use the new keyword followed by the name of the function.

```javascript
function Person(name, age, city) {
  this.name = name;
  this.age = age;
  this.city = city;
}

let person = new Person("John", 30, "New York");

```

* Object.create(): The Object.create() method is used to create a new object with a specified prototype object and properties.

```javascript
let person = {
  name: "John",
  age: 30,
  city: "New York"
};

let person2 = Object.create(person);
person2.name = "Jane";
person2.age = 25;


```

* ES6 Classes: ES6 classes provide a new way to create objects with methods and properties. To create an object using a class, use the new keyword followed by the name of the class.

```javascript
class Person {
  constructor(name, age, city) {
    this.name = name;
    this.age = age;
    this.city = city;
  }
}

let person = new Person("John", 30, "New York");

```

* Factory Function: A factory function is a function that returns an object. This method is useful when you need to create multiple objects with the same properties and methods.

```javascript
function createPerson(name, age, city) {
  return {
    name: name,
    age: age,
    city: city,
    sayHi: function() {
      console.log(`Hi, my name is ${this.name}`);
    }
  };
}

let person = createPerson("John", 30, "New York");

```


## 12-What is a closure in JavaScript? <a name="q12"/>

A closure is created whenever a function is defined inside another function, and the inner function references variables or parameters from the outer function. The inner function retains a reference to the outer function's scope chain, which allows it to access these variables and parameters.

Here is an example of a closure in JavaScript:

```javascript
function outerFunction() {
  let outerVariable = "Hello";

  function innerFunction() {
    console.log(outerVariable);
  }

  return innerFunction;
}

let closure = outerFunction();
closure(); // Output: "Hello"

```

In this example, `outerFunction` returns `innerFunction`, which is defined inside it. `innerFunction` references `outerVariable`, which is defined in the outer function's scope. When `outerFunction` is called and `innerFunction` is returned, a closure is created that allows `innerFunction` to access `outerVariable`, even though `outerFunction` has already returned.

Closures are commonly used in JavaScript to create `private variables` and `functions`, as well as to create `callbacks` and `event handlers`.


## 13-Name Scopes in JavaScript? Can you explain them? <a name="q13" />

* `Global Scope:` A variable declared outside of any `function` or `block` has `global scope`, which means it can be accessed from `anywhere` in the code.
Example: 
```javascript
let globalVariable = "Hello";

function sayHello() {
  console.log(globalVariable);
}

sayHello(); // Output: "Hello"

```

* `Local Scope:` A variable declared inside a `function` or `block` has local scope, which means it `can only be accessed from within that function or block`.
 Example:
 
 ```javascript
function sayHello() {
  let localVariable = "Hi";
  console.log(localVariable);
}

sayHello(); // Output: "Hi"
console.log(localVariable); // Throws an error: "Uncaught ReferenceError: localVariable is not defined"

```

* `Block scope:` refers to the scope of a variable declared using the `let` or `const` keywords within a block, such as within a `loop` or an `if statement`. The variable is only accessible within that block and any nested blocks.

Example:

```javascript
if (true) {
  let blockVariable = "Hello";
  console.log(blockVariable); // Output: "Hello"
}

console.log(blockVariable); // Throws an error: "Uncaught ReferenceError: blockVariable is not defined"

```

* `Function scope:` refers to the scope of a variable declared using the `var` keyword within a function. The variable is only accessible within that function and any nested functions.

Example:

```javascript
function sayHello() {
  var functionVariable = "Hi";
  console.log(functionVariable); // Output: "Hi"
}

sayHello();
console.log(functionVariable); // Throws an error: "Uncaught ReferenceError: functionVariable is not defined"

```


## 14-What is a Promise in JavaScript? <a name="q14" />

In JavaScript, a Promise is an object that represents the eventual completion (or failure) of an `asynchronous operation`, and allows us to handle the result of that operation in a more flexible way.

Promises are commonly used in JavaScript for `asynchronous operation`s such as `network requests`, `file I/O`, and `animations`. They provide a way to write more `readable` and m`aintainable` asynchronous code by separating the logic for handling the result of an operation from the logic for initiating the operation itself.

Here is an example of using a Promise to fetch data from a server:

```javascript
fetch("https://jsonplaceholder.typicode.com/todos/1")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));

```

## 15-What are the main states of a Promise? <a name="q15" />

* `Pending`: The initial state, before the Promise has resolved or rejected.

* `Fulfilled`: The Promise has resolved, meaning the asynchronous operation completed successfully, and the result is available.

* `Rejected`: The Promise has rejected, meaning the asynchronous operation encountered an error, and the reason for the error is available.



## 16-What is Promise chaining in JavaScript? <a name="q16" />

Promise chaining in JavaScript refers to the practice of chaining multiple asynchronous operations together using Promises, in order to perform a series of tasks that depend on each other.

When we have multiple asynchronous operations that need to be executed in a specific order, we can use Promise chaining to `ensure that each operation is completed before moving on to the next one`.

Example:

```javascript
fetch("https://jsonplaceholder.typicode.com/todos/1")
  .then(response => response.json())
  .then(data => {
    console.log(data);
    return fetch("https://jsonplaceholder.typicode.com/users/" + data.userId);
  })
  .then(response => response.json())
  .then(user => console.log(user))
  .catch(error => console.error(error));

```

In this example, we first fetch data from the server using the `fetch()` function, and then `parse` the resulting response using the first `.then()` method.

Then, we log the data to the `console` and use it to construct a `new URL` for a `second fetch` request. We use the return keyword to pass the `second Promise` to the next `.then()` method, which will be called with the result of the second request.

Finally, we log the result of the second request to the console, and use the `.catch()` method to handle any `errors` that may occur during the operation.



## 17-`Promise.all()` vs `Promise.race()` in JavaScript? <a name="q17" />

`Promise.all()` waits for `all Promises` to complete, while `Promise.race()` waits only for the `first Promise` to complete.

* `Promise.all()` takes an array of Promises as its argument, and returns a new Promise that resolves when all the Promises in the array have resolved.

Example:

```javascript
Promise.all([
  fetch('https://jsonplaceholder.typicode.com/todos/1').then(response => response.json()),
  fetch('https://jsonplaceholder.typicode.com/users/1').then(response => response.json())
])
.then(results => console.log(results))
.catch(error => console.error(error));

```

In this example, we pass an array of two Promises to Promise.all(), which will resolve when both Promises have resolved. The resulting array will contain the resolved values of both Promises.

* `Promise.race()` takes an array of Promises as its argument, and returns a new Promise that resolves or rejects as soon as one of the Promises in the array resolves or rejects.

Example:

```javascript
Promise.race([
  fetch('https://jsonplaceholder.typicode.com/todos/1').then(response => response.json()),
  fetch('https://jsonplaceholder.typicode.com/users/1').then(response => response.json())
])
.then(result => console.log(result))
.catch(error => console.error(error));

```

In this example, we pass an array of two Promises to Promise.race(), which will resolve or reject as soon as the first Promise in the array resolves or rejects. The resulting value or reason of the Promise.race() Promise will be the same as that of the first Promise to complete.



## 18-What are pure functions in JavaScript? <a name="q18" />


pure function is a function that always returns the same output for the same input and does not cause any side effects.

Here's a simple example:


```javascript

function add(a, b) {
  return a + b;
}

```

This add function is a pure function because it takes two arguments a and b and always returns their sum without modifying any variables outside its scope.

Pure functions are beneficial in several ways:

* They are easier to reason about because they don't depend on any external state.
* They can be easily tested because they have a fixed output for a given input.
* They can be used in memoization to improve performance by caching the result of the function for a given input.
* Note that a function can still be pure even if it uses variables outside its scope, as long as it doesn't modify them. For example:

```javascript

const taxRate = 0.1;

function calculateTotal(amount) {
  return amount + (amount * taxRate);
}


```

This calculateTotal function uses the taxRate variable from outside its scope, but it doesn't modify it, so it is still considered a pure function.



## 19-What is a HOF (Higher-Order Function) in JavaScript? <a name="q19" />

In JavaScript, a Higher-Order Function (HOF) is a function that takes one or more functions as arguments or returns a `function` as its result.

To put it simply, an HOF is like a function that deals with other functions.

Here's a simple example:

```javascript

function applyOperation(number1, number1, operation) {
  return operation(number1, number2);
}


```


This `applyOperation` function is an `HOF` that takes two numbers (number1 and number2) and a function (operation) as `arguments`, and applies the function to the numbers.

You can use the `applyOperation` function like this:


```javascript

function add(a, b) {
  return a + b;
}

function multiply(a, b) {
  return a * b;
}

console.log(applyOperation(2, 3, add)); // Output: 5
console.log(applyOperation(2, 3, multiply)); // Output: 6


```

Here, we define two functions (`add` and `multiply`) that take two arguments and return the sum and product of those arguments, respectively. Then, we use the `applyOperation` function to apply each of these functions to the numbers 2 and 3.





## 20-What are benefits and use cases of HOF (Higher-Order Function) in JavaScript? <a name="q20" />

Here are some use cases and benefits of Higher-Order Functions (HOFs) in JavaScript:

### Use cases:

* Creating `generic functions` that work with different functions based on the context.
* Implementing function `composition`, where multiple functions are combined to form a new function.
* Implementing `callback functions` that are executed when certain `events` occur or conditions are met.
* Implementing function `currying`, where a function with multiple arguments is transformed into a `series of functions` that each take a single argument.
* Implementing `memoization`, where the results of a function are `cached` to improve `performance`.

### Benefits:

* Improved code `reusability` and `maintainability`, as common functionality can be `encapsulated` in HOFs and reused across different parts of an application.
* Improved `flexibility` and `extensibility`, as HOFs can be used to customize or extend the behavior of existing functions without modifying their original code.
* Improved code readability and abstraction, as HOFs can provide a higher-level view of the problem being solved and abstract away low-level details.
* Improved code `testability`, as HOFs can be easily tested in `isolation` without needing to test the entire application.
* Improved `performance` in certain cases, as HOFs can enable `optimizations` like `memoization` and `lazy evaluation`.


## 21-What is memoization in JavaScript? <a name="q21" />

Memoization is a technique used to speed up the execution of a function by caching its results. When a function is called with the same arguments multiple times, instead of recalculating the result, the cached result is returned.

Here's a simple example in JavaScript:

```javascript

function multiplyByTwo(n) {
  console.log('Function called with argument', n);
  return n * 2;
}

const memoizedMultiplyByTwo = memoize(multiplyByTwo);

console.log(memoizedMultiplyByTwo(5)); // Output: 10 (Function called with argument 5)
console.log(memoizedMultiplyByTwo(5)); // Output: 10 (No function call, result returned from cache)


```

 this example, we define a function` multiplyByTwo` that simply multiplies its argument n by two and logs a message to the console. We then create a `memoized` version of this function using memoize, and call it twice with the argument 5. The first time, the function is called and the message is logged to the console. The second time, the `cached` result is returned and no function call is made, resulting in a faster execution.

Note that the memoize function used in this example is a simplified version that assumes the function takes only one argument and that the argument is a primitive value (such as a number or a string). In practice, a more robust implementation would be needed to handle functions with multiple arguments and non-primitive types.

another example:

```javascript

function memoize(func) {
  const cache = {};
  return function(...args) {
    const key = JSON.stringify(args);
    if (cache[key]) {
      return cache[key];
    } else {
      const result = func.apply(this, args);
      cache[key] = result;
      return result;
    }
  };
}

function fibonacci(n) {
  if (n < 2) {
    return n;
  } else {
    return fibonacci(n - 1) + fibonacci(n - 2);
  }
}

const memoizedFibonacci = memoize(fibonacci);

console.log(memoizedFibonacci(10)); // Output: 55
console.log(memoizedFibonacci(10)); // Output: 55 (Returned from cache)


```

In this example, we define a memoize function that takes a function func as its argument and returns a new function that caches the results of func. The cached results are stored in an object cache, using a stringified version of the arguments as the key.

We then define a fibonacci function that calculates the nth number in the Fibonacci sequence. We create a new memoized version of this function using memoize, and call it with the argument 10 twice. The first time, it calculates the result using the recursive Fibonacci algorithm, but the second time it returns the result from the cache, which saves time and resource.


## 22-What is Hoisting in JavaScript? <a name="q22" />

Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their respective scopes during the compilation phase, before any code is executed. This means that a variable or function can be used before it has been declared in the code. However, the behavior of hoisting differs based on the type of variable or function declaration.

## 23-Explain `var` , `let` and `const` hoisting in JavaScript? <a name="q23" /> 

* Hoisting with var:
When a variable is declared using the `var` keyword, its declaration is `hoisted` to the top of its scope, but its initialization remains in place. This means that the variable can be used before it is assigned a value, but its value will be `undefined`. Here's an example:

```javascript

console.log(myVar); // undefined
var myVar = 10;

```

* Hoisting with `let` and `const`:
When a variable is declared using the `let` or `const` keyword, its declaration is also hoisted to the top of its scope, but unlike `var`, it is not initialized. This means that the variable cannot be used before it is assigned a value. Here's an example:

```javascript

console.log(num); // ReferenceError: num is not defined
console.log(name); // ReferenceError: name is not defined

let num = 10;
const name = "Sarah";


```

[Back to top](#top1)

