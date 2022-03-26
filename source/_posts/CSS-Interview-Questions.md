---
title: CSS Interview Questions
date: 2022-01-28 11:39:06
tags: [CSS, Interview, frontend develper, web developer]
banner_img: https://tva3.sinaimg.cn/large/0060lm7Tly1ftg6omnqa4j31hc0u010z.jpg
index_img: https://tva3.sinaimg.cn/large/0060lm7Tly1ftg6omnqa4j31hc0u010z.jpg
categories: Interview Questions
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

### 4. Explain Box Sizing Property

Box Sizing property defines how the height and width of a box are calculated.

- Content Box - The default width and height apply only to the element’s content. Padding and border are added outside the box.-
- Padding Box - You add the dimensions to both element’s content and padding. It adds the border outside the box.
- Border Box - The dimensions are added to the content, padding, and border.

### 5. What are the different ways to hide an Element using CSS?

- display: none: Hides the content and doesn’t store it in the DOM

- visibility: hidden: It adds the element to the DOM and takes up space. However, it is not visible to the user

- position: absolute: You can make the element appear outside the screen

### 6. What does ‘Important’ in CSS mean?

The ‘important’ keyword indicates the highest precedence, and it overrides the cascaded property.

```
p {

                color:blue !important;

            }

            #thing {

                color: green;

            }


<p id="thing">Will be BLUE.</p>
```

### 7. What are CSS Sprites?

- Since each image sends out an HTTP request separately, a web page with a high number of photos takes longer to load.
- CSS sprites are used to minimize the loading time of a web page by combining multiple small pictures into a single image.
- It decreases the number of HTTP requests and, as a result, the time it takes for pages to load.

### 8. Which Property is used to Underline, Strikethrough, and Overline Text?

- text-style

- Text-type

- text-decoration

- Text-transform
