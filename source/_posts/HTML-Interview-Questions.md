---
title: HTML Interview Questions
date: 2022-01-28 00:02:12
tags: [HTML, interview, frontend]
banner_img: https://tva1.sinaimg.cn/large/87c01ec7gy1frmrtnq32hj21hc0u0wnl.jpg
index_img: https://tva1.sinaimg.cn/large/87c01ec7gy1frmrtnq32hj21hc0u0wnl.jpg
categories: Interview Questions
---

### 1. What Is an Attribute in HTML?

- Attributes are the properties that can be added to an HTML tag that change the way the tag behaves or is displayed.
- It adds attributes right after the name of the HTML tag, inside the brackets.

### 2. What is Marquee in HTML?

- The marquee is used to scroll the text on the webpage.
- It automatically scrolls the image or text up, down, left, or right.
- You must use \<marquee> tags to apply for a marquee.
- This tag has been deprecated

### 3. What is Semantic HTML? and how does it work?

- Semantic HTML is a type of coding.
- It is the use of HTML markup to emphasize the content's semantics or meaning.
- Consider the following scenario: The <b></b> tag is not used for bold statements in semantic HTML, while the <i></i> element is used for italic.
- Instead, you use the <em></em> and <strong></strong> tags.

### 4. How do you Display a Table on an HTML Webpage?

![HTMLTable](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220128001209.png)

### 5. What is SVG in HTML?

- HTML SVG is a markup language that describes **vector and raster graphics**. XML text files define SVG pictures and associated behaviors.
- It's typically used for X, Y coordinate system diagrams like pie charts and 2-Dimensional graphs.

### 6. In HTML, how do you separate a section of text?

```
<br> <p> <blockquote>
```

### 7. How do you Create Nested Web Pages in HTML?

```
<!DOCTYPE html>

    <html>

      <body>

        <h2>HTML Iframes example</h2>

        <p>

          specify the size of the iframe using the height and width attributes:

        </p>

        <iframe src="https://simplilearn.com/" height="600" width="800"></iframe>

      </body>

    </html>
```

- You refer a webpage within a webpage to as a nested web page.
- Using HTML's built-in iframe tag, you can create nested web pages.

### 8. Differentiate Between Ordered List and Unordered List

```
<!DOCTYPE html>

    <html>

      <body>

        <h2>HTML List Example</h2>

        <ul>

          <li>Coffee</li>

          <li>Tea</li>

          <li>Milk</li>

        </ul>

        <ol>

          <li>Coffee</li>

          <li>Tea</li>

          <li>Milk</li>

        </ol>

      </body>

    </html>
```

![List Example](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220128003239.png)


### 9. What does a doctype do?
- It stands for Document Type Declaration.
- It informs the web browser about the type and the version of HTML used in building the web document.

### 10. How do you serve a page with content in multiple languages?
- lang attribute in HTML

```html
<!-- by default -->
<html lang='en'>  
```

```html
<!DOCTYPE html>
<html lang="en">

<body>
	<p>
		We can use different languages in the HTML
		document simply by defining the
		"lang" property
	</p>

	<p>French " <span lang="fr">Bonjour</span> "</p>
	<p>Spanish " <span lang="es">Hola</span> "</p>
	<p>Hindi " <span lang="hi">नमस्ते</span> "</p>
</body>

</html>
```

### 11. What kind of things must you be wary of when designing or developing for multilingual sites?
- SEO Search Engine Optimization: 
    - use the  ```lang``` attribute in the html tag
    - include the locale in the url ```en_US, zh_CN```
    - Webpages should use``` <link rel="alternate" hreflang="other_locale" href="url_for_other_locale">```
- Understanding the difference between locale and language
    - Locale settings control how numbers, dates, and times display for your region: which may be a country, or a portion of country or may not even honor country boundaries.
- Language can differ from countries.
- Do not concatenate the translated strings
- Formatting dates and currency
- Do not put text in the image

### 12. What are data- attributes good for?
- store extra data within the DOM
- Javascript access and CSS access


```html
  <article
    id="electric-cars"
    data-columns="3"
    data-index-number="12314"
    data-parent="cars">
    …
  </article>
```

