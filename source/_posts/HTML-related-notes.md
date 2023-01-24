---
title: HTML related notes
date: 2022-07-18 14:55:36
banner_img: https://tva4.sinaimg.cn/large/87c01ec7gy1frmr2kh3xkj21kw0w0e8e.jpg
index_img: https://tva4.sinaimg.cn/large/87c01ec7gy1frmr2kh3xkj21kw0w0e8e.jpg
tags: [HTML, interview, frontend]
categories: Interview Questions
---

*This article was written by  [Career Karma](https://careerkarma.com/).* I am just studying this material.

### 1. What is Semantic HTML and why do we use it?

Semantic HTML codes meaning to web pages, making it not only useful for search engine optimization and other developers reading your code, but also to screen readers.

If you are being interviewed to help a product at a company, you want that product to produce value for every user, including those who visit the company’s site using screen readers. A screen reader is a tool used to render text,Accessible Rich Internet Applications (ARIA) roles, states, and properties, and “alt” attributes into speech.

An example of semantic HTML is using a \<p> tag instead of a \<div> to write a paragraph, or an \<h1> tag to highlight the most important heading on the webpage.

Semantic HTML is also used for native browser functionality. One reason we use the \<button> tag instead of a \<div> with a role=“button” is because \<button> already conveys the meaning that the piece of code being built is a button.

### 2. What is `<head>` a container for?

The <head> element is a container for other elements’ metadata. Metadata refers to data that will not be displayed on the webpage, but is needed for any professional product. It lives in between the <html> and <body> tags and can contain the following elements:

| ELEMENTS   | DESCRIPTION                                                  |
| :--------- | :----------------------------------------------------------- |
| `<title>`  | Required in HTML documents. The title is what is displayed not on the web page, but on the page’s tab. It must be text only. |
| `<style>`  | Used to style within a single HTML page.                     |
| `<meta>`   | Used to specify keywords for search engines, defining descriptions, name, and character set. |
| `<link>`   | Used to link external documents like Cascading Style Sheets (CSS). |
| `<script>` | Used to define JavaScript.                                   |
| `<base>`   | Used with a href attribute to specify a base URL.            |

Below is a code sample of the `<head>` element containing all of the elements above.

```
​```
<head>

  <title>My Ebook</title>
  
  <style>
  
  	body {background-color: black;}
    
  	h1 {color: green;}
    
  	p {color: white;}
    
  </style>
  
  <meta charset="UTF-8">
  
  <meta name="your name" content="biography"> 
  
  <link rel="stylesheet" href="main.css">
  
  <script>
  
    function myFunction() {
    
    document.getElementByTagName(h1).innerHTML = "My Biography";
    
    }
    
 </script>
 
<base href="https://www.landingpage.com/" target="_blank">

</head>

​``` 
```

### 3. How would you use HTML for audio/video placement?

The HTML5 DOM, an Object Model for HTML5 which has methods, properties, and events, works with the <audio> and <video> elements. Using HTML this way allows you to use methods like play() and pause(), as well as properties like duration, muted, and events like seeking and volumechange.

There are usually other ways to implement audio and videos by implementing JavaScript, however, diving into the HTML5 DOM and playing with this technique will give you more knowledge and skills as to how you can use the language in a different way.

### 4. What are global attributes?

Global attributes are [HTML attributes](https://careerkarma.com/blog/html-attributes/) that can be used with all elements. Below you will find a chart description of some of the most commonly used global attributes.

| GLOBAL ATTRIBUTE | DESCRIPTION                                                  |
| :--------------- | :----------------------------------------------------------- |
| class            | Used to specify a class name for styling.                    |
| title            | Used to specify additional information about an element.     |
| id               | Used to specify a unique ID for an element for styling purposes or links within a single web page. |
| style            | Used for inline styling.                                     |

### **5. How can you use HTML to declare the language of the web page? Why is this important?**

The lang attribute is used to declare the language of the web page. It should be included inside the <html> tag.

Declaring the language of a webpage is important because it lets search engines and browsers know the language in which a webpage appears. Yes, a user will not directly see this attribute. But because it has an impact on how a browser reads the page, you should specify a language.

```
<html lang="en">

</html>
```

### 6. How do you embed an image onto a web page?

An image can be embedded onto a webpage by using the HTML <img> element. This element must be used with the attribute “src” to specify the image path (image location in your code base), or image url. The “alt” attribute is also required for screen readers and in the case where the actual image cannot load or be displayed on the page.

```
<img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1504&q=80" alt="laptop--on-desk-with-other-electronics">
```

### 7. How would you go about finding if the element and attribute you are using will be supported with the browser for our audience?

This type of question offers a good opportunity for a follow up question. Usually the engineering manager or tech lead will have data on the most popular browser being used by their users, so a follow up question can be “what are the top browsers your audience usually uses?”

A way to confirm that your element or attribute will be supported by whatever browsers are used is to refer to an HTML reference for browser support. This will give you an idea of how to set up your HTML in a way that will be compatible for the audience you are helping build a product for.

