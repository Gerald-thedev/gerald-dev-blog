## A Beginner's Guide To Understanding Specificity In CSS

Browsers have a way of reading code, usually from top to bottom, and the code that is at the bottom in CSS is most times considered more relevant to an element even if they have the same property name but different values. Although with CSS specificity it is totally different. You see the cover image of this article above, with the phone sitting on top of the CSS and JavaScript textbooks, that's a summary of CSS specificity. Imagine you suddenly get a notification on your phone from your mum and you had to choose between checking the notification on your phone or opening the CSS, or the JavaScript textbook, we can be certain that you'd rather check the notification on your phone first. Communicating with your mum will be the most relevant to you at that point in time. You might also prefer to study CSS over JavaScript because you consider yourself, someone who is more into aesthetics than logic.

In this article, we will be discussing how specificity works in CSS and how to target elements using selectors.  

## What is CSS Specificity? 
Specificity is simply a way web browsers try to decide how important a declaration is, regarding an element, i.e; how the declaration of the property's value is important or relevant to an element. After the decision is made by the browser, the property value is then applied.

Let us look at some examples to better understand how CSS specificity works.

#### Example 1

<iframe height="300" style="width: 100%;" scrolling="no" title="CSS specificity example 1" src="https://codepen.io/Mistar_codepen/embed/mdxPKzO?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/mdxPKzO">
  CSS specificity example 1</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

In this example, if you navigate to the CSS section of the code, you'll realize that we had the same selectors (the p selector) with the same property name but different values. The first selector has the property name, **color** with a value of **red** and the second selector which is also the p selector has a property name, color with a different value of **green**. We are aware of how browsers read code from top to bottom, so since the property value of green is beneath the property value of red, then the second declaration is of more importance to the p element, overriding the first declaration. 

If you notice, we also gave the first declaration a larger font size **100px** compared to the second declaration **20px**, but because browsers read our code from top to bottom, again, the second declaration of **font-size: 20px;** overrides the first declaration, if not, the font size would have been a lot larger than 20px. 

#### Example 2 

<iframe height="300" style="width: 100%;" scrolling="no" title="CSS specificity example 2" src="https://codepen.io/Mistar_codepen/embed/JjLXZVo?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/JjLXZVo">
  CSS specificity example 2</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

In this example, we gave a class to the opening (p) tag, **"paragraph1"**, and also gave it the color green and font size of 20px. Despite using a p selector and giving it a color red, the browser only recognized the **class** given to the paragraph because the **class selector**, "paragraph1" is of higher relevance compared to the p selector.

#### Example 3

<iframe height="300" style="width: 100%;" scrolling="no" title="CSS specificity example  3" src="https://codepen.io/Mistar_codepen/embed/abYNKeb?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/abYNKeb">
  CSS specificity example  3</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

For this third example, we added an **id selector** "more-specific" to the opening (p) tag. An id selector is considered to be more relevant than the class selector, despite the paragraph having both the id and class attributes. The new color of the paragraph will now be purple, even though browsers read our code from top to bottom and the ID selector is above the class selector. In this case, the ID selector is of more relevance, ignoring the styles applied to the class selector.

#### Example 4

<iframe height="300" style="width: 100%;" scrolling="no" title="CSS specificity example  4" src="https://codepen.io/Mistar_codepen/embed/GRxZBJv?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/GRxZBJv">
  CSS specificity example  4</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We have used an inline styling for the opening tag of the (p) element in this example and given it a hex code color value of **#27CEC2**, a very fine bluish color. As we can see, the inline styling is the most specific and relevant of them all. It overrides every other selector, including the ID and class selectors. This is because the styling given to the (p) element is directly done within the HTML file, it overrides all styles done in an external CSS file.  

## The **"!important"** property
**!important** is another CSS property that adds more importance to an element and overrides ALL the previous property values given to an element, irrespective of an inline style, an ID, or a class attribute.

<iframe height="300" style="width: 100%;" scrolling="no" title="!important property" src="https://codepen.io/Mistar_codepen/embed/abYmvme?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/abYmvme">
  !important property</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We have already established that inline styles are the most relevant to an element and an id attribute is of more relevance to an element compared to a class attribute, but in the CSS section of the code, you'll realize that the **p selector** has been given an **!important** property value after the color red. The !important property has overridden all other styles applied to the p element. This includes the inline style, the id, and class selectors given to the p element.   

### Specificity Hierarchy 

There is always a place for every CSS selector in terms of relevance and hierarchy.
The following hierarchy levels will be based on the importance of the CSS selectors.

- Inline styling - Done within the HTML file. This means that a style applied to an element within the HTML file is of more relevance to the style applied to an element within an external CSS file. `<p style="color: blue;">The paragraph</p>`

- ID selectors - IDs are denoted with a **#** symbol before the name of the ID. This means that an inline style is more relevant to an element compared to when given an ID name and is styled in an external CSS file. `<h2 id="sub-heading">Sub Heading</h2>` **#sub-heading {...}**

- Class selectors, pseudo-classes, and attribute selectors - classes are usually denoted with a dot, period, or full stop **" . "** symbol before the class name. `<p class="paragraph1">First Paragraph</p>`**.paragraph1 {...}**

Examples of pseudo-classes are **:link** **:visited** **:hover** **:active**

Examples of attribute selectors are **[target=_blank]** **[href="https"]**

- Elements and pseudo-elements - are the least relevant in terms of hierarchy. This is when you want to style an element using its tag. Examples are **h1**, **h2**, **p**, **div** etc.

Examples of pseudo-elements are **:before**, **:after**, **::first-line** etc. 

## Conclusion 
We discussed CSS specificity and the hierarchy of selectors in CSS with various examples showing you how each selector has more specificity over other selectors. Inline-styles are the most relevant to an element, although it is bad practice to style your elements using inline styles. Lastly, we looked at the !important property in CSS and saw how it shows more importance and relevance to an element. It overrides every other style given to an element.

Comments and questions are well appreciated and can be left in the comments section below.



  