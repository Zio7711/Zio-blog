---
title: helpful single line js code
date: 2022-12-17 00:11:29
tags: [javascript, cheat sheet]
categories: [cheat sheet, fundamentals]
banner_img: https://tva3.sinaimg.cn/large/0060lm7Tly1ftg6xjnwe8j31hc0u0kjl.jpg
index_img: https://tva3.sinaimg.cn/large/0060lm7Tly1ftg6xjnwe8j31hc0u0kjl.jpg

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

## 9. get an integer between two numbers

```js
const randomIntFromInterval = (min, max) => Math.floor(Math.random() * (max - min + 1) + min);

randomIntFromInterval(2, 10) // 5
randomIntFromInterval(2, 10) // 8
```

## 10. get the average of the parameter 

```js
const average = (...nums) => nums.reduce((acc, val) => acc + val, 0) / nums.length;

average(...[1, 2, 3]) // 2
average(1, 2, 3) // 2
```

## 11. random color

```js
const randomColor = () => `#${Math.random().toString(16).slice(2, 8).padEnd(6, '0')}`;

randomColor() // '#e34155'
```

## 12. translate rgb to hex

```js
const rgbToHex = (r, g, b) => '#' + [r, g, b].map(x => {
  const hex = x.toString(16)
  return hex.length === 1 ? '0' + hex : hex
}).join('');

rgbToHex(0, 51, 255) // '#0033ff'
```

## 13. translate hex to rgb

```js
const hexToRgb = hex => hex.replace(/^#?([a-f\d])([a-f\d])([a-f\d])$/i
  ,(m, r, g, b) => '#' + r + r + g + g + b + b)
  .substring(1).match(/.{2}/g)
  .map(x => parseInt(x, 16));

hexToRgb('#0033ff') // [0, 51, 255]
```

## 14. clear all cookies

```js
const clearCookies = () => document.cookie.split(";").forEach(c => document.cookie = c.replace(/^ +/, "").replace(/=.*/, "=;expires=" + new Date().toUTCString() + ";path=/"));
```

## 15. check if it's in dark mode
    
```js
const isDarkMode = () => window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;

isDarkMode()
```

## 16. pause for a specified time

```js
const sleep = (ms) => new Promise(resolve => setTimeout(resolve, ms));

sleep(2000).then(() => {
  // do something after the sleep
})
```