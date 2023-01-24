---
title: Interesting Question 1
date: 2022-07-19 14:29:39
banner_img: https://tva3.sinaimg.cn/large/0060lm7Tly1ftg6xehevfj31hc0u0b29.jpg
index_img: https://tva3.sinaimg.cn/large/0060lm7Tly1ftg6xehevfj31hc0u0b29.jpg
tags: [interview, frontend]
categories: Interview Questions
---

## Interesting Question 1: 

> Classic JS question 

```javascript 
//what should the question mark ? be so that it will console.log true?

const a = ?; 

console.log(a == 1 && a == 2 && a == 3); 

```

> Answer 

```javascript 

const a = { n: 1, valueOf: function() { return this.n ++; } } 

console.log(a == 1 && a == 2 && a == 3); // the output is true 

``` 

The **==** operator: if data type is different, it will invoke valueOf method, if the value cannot be converted, it will invoke toString method.