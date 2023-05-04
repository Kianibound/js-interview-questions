# JavaScript most important and frequently asked interview questions:

## Here is the list of questions:

[1-What is Javascript Exactly?](#q1)

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

[14-What is a Promis in JavaScript?](#q14)

[15-What are the main states of a Promise?](#q15)


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


## 14-What is a Promis in JavaScript? <a name="q14" />

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


