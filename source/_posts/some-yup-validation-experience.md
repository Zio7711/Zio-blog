---
title: some yup validation experience
date: 2022-03-26 19:28:15
tags: [Yup, Form validation]
categories: Working fragment
index_img: https://images.unsplash.com/photo-1566837945700-30057527ade0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80
banner_img: https://images.unsplash.com/photo-1566837945700-30057527ade0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80
---

This week, I was asked to fix lots of legacy bugs in our projects that are related to the Frontend form validation. Our project uses Formik and Yup to do the validation. From the code, I found out the previous developer made some common mistakes and I would like to share with you here.



## Empty String Validation

With Yup and Formik, it is actually very easy to validate if the input is a empty string, but many developers tend to forget this step when they already validated **Required Field**. 

```js
const validationSchema = Yup.object().shape({
    newPassword: Yup.string().required()
})
```

For example, if the validation schema is like the code above, when a user enters an empty space for setting up the password, it will pass the validation, which is not what we want. In order to solve this, just add an another restriction **.trim()** :

```js
const validationSchema = Yup.object().shape({
    newPassword: Yup.string().trim().required()
})
```

There is another way of doing this by adding a custom test:

```js
const validationSchema = Yup.object().shape({
    newPassword: Yup.string().test(
        'empty-check',
         password => !password
    });
```



# Date Validation

