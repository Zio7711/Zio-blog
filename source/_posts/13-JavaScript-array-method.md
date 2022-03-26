---
title: 13 JavaScript array method
date: 2022-02-10 21:03:09
index_img: https://tva2.sinaimg.cn/large/87c01ec7gy1frmroo4iggj21hc0u0th9.jpg
banner_img: https://tva2.sinaimg.cn/large/87c01ec7gy1frmroo4iggj21hc0u0th9.jpg
tags: [array, JavaScript, method]
categories: JavaScript Fundamentals
---

Let’s talk about Array methods.

We work with data every day. The world itself is data. When we work with data in programming, we widely use the array to store and process the data.

> But… Are we using the right method at right place to process the array of data?

To be honest… I see a lot of developers still use the map and filter method to print the array element. A lot of them still don’t know the reduce, some, and every method. And some of them only use the forEach everywhere.

So here I have described the **13 most used array methods** in easy words.

# forEach

- The forEach() method **calls a callback function** once for each array element
- The callback function takes **3 arguments:**
  \- value
  \- index
  \- array itself

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210210804.png)

# map

- It is **used to map** the array data
- It **creates a new array** and does not change the original array
- The returned array has the **same length** as the input array

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210210835.png)

# filter

- Used to **filters the array** based on the given condition
- It also **creates a new array** and does not modify the original array.
- **Return an empty array** if array elements do not match with the given condition

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210210859.png)

# find

- Behaves the same as a filter, but it only **returns a single element**
- It also has the **condition**
- It stops at the first element that **“passes the condition”** and returns that
- Returns **undefined** if the condition does not match with any element

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211206.png)

# findIndex

- Similar to find() but **returns index** instead of element
- **Returns -1** If does not passes the test

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211237.png)

# reduce

- The reduce() method runs a function on each array element to **produce (reduce it to) a single value**
- For each iteration, the return value of the callback passed on as an **accumulator** argument of the next iteration
- Takes **initial value** as a second argument (Optional)

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211253.png)

# reduceRight

- Same as reduce, but reduceRight() works from **right-to-left** in the array

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211313.png)

# every

- Check if **all array values** pass a given condition
- Returns true or false

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211656.png)

# some

- Check if **some array values** pass a condition
- It returns true or false

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211704.png)

# indexOf

- **Returns the index** of an array element if passes the condition
- Returns **-1** otherwise

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211519.png)

# lastIndexOf

- Same as indexOf(), but returns the index of the **last occurrence** of the specified element

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211541.png)

# includes

- Used to check if an **element is present** in an array
- **Returns true or false** based on the presence of element in the array

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211603.png)

# Array.from

- Create an Array from a String

![](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220210211624.png)
