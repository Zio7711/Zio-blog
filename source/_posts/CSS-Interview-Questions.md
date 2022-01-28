---
title: CSS Interview Questions
date: 2022-01-28 11:39:06
tags: [CSS, Interview, frontend develper, web developer]
---

### 1. What is the best way to include CSS Styling in HTML?

- You use inline [CSS](https://www.simplilearn.com/11-css-secrets-rar400-article) when only a single element needs to be styled or when a little quantity of styling is required.
- External Style Sheet: When a style is applied to many elements or HTML pages, it employs an external style sheet.
- Internal Style Sheet: An internal style sheet is employed when a single HTML document has a distinct style and numerous elements



### 2. Mention the different types of CSS Selectors

- Universal Selector

  ```
  * {
  
          color: "green";
  
          font-size: 20px;
  
          line-height: 25px;
  
        } 
  ```

  

- Element type Selector

  ```
  ul {
  
      line-style: none;
  
      border: solid 1px #ccc;
  
    } 
  ```

  

- ID selector

  ```
  #container {
  
      width: 960px;
  
      margin: 0 auto;
  
    } 
  
    <div id="container"></div>
  ```

  

- Class selector

  ```
   .box {
  
      padding: 10px;
  
      margin: 10px;
  
      width: 240px;
  
    }  
  
    <div class="box"></div>
  ```

  

- Descendent Combinator

  ```
  #container .box {
  
      float: left;
  
      padding-bottom: 15px;
  
  }  
  
  <div id="container">
  
      <div class="box"></div>    
  
      <div class="box-2"></div>
  
  </div> 
  
  <div class=”box”></div>
  ```

  

- Child Combinator

  ```
   #container> .box {
  
      float: left;
  
      padding-bottom: 15px;
  
  }
  
  <div id="container">
  
      <div class="box"></div>   
  
      <div>
  
          <div class="box"></div>
  
      </div>
  
  </div> 
  ```

  

- General Sibling Combinator

  ```
  h2 ~ p {
  
      margin-bottom: 20px;
  
  }
  
  <h2>Title</h2>
  
  <p>Paragraph example.</p>
  
  <div class=”box”>
  
      <p>Paragraph example.</p>
  
  </div>
  ```

  

- Attribute Selector

  ```
  input [type=”text”] {
  
      background-color: #444;
  
      width: 200px;
  
  }
  
  <input type="text">
  ```

  

### 3. What are Sass, Less, and Stylus?

- Sass - Sass is the acronym for “Syntactically Awesome Style Sheets”. A ‘$’ sign commonly precedes it.

```
$font-color: #fff 

        $bg-color: #00f       
#box

          color: $font-color

          background: $bg-color
```



- Less - LESS is an acronym for “Leaner Stylesheets”. Less uses ‘@’ to define the variables.

```
@font-color: #fff;

          @bg-color: #00f          

          #box{

            color: @font-color;

            background: @bg-color;

          }
```



- Stylus - Stylus offers a great deal of flexibility in writing syntax. It doesn’t use @ or $ for defining variables. 

```
font-color= #fff;

        bg-color = #00f;    
#box {

          color: font-color;

          background: bg-color; }
```