```javascript
const article = document.querySelector("#electric-cars");
// The following would also work:
// const article = document.getElementById("electric-cars")

article.dataset.columns; // "3"
article.dataset.indexNumber; // "12314"
article.dataset.parent; // "cars"
```

```css
article::before {
  content: attr(data-parent);
}

article[data-columns="3"] {
  width: 400px;
}
article[data-columns="4"] {
  width: 600px;
}
```

- Not recommended: 1. data can be modified easily by user


### 13. Consider HTML5 as an open web platform. What are the building blocks of HTML5?

- Semantics - Allowing you to describe more precisely what your content is.
- Connectivity - Allowing you to communicate with the server in new and innovative ways.
- Offline and storage - Allowing webpages to store data on the client-side locally and operate offline more efficiently.
- Multimedia - Making video and audio first-class citizens in the Open Web.
- 2D/3D graphics and effects - Allowing a much more diverse range of presentation options.
- Performance and integration - Providing greater speed optimization and better usage of computer hardware.
- Device access - Allowing for the usage of various input and output devices.
- Styling - Letting authors write more sophisticated themes.


### 14. Describe the difference between a cookie, sessionStorage and localStorage.
- All of the above are key-value pairs store in the client side, they are only allowed to store string values
- localStorage:
    - providing much greater storage capacity 5mb, cookie 4kb
    - The data is not sent back to the server for every HTTP request
    - The data stored in localStorage persists until explicitly deleted. Changes made are saved and available for all current and future visits to the site.
    - It works on same-origin policy. So, data stored will only be available on the same origin.

- cookie:
    - The data is sent back to the server for every HTTP request
    - 4kb limit
- sessionStorage:
    - It is similar to localStorage.
    - The data is not persistent i.e. data is only available per window

### 15. Describe the difference between ```<script>, <script async> and <script defer>```.

- ```<script>``` HTML parsing is blocked, the script is fetched and executed immediately, HTML parsing resumes after the script is executed.

- ```<script async>``` The script will be fetched in parallel to HTML parsing and executed as soon as it is available (potentially before HTML parsing completes). Use async when the script is independent of any other scripts on the page, for example, analytics.

- ```<script defer>``` The script will be fetched in parallel to HTML parsing and executed when the page has finished parsing. If there are multiple of them, each deferred script is executed in the order they were encountered in the document. If a script relies on a fully-parsed DOM, the defer attribute will be useful in ensuring that the HTML is fully parsed before executing. A deferred script must not contain document.write.

### 16. Why is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?

- Placing ```<link>```s in the ```<head>```
    - It is the proper specification in building an optimized website.
    - When a page first loads, HTML and CSS are being parsed simultaneously; Both are needed to create the visuals in a website, allowing for a quick "first meaningful paint" timing.
    - If Not, there can be flashes of unstyled content (FOUC), which show a webpage with no styling applied.

- Placing ```<script>```s just before ```</body>```
    - ```<script>``` tags block HTML parsing while they are being downloaded and executed which can slow down your page. Placing the scripts at the bottom will allow the HTML to be parsed and displayed to the user first.
    - This ensures your code that needs to manipulate DOM elements will not throw an error and halt the entire script.

### 17. What is progressive rendering?
- Progressive rendering is the name given to techniques used to improve the performance of a webpage (in particular, improve perceived load time) to render content for display as quickly as possible.

- lazy-loading image
- minimum css
- async html elements


### 18. Why you would use a srcset attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.

You would use the srcset attribute when you want to serve different images to users depending on their device display width.

### 19. Have you used different HTML templating languages before?

EJS. they are more or less the same and provide similar functionality of escaping content and helpful filters for manipulating the data to be displayed.


### 20. What is the difference between canvas and svg?
- Canvas can be modified through script only, SVG can be modified through script and CSS
- Canvas has poor scalability. Hence it is not suitable for printing on higher resolution, SVG has better scalability. So it can be printed with high quality at any resolution
- SVG is vector based and composed of shapes. Canvas is raster based and composed of pixel.
### 21. What are empty elements in HTML?
An empty element is a component that doesn’t have any embedded elements or text elements.

```html
<area> <base> <br> <col> <embed> <img> <input> <meta> <param>
```

