---
title: CSS related notes
date: 2022-07-11 15:10:22
banner_img: https://tva2.sinaimg.cn/large/0060lm7Tly1ftg6wuhgywj31hc0u0wjr.jpg
index_img: https://tva2.sinaimg.cn/large/0060lm7Tly1ftg6wuhgywj31hc0u0wjr.jpg
tags: [CSS, interview, frontend]
categories: Interview Questions
---

*This article was written by  [Career Karma](https://careerkarma.com/).* I am just studying this material.


### **Question 1:** Tell me about an approach you took to decide the layout of a project you worked on. What pushed you to choose one type of layout (Flexbox/Box/Grid) over another?


This is an interesting type of question because it requires you to think back to previous projects you have worked on. Before going into a technical or behavioral interview, be sure to study up on previous projects you completed to recall choices made.

You don’t necessarily need to defend your answers, but you need to basically speak to your reasoning. The interviewers would like to hear your thought process on why you chose the approach you did. This is valuable information to them because it hints at how you might approach a problem at their company.

#### What should you study about layout?

When it comes to the [differences](https://careerkarma.com/blog/css-grid-vs-flexbox/) between Flexbox, Box, and Grid, there are a couple of points to remember so you can reason through your job interview questions:

\1. [Box model](https://careerkarma.com/blog/css-box-model/) was the first of the three layouts styles to be created. Block boxes are the main types of containers used in the box model, but inline-boxes are used (they just don’t use all the properties that block boxes do).

Each box, or container, consists of a margin, a border, padding, and content. Limitations of the box model include responsive and/or adaptive layout issues because of the static or fixed nature of the layout. The need to use the [clearfix hack](https://careerkarma.com/blog/css-clearfix/) when you have float elements is also an issue with the box model.

\2. Flexbox model was introduced after the box model to improve on some of the box model’s limitations in regards to positioning. It still uses all of the pertinent parts of the box model, but has been expanded to allow for more adaptive or responsive design.

Be sure to know that flexbox is used when you care more about the flow of the content so it can be more responsive than about the actual design of the page.

\3. Grid model was the last of the three layout types to be introduced. It’s becoming more popular due to its ability to completely control content placement. It is still, however, not as popular a solution as flexbox is.

When you discuss the reasoning behind choosing box, flexbox, or grid, be sure to focus on the purpose of the layout.

- **Does the flow of the content matter?** *Use CSS Flexbox*
- **Does the content placement matter?** *Use CSS Grid*
- **Are you working with legacy code using CSS Box Model several years old?** *Use the inherited system unless there is a budget to change to one of the other preferred methods.*

### **Question 2:** How does CSS actually work ?

This question tests your ability to be able to describe what CSS is from a technical standpoint.

Start from the very beginning and describe that CSS literally means Cascading Style Sheets. It uses three ways to style the HTML document:  inline-styling, internal stylesheet, and external stylesheet.

The stylesheet is how we essentially decorate our web page. We use [CSS selectors](https://careerkarma.com/blog/css-selectors/) to create rules for those elements. When the CSS renders, it will take the CSS, and apply it to the document from the top to the bottom.

If there is a selector that is repeated in the stylesheet, the newest rule(s) overwrite the previous ones. Inline styles and the !important keyword maintain the highest importance and will overwrite CSS written in the stylesheet.

### **Question 3:** Describe pseudo-elements and pseudo-classes, discuss the differences between the two, and what they are used for.

Pseudo-elements and pseudo-classes are quite often conflated. They are two distinct concepts in CSS. This question is designed to see if you know the difference.

The similarity between the two is that they are keywords that are added to a selector that lets you style the selector in a specific way.

A **pseudo-element** is added to a selector when you want to style a specific part of the selected element.

```
p::selection {
 background-color: yellow;
}
```

The `::selection` pseudo-element styles the `<p>` tag when a user highlights text in that element. Other popular pseudo-elements are `::first-letter` and `::first-line`.

In contrast, the **pseudo-class** is added to a selector when you want to control the styling when an element is in a particular *state*. This applies not only to the document tree, but also to the location’s history.

```
button:hover {
 background-color: blue;
 color:white;
}
 
a:visited {
 color: orange;
}

a:hover {
 color: yellow;
}
```

All you need to remember really is that the pseudo-element styles specific parts of an element and the pseudo-class styles a specific state of an element.

### **Question 4:** Explain the concept of specificity.

[CSS Specificity](https://careerkarma.com/blog/css-specificity/) concerns itself with how style rules are applied to an HTML document. Each type of selector has a number associated with it. The higher the number, the higher the specificity. Inline-styling has the highest specificity, along with ids. Universal selectors have the lowest specificity.

When a specificity is higher, that means those styling rules will win over any sort of cascading rules.

### **Question 5:** What does a preprocessor do and why would it be advantageous to use one?

A preprocessor like SASS or LESS allows you to do a number of things:  assign variables, create mixins, and use nested rules. It makes the coding process simpler and allows your CSS to be nested like your HTML. To be used it needs to be compiled into a single CSS file that is then linked to your HTML Document.

Using a preprocessor like LESS or SASS cuts down on code reuse, assigns color schemes to variables, and prevents unintended behavior because your code is more dynamic due to the use of variables.

If there comes a time when you need to change the font or the color scheme, for instance, you can change it in one spot instead of 100 spots because you have it declared as a variable at the top of your LESS or SASS files. Preprocessors can be super useful.

### **Question 6:** Tell me about the CSS Box model and its constituent elements.

The CSS Box Model was the first of the layout models that were introduced in CSS. It consists of margin, padding, content, and border.

1. The **margin** is indicative of how far away you want your boxes to be from each other. It’s the area outside the border.
2. **Padding** is the area in between the content and the border. The more padding there is, the more room there is between the content of your box and the border itself.
3. The **border** of a box lays in between the padding and the margin. It frames padding and the content of the box.The feature of the box is the **content**. It’s what makes the box, a box.
4. The feature of the box is the **content**. It’s what makes the box, a box.

**Note:** By default, CSS’s `box-sizing` property is `content-box`. To have more control over the size of the boxes on your page, change your `box-sizing` property to `border-box`. You can use the universal selector `(*)` to do so at the top of your CSS.

### **Question 7:** How would you select every paragraph with a class name of `about-me` that is a child of a div?

```
div > .about-me {
 color: red;
}
```
