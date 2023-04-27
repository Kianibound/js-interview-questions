# JavaScript most important and frequently asked interview questions:

## Here is the list of questions:

[1-What is Javascript Exactly?](#q1)

[2-What is single thread meaning?](#q2)

[3-What are primitives in JavaScript?](#q3)

[4-What are non-primitives in JavaScript?](#q4)

[5-What '&&' operator does in JavaScript?](#q5)

[6-What '||' operator does in JavaScript?](#q6)

[7-What is difference between undefined and null in JavaScript?](#q7)


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


## 7-What is difference between undefined and null in JavaScript? <a name="q7"/>

In JavaScript, `null` and `undefined` are both values that represent the absence of a value. `undefined` is used when a variable has not been initialized or a function has no return value, while `null` is used when you want to explicitly indicate that a variable has no value.
