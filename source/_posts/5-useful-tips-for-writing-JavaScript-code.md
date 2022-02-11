---
title: 5 useful tips for writing JavaScript code
date: 2022-02-11 21:43:35
tags: [tips, writing code, JavaScript]
---

## Filtering 'null' value

使用 `filter()` 过滤 “空” 值，如 `null`、`undefined` 或空字符串，可以使用 `.filter(Boolean)` 的缩写方法；

它将所有空值转为 `false` 并从列表中删除它们，优雅！

```
const groceries = ['apple', null, 'milk', undefined, 'bread', ''];

const cleanList = groceries.filter(Boolean);

console.log(cleanList);

// 'apple', 'milk', 'bread';
复制代码
```

## Array Deconstruction

我们经常使用 ES6 的解构，对于一个数组，每项都是一个对象，如果想获得数组第一项的对象的某个值，可以这样写；

```
const people = [
  {
    name: "Lisa",
    age: 20,
  },
  {
    name: "Pete",
    age: 22,
  },
  {
    name: "Caroline",
    age: 60,
  }
];

const [{age}] = people;

console.log(age);

// 20
复制代码
```

也可以采用逗号占位的方式指定一个项进行赋值；

```
const people = [
  {
    name: "Lisa",
    age: 20,
  },
  {
    name: "Pete",
    age: 22,
  },
  {
    name: "Caroline",
    age: 60,
  }
];

const [, , caroline] = people;

console.log(caroline);

//  {
//     name: "Caroline",
//     age: 60,
//   }
复制代码
```

当然，也有常见的对象解构赋值；

```
const caroline = {
  firstNm: 'Caroline',
  ag: 27,
};

const {firstNm: firstName, ag: age } = caroline;

console.log(firstName, age);

// Caroline, 27
复制代码
```

## Split Number

对大数字使用分隔符号，将极大的提高可读性；这是 ES12 的新特性；

```
const bigNumber = 1_000_000;
console.log(bigNumber);
// 1000000
复制代码
```

## Arrow function returns an object directly

使用箭头函数返回一个对象，为了和函数的 `{` 区分开来，在外层包一层 `(` 即可解决；

```
const createPerson = (age, name, nationality) => ({
  age,
  name,
  nationality,
});

const caroline = createPerson(27, 'Caroline', 'US');

console.log(caroline);

// {
//   age: 27,
//   name: 'Caroline'
//   nationality: 'US',
// }
复制代码
```

## await chain

我们可以用 `filter` 和 `map` 方法接在 await 方法后形成链条过滤或映射处理获取的数据；

```
const chainDirectly = (await fetch('https://www.people.com'))
  .filter(person => age > 20)
  .filter(person => nationality === 'NL')
```