---
title: JavaScript practices
date: 2022-07-15 15:05:25
banner_img: https://tva1.sinaimg.cn/large/0060lm7Tly1ftg6xjnwe8j31hc0u0kjl.jpg
index_img: https://tva1.sinaimg.cn/large/0060lm7Tly1ftg6xjnwe8j31hc0u0kjl.jpg
tags: [JavaScript, interview, frontend]
categories: Interview Questions
---

*This article was written by  [Career Karma](https://careerkarma.com/).* I am just studying this material.

### What is the difference between a forEach loop and the .map() function?

Both [JavaScript forEach loops](https://careerkarma.com/blog/javascript-foreach-loop/) and map() functions iterate over items in a list.

The forEach loop executes a callback function for each element in a list. It does not return any values once it has been run. A map statement calls a function on each element in a list and returns a transformed array with the values returned by that function.

In short, forEach() loops do not return a new array but map() functions do.

### **1. What is a JavaScript Promise? What are the benefits of using a Promise over a callback?**

A [JavaScript Promise](https://careerkarma.com/blog/javascript-promise/) is a way to write more asynchronous code. A Promise is defined with two functions: a resolve and a reject function. If a Promise is executed successfully, the resolve function is returned to the main program; otherwise, the reject function is returned.

Promises allow you to avoid “callback hell.” This is where you define callback functions within callback functions. Callback hell results in unreadable code. Promises, unlike callbacks, support .then() statement. This means that the order in which a block of code runs can be made clearer if you use a Promise.

### **2. How can you check if an array is empty?**

To check if an array is empty, you use an “if” statement:

```
if (array_name === undefined || array_name.length === 0) {
	// Code to run
}
```

First, the “if” statement makes sure that an array has been defined. Without this check, our code would return an error if "array_name" could not be found.

Next, our code checks whether the length of “array_name” is equal to 0. If either of these conditions are true, our “if” statement will execute.

### **3. What are default parameters in a function?**

Default parameters let you specify default values for a parameter in a function. This means you call a function without defining a value and a default value will be set in its place.

A default parameter is written using this syntax:

```
function multiply_numbers(number_one = 0, number_two = 0) {
	return number_one * number_two;
}
```

Default parameters are specified as a parameter name, followed by an equals sign, followed by the default value you want to set.

This syntax means you don’t have to check if a value is defined before you start to use it in a function. Default parameters therefore make a function easier to read and understand.

### 4. What is the difference between synchronous and asynchronous functions?

Synchronous functions wait until each statement in a method has been run before moving on to the next. This means a synchronous function is read line-by-line and may depend on the value of a previous statement to work successfully.

Asynchronous functions, on the other hand, execute each line of code without stopping to wait for a value from a function. An asynchronous function usually depends on a Promise or a callback which executes while the main program is running. The Promise or callback will return a value back to the main program.

### **5. What are Arrow Functions?**

Arrow functions are an alternative way of defining a JavaScript function. Arrow functions allow you to define a function without using the function() keyword. This lets you write more concise and readable code.

An arrow function can be written on one line:

```
const multiply_values = (value1, value2) => console.log(value1 * value2);
```

Arrow functions accept arguments just like a regular function expression. You do not need to use a return statement with an arrow function. This is because arrow functions implicitly return a value if there is only one value to return.

### 6. How can you filter values out of an array of objects?

An efficient way to filter values out of an array of objects is to use the [JavaScript filter() function](https://careerkarma.com/blog/javascript-filter-reduce/). The filter function iterates through a list of items and creates a new list of items that meet a particular condition or set of conditions.

Consider this list of students:

```
var students = [ { name: “Sam”, grade: 6 }, { name: “Alix”, grade: 7 }];
```

To retrieve all the students in sixth grade, we use a filter function:

```
var sixth_grade = students.filter(student => (student.grade === 6));
```

Our code returns all the students who are in sixth grade:

```
{ name: “Sam”, grade: 6 }
```

### 7. What is functional programming?

JavaScript supports functional and [object-oriented programming](https://careerkarma.com/blog/object-oriented-javascript-interview-questions/). Functional programming is a programming paradigm where programs are written using pure functions.

Pure functions produce the same output. This makes them easier to read, debug, and interpret. One way to think about pure functions is like a calculator. If you evaluate 9 multiplied by 9 in a calculator, 81 will always be returned.

JavaScript offers features like first-class functions and higher-order functions to support the functional programming paradigm. Other functional programming languages include Lisp, Haskell, and Elm.