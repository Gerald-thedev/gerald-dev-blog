## How To Use Various CSS Combinator Selectors

In CSS, specific elements can be targeted when applying styles to them in various ways. In this article, we will walk you through the different combinator selectors and how elements are being targeted.  

**Various Combinator selectors:**

-  Descendant Selector

- Child Selector

- Chained Class Selector

- Adjacent Sibling Selector

- General Sibling Selector

**Descendant Selector** - Just like how we are all descendants of our ancestors when we look at our family tree, the same principles apply to this. if there are any child elements of a parent element, those child elements will be targeted. 

It must not necessarily have to be a direct child of the parent. As long as the element being targeted is within a parent element. For example, having an anchor tag **a** within a div, that is nested inside a paragraph.

```
  <div>
      <p>This is a paragraph that has a <a href="#">LINK</a> nested within it.
      </p>
  </div>
```

```
div a {
    color: red;
}
```
"a" is a descendant of the div element. 

**Child Selector** - This is just like an individual being a direct child to their parents. Styles to be applied will only affect a direct child of the parent. Elements that are nested further down within the parent element will not be styled. An example will be an **li** element being a child of an unordered list. 

```
  <ul>
      <li><p>A paragraph with a link of the first item<a href="#">Item1</a></p></li>
      <li><p>A paragraph with a link of the Second item<a href="#">Item2</a></p></li>
  </ul>
```

```
  ul > li {
      color: red;
  }
```
The greater than sign **(>)** is used to link the parent element with the child element.

The color of the paragraphs changes to red, but not the link. The color of the link remains its default color which is blue.

**Chained Class Selector** - A chained class selector will select elements having their various class names, separated by a comma.

```
  <ul>
      <li><p class="class1">A paragraph with a link of the first item<a href="#">Item1</a></p></li>
      <li><p class="class2">A paragraph with a link of the Second item<a href="#">Item2</a></p></li>
  </ul>
```

```
  .class1, .class2 {
      color: yellow;
  }
```
This will change the colors of the elements having class 1 and class 2 to yellow. Only the colors of the paragraphs will change to yellow.

**Adjacent Sibling Selector** - This combinator selector will match an element that is the next sibling of another element. For example, if there are two paragraphs after an h1 tag, only the first paragraph will be targeted when styles are applied.

```
<h1>The main heading</h1>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Architecto, repellat?</p>
```
To target the first paragraph only, and not include the second paragraph, we use the plus sign **(+)** after the h1 tag, then the p tag.
```
h1 + p {
    color: green;
}
```
This will change only the color of the first paragraph to green.

** General Sibling selector** - This combinator selector will match elements that are siblings of one another. The elements that are siblings do not have to be arranged sequentially(on top of one another).

An example will be having an h1 tag and various p tags beneath.

```
<h3>A sub heading</h3>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
    <ul>
        <li>list1</li>
        <li>list2</li>
        <li>list3</li>
    </ul>
    <p>Lorem ipsum, <strong>consectetur adipisicing</strong> elit. Architecto, repellat?</p>
```
```
  h3 ~ p {
      color: red;
  }
```
This type of combinator selector will change the color of all the paragraphs to red. 

The sign **(~)** is used in this case, unlike how we used the plus sign (+) in the adjacent sibling selector.

Even though we have an unordered list in between the paragraphs that are siblings, the styles applied will still be visible.

**Conclusion**

We looked at various combinator selectors in CSS and different ways of targeting elements and how to apply styles to them in a specific way.

Kindly leave your comments and questions in the comments section below.










