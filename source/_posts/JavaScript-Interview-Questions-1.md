---
title: JavaScript Interview Questions (1)
date: 2021-04-01 09:21:12
tags: [JavaScript, beginners, interview]
---

## 1. How to test data types?

1. type of: cannot distinguish array, object and null
2. instance of: test its prototype chain to get its datatype, it cannot detect basic data types
3. Object.protopeype.toString.call()
4. constructor

## 2. Undefined VS. Null in JavaScript.

1. **Definition:**

   - **Null:** It is the intentional absence of the value. It is one of the primitive values of JavaScript.
   - **Undefined:** It means the value does not exist in the compiler. It is the global object.

2. **Type:**

   **Null:** Object

   **Undefined:** undefined

## 3. What is the result of Typeof NaN ?

Number. `NaN` just means the specific value cannot be represented within the limitations of the numeric type (although that could be said for all numbers that have to be rounded to fit, but `NaN` is a special case).

A specific `NaN` is not considered equal to another `NaN` because they may be different values. However, `NaN` is still a number type, just like 2718 or 31415.

## 4. What Does the && Operator Do?

The `&&` operator is the _AND_ operator and it finds the first falsy expression and returns it. If there are no falsy expressions then it returns the last expression.

For example, if we have:

```
let foo = null && undefined && 'foo';
```

The `foo` is `null` since `null` and `undefined` are falsy.

If we have:

```
let foo = true && 'foo';
```

Then we have `'foo'` assigned to `foo`. It does short-circuit evaluation to prevent unnecessary checks.

It’s also a handy shortcut for:

```
if (condition){
  doSomething();
}
```

Because the code above is the same as:

```
condition && doSomething();
```

Because, if `condition` is falsy then `doSomething();` won’t run because of short-circuiting.

## 5. What’s the Difference Between `==` and `===`?

The difference between `==` and `===` is that `==` only checks the content for equality and `===` checks both the content and the data type for equality.

For example:

```
2 == '2'
```

This will return `true` since they both have `2` as their content. This is because `==` does type coercion.

The full list of rules for type coercion for the `==` operator is:

1. If `x` and `y` have the same value, compare with the `===` operator.
2. If `x` is `null` and `y` is `undefined`, return `true`.
3. If `x` is `undefined` and `y` is `null`, return `true`.
4. If `x` has the `number` type and `y` is a string, return `x == +y`.
5. If `x` has the `string` type and `y` is a `number`, return `+x == y`.
6. If `y` has the `boolean` type, return `+x == y`.
7. If `y` is a `boolean`, return `x == +y`.
8. If `x` is a `string`, `symbol`, or `number` and `y` is an `object` then:

- Return `x == y.valueOf()` if `y` is a `String` instance.
- Return `x == y.valueOf()` if `y` is a `Number` instance.
- Return `x == y[Symbol.toPrimitive]()` if `y` is any other kind of object or value.
