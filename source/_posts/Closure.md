---
title: Closure
date: 2021-06-05 18:30:29
tags: [Closure, JavaScript]
---

## What is a Closure?

1. Closures are a property of JavaScript functions, and only functions. No other data type has them.
2. To observe a closure, you must execute a function in a different scope than where that function was originally defined.

A **closure** is the combination of a function bundled together (enclosed) with references to its surrounding state (the **lexical environment**). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

To use a closure, define a function inside another function and expose it. To expose a function, return it or pass it to another function.

The inner function will have access to the variables in the outer function scope, even after the outer function has returned.

## Why should we know closures?

Let's answer the original question we set out to answer. Based off of what we've seen, pause and take a stab at answering this question. Why should we care about closures as JS developers?

Closures matter for you and your code because they allow you to 'remember' values, which is a very powerful and unique feature in the language which only functions possess.

We saw it right here in this example. After all, what use is a like count variable that doesn't remember likes? You'll encounter this often in your JS career. You need to hold onto some value somehow and likely keep it separate from other values. What do you use? A function. Why? To keep track of data over time with a closure.

And with that, you're already a step ahead other developers.

## Using Closures (Examples)

Among other things, closures are commonly used to give objects data privacy. Data privacy is an essential property that helps us program to an interface, not an implementation. This is an important concept that helps us build more robust software because implementation details are more likely to change in breaking ways than interface contracts.

In JavaScript, closures are the primary mechanism used to enable data privacy. When you use closures for data privacy, the enclosed variables are only in scope within the containing (outer) function. You can’t get at the data from an outside scope except through the object’s **privileged methods**. In JavaScript, any exposed method defined within the closure scope is privileged. 

# What problem can it solve?

1. Debounce and Throttle 



