---
title: helpful single line js code
date: 2022-12-17 00:11:29
tags:
---

## 1. generate random string

```js

const randomString = () => Math.random().toString(36).slice(2);

```

## 2. translate html special characters

```js
const escape = str => str.replace(/[&<>"']/g, tag => ({
  '&': '&amp;',
  '<': '&lt;',
  '>': '&gt;',
  '"': '&quot;',
  "'": "&#39;"
}[tag] || tag));

escape('<a href="#">Me & you</a>') // '&lt;a href=&quot;#&quot;&gt;Me &amp; you&lt;/a&gt;'
```

## 3. capitalize first letter

```js
const capitalize = (str) => str.replace(/\b[a-z]/g, char => char.toUpperCase());

capitalize('foo bar') // 'Foo Bar'
```

## 4. translate string to camel case

```js
const toCamelCase = (str) => str.trim().replace(/([-_][a-z])/ig, ($1) => $1.toUpperCase()
  .replace('-', '')
  .replace('_', ''));

toCamelCase('background-color') // 'backgroundColor'
toCamelCase('-webkit-scrollbar-thumb') // 'WebkitScrollbarThumb'
toCamelCase('_hello_world') // 'HelloWorld'
```

## 5. remove duplicates from array

```js
const removeDuplicates = (arr) => [...new Set(arr)];

console.log(removeDuplicates([1, 2, 2, 3, 4, 4, 5])); // [1, 2, 3, 4, 5]
```

## 6. flat array

```js
const flat = arr => arr.reduce((a, b) => a.concat(Array.isArray(b) ? flat(b) : b), []);

flat(['cat',['lion',['tom'], 'tiger', ['lion']]]) // ['cat', 'lion', 'tom', 'tiger', 'lion']
```

## 7. remove falsy values from array

```js
const removeFalsy = arr => arr.filter(Boolean);

removeFalsy([0, 1, false, 2, '', 3, 'a', 'e'*23, NaN, 's', 34]) // [ 1, 2, 3, 'a', 's', 34 ]
```

## 8. check if a number is even

```js
const isEven = num => num % 2 === 0;

isEven(3) // false
isEven(4) // true
```
