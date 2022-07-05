## Understanding The CSS Box Model

## Introduction
A box, we always tend to think outside of it whenever we want to have thoughts that are unconventional. In CSS, its representation is entirely different. The box model is a way CSS handles its layout and design. Every element you can find in HTML is always wrapped by an imaginary box. This box becomes visible only when this single line of code, "**border: 2px solid black;**" is added to an element. All of a sudden, your vision is no longer blurry. Just this line of code can bring about clarity. 

In this article, we will be discussing the main components that make up the box model, which are; the **margin**, **border**, **padding**, and the **content** itself. 


![A diagram showing all the components of the box model](https://cdn.hashnode.com/res/hashnode/image/upload/v1656626132754/VIIYFzH-l.jpg align="left")

Above, is a simple diagram that describes all the components of the box model.

Let's take a look at each component individually, starting with the content itself.

## Content
This is where you'll see texts and images wrapped in an imaginary box.
Usually, HTML is used to display the contents of a web page and also its structure, so we always have something like this:

<iframe height="300" style="width: 100%;" scrolling="no" title="content of a Box Model" src="https://codepen.io/Mistar_codepen/embed/BaryONW?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/BaryONW">
  content of a Box Model</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

This is how the contents are displayed since they are all block-level elements, it is not quite clear what is happening as we only aligned the text of every element to the center and removed default margins and paddings set by the browser. Remember that block-level elements occupy the full width of the viewport and start on a new line. This is the default behavior of all block-level elements. To make things clearer, we will be using you as an example to clarify the components of the box model. For now, let us assume that you represent the content.

## Padding
Paddings surround the content and they are the areas that give the content some space and room to breathe. Without borders, padding always seems invincible. We have established that you are the content. Assuming you want to go shopping for clothes, you wouldn't buy clothes that are too tight on you, or show that you have a protruding belly right? You'd instead buy clothes that fit and at least give you some freedom and enough room to breathe. That space and freedom given to you by the clothes you wear is a representation of padding. The larger the clothes, the larger the padding, keeping in mind that you represent the content.

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/Mistar_codepen/embed/jOzEvzp?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/jOzEvzp">
  Untitled</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Everything begins to make sense once you have borders surrounding the content. So let's look at how borders work.

## Border
Borders are wrapped around the content and its padding within. With the borders added, you will see that the natural behavior of block-level elements is much clearer compared to when we had no borders. We also notice that every block-level element is taking up the full width of the viewport. Now you understand why we said everything begins to make sense when you add just that single line of code, **"border: 2px solid black;"**. 

If you represent the content and the freedom given to you by the clothes you wear is a representation of padding, then borders will be you in a car or you, making a phone call in a telephone booth. It means you're within an enclosed space. The car you are in or the telephone booth will be a representation of the border.  Making another reference to padding, padding could also be the space around you within the car you are in or the telephone booth. 

<iframe height="300" style="width: 100%;" scrolling="no" title="Borders(Box model)" src="https://codepen.io/Mistar_codepen/embed/GRxgXrN?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/GRxgXrN">
  Borders(Box model)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Margin
Margins are the areas outside of the borders. The only time you can see the margin of an element is when it has surrounding elements enclosed by their borders. The spacing between two or more boxes is called a margin. For example, when you are driving your car and you leave some gap to the vehicle in front of you in case the vehicle comes to a sudden stop so as to not bash into the vehicle. Well, that gap can be referred to as margin. The spacing between two cars on different lanes is also known as margin. Below is an example of boxes arranged horizontally with margins separating the boxes. You can make reference to each box in the examples as cars, and the spaces around them are the margins.

<iframe height="300" style="width: 100%;" scrolling="no" title="Margins(Box Model)" src="https://codepen.io/Mistar_codepen/embed/rNdaqVa?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/rNdaqVa">
  Margins(Box Model)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Conclusion
Let's recap what has been learned in this tutorial. We have learned the main components that make up the box model, which are margin, border, padding, and content. We used you as an example to clarify each component and gave examples and scenarios where these components can be applicable. With this tutorial, it is certain that you now understand all the components that make up the box model and how to apply them to different elements on a web page.

Questions and comments can be left in the comments section below.







