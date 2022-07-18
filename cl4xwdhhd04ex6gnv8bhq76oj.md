## CSS Position Properties

Every element in CSS needs to be positioned in a particular area on the web page. Various position properties have certain behaviors they exhibit when used on an element. We have five different position properties that can be used, depending on where you want the element to be placed.
You know how the navigation bar sticks along with you when scrolling through a page on a website, or how some of those annoying adverts remain in a fixed position that you can't get rid of? Not to mention those annoying cookies that pop up at the bottom of the page you sometimes don't feel like accepting, simply because they intend not to offer you an actual cookie? 

Well, those elements were given a particular position, and those position properties all exhibit their various behaviors on a web page. 
 
In this article, we will be breaking down the five position property values and how you can apply them to an element within a web page.

## Prerequisites 
For this tutorial, you really don't have to be a wizard at CSS, you only need to know the basics and how to structure the contents in an HTML file. 

## The Five Position Properties

- static

- relative

- absolute

- fixed

- sticky

For all the above position properties to work effectively, the **position** property is set first, then the elements can be positioned using the coordinates, **top**, **bottom**, **left** and **right** properties, depending on the values that have been set.

## position: static;

By default, HTML elements are always positioned statically. We are aware that divs are block-level elements, so they usually start on a new line and occupy the full width of the web page, unless defining the widths ourselves. When an element is given the position static, nothing happens. The position of that element remains the same. Elements given the position static, are positioned according to the normal document flow of the web page.

 #### Example of position: static;

<iframe height="300" style="width: 100%;" scrolling="no" title="Static Position Property" src="https://codepen.io/Mistar_codepen/embed/jOZgawK?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/jOZgawK">
  Static Position Property</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

You can see that nothing happens to the first and second elements(red and blue boxes) as they have been given static positions. This is the default behavior. If you navigate to the CSS section of the code, you'll realize that we gave a coordinate position to the second element with a background color of blue, **left: 40rem;** (this should have moved the element 40rems away from its default position) but nothing changed.

## position: relative;
When an element is given the **position: relative;** without any coordinate properties, i.e; **left**, **right**, **top**, **bottom**, the element stays in the same position, and nothing changes. Until the element is given a coordinate property, i.e; **left: 50px;** **top: 20px;** it will always remain in its original position just like the position static. It does not affect the normal document flow in the sense that other elements around it, still recognize that it is there. "A picture is worth a thousand words" so here is an example below.

#### Example of position: relative;

<iframe height="300" style="width: 100%;" scrolling="no" title="Static Position" src="https://codepen.io/Mistar_codepen/embed/jOZgmrM?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/jOZgmrM">
  Static Position</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

From the result above, we can see that the red box has been given a position of relative and a coordinate position of **left: 100px;** which has moved the element 100px away from its default position. It also doesn't affect the flow of other elements, meaning that the remaining elements, i.e; the blue, green, and purple boxes, will always remain in their default position even if the red box has been given a relative position with a coordinate of left: 100px; or more.

## position: absolute; 
When an element is given a **position: absolute;** the element will be taken out of the normal document flow. This means that it no longer retains the default position and acts like it is being floated in the air above others (similar to how floats work).

Other surrounding elements are affected by the element given a position of absolute. If the parent container that is containing the child element is not given a position of relative i.e (parent container, position: relative;), then the child element that has been given a position of absolute, will take a reference point from the body of the web page, and not the parent element containing the child element. 

#### Example of position: absolute;

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/Mistar_codepen/embed/qBxepQp?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/qBxepQp">
  Untitled</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

From the result above, you can see how the position absolute works. If you look through the CSS section of the code, we intentionally commented out the position: relative; given to the parent element, which is the container containing the colored boxes.

Without the parent container element having a relative position, you can see that the red box that has been given a position of absolute, takes a reference point from the body of the web page. It has been given a coordinated position of **left: 20px;** So the red box positions itself 20px away from the body of the web page, and not its immediate parent container that is containing all the colored boxes.

Below, is an example of when the parent container is given a position of relative. You will notice that the child element (the red box with a position of absolute) now takes a reference point from the parent container and is no longer taking its reference point from the body of the web page.

<iframe height="300" style="width: 100%;" scrolling="no" title="Absolute Position Property Example 2" src="https://codepen.io/Mistar_codepen/embed/eYVqVzE?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/eYVqVzE">
  Absolute Position Property Example 2</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

As you can see from the CSS section of the code, we uncommented the position relative to the parent container we had initially and now, the child element (the red box) now takes a reference point from its container, i.e; the parent element, and no longer from the body of the web page.  

## position: fixed;
An element that is given the **position: fixed;** will always remain in the same fixed position even upon scrolling. It is taken out of the normal document flow and affects the surrounding elements. For the element to exhibit the behavior of a fixed position, other elements must be present on the web page. That is, an element given a position fixed will have no effect on its own because it needs to float above other elements for this property to work. 

With other elements present, the surrounding elements assume it is not there. The element with a fixed position acts as a floated element with its surrounding elements underneath. The element does not accept any parent element even if the container i.e; the parent element, that is containing the child element is given a position value of relative. 

An element given a position, fixed, takes its reference point from the body of the web page.

#### Example of position: fixed;

<iframe height="300" style="width: 100%;" scrolling="no" title="position fixed" src="https://codepen.io/Mistar_codepen/embed/oNEKEJR?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/oNEKEJR">
  position fixed</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## position: sticky;

The **position: sticky;** is really tricky, to be honest, but hey, not to worry, we will explain all its quirks and help you understand better how it works. It is quite similar to position fixed, but it has its differences. Unlike the position fixed, it is not taken out of its normal document flow and does not affect the surrounding elements. Although, only when you scroll through the page, that is when you see its effects. You can mostly find this position sticky property used in navigation bars of a website that scrolls along with the user, usually sticking to the top of the web page.

Unlike an element with a fixed position that doesn't need a parent element(container), which usually takes a reference point from the body of the web page, an element given a position sticky can have a parent container. An element with a position of sticky needs surrounding elements for the property to have any effect. 

Another tricky sticky behavior is that it needs a coordinated position value of **top: 0;** or any value of your choice for it to take effect if not, you will get frustrated by why the position sticky isn't working as it should. Any value that is given to the top coordinate, i.e, top: 10px; takes a reference point from the top of the viewport which will stick on the page as you scroll.

You could also try coordinated values of **left**, **right**, and **bottom**. Play around with the values and see what it results to.

One last thing about position sticky is that it is currently not supported by Safari, so it requires a **-web-kit-sticky** prefix which will serve as a fallback for the actual property of position: sticky; The prefix is usually above the position sticky property, like this: 

```
position: -web-kit-sticky;
position: sticky;
```

#### Example of position: sticky; without a top coordinate value

<iframe height="300" style="width: 100%;" scrolling="no" title="Sticky position property" src="https://codepen.io/Mistar_codepen/embed/rNdBjvP?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/rNdBjvP">
  Sticky position property</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

If you go to the CSS section of the code snippet, you will notice that we intentionally commented out the coordinate value of top: 0; just for you to see the effect of not including a coordinate to the sticky position property. The result is that it will not work as expected.

#### Example of position: sticky; with a top coordinate value

<iframe height="300" style="width: 100%;" scrolling="no" title="Sticky position property with top coordinate value" src="https://codepen.io/Mistar_codepen/embed/jOzNBNe?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/jOzNBNe">
  Sticky position property with top coordinate value</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Now that we included the coordinate value by removing the comment around the property **top: 0;** you can see that the nav bar is sticky and our code works perfectly. Isn't that awesome? Just remember that sticky position and coordinate value work hand in hand. 

Let's look at one last scenario where the sticky position can once again be tricky, shall we? We will change the dimensions of the blue box to a nav bar and place it outside its parent container and give it a position of sticky. In case you have a situation where your nav bar is beneath other elements or it isn't floating above other elements, you can make use of the **z-index** property. This is due to the inconsistencies in CSS. 

What is **z-index** property you may ask, and what is it possibly used for? Well, the z-index property is used to place an element above another element or overlap an element over another. If you have an element behind another element and you want the element behind, to be in front, then the z-index property is used. 
The z-index property uses numbers as its property values. The default value of any element is 0. You can also use a negative number as an element's z-index property value. 

#### An example explaining the z-index property
Giving the blue nav bar a z-index property of **-1** will make the element appear below other elements. Remember, the default value for every element is 0. Since 0 is greater than (-1) the result below is expected.

<iframe height="300" style="width: 100%;" scrolling="no" title="Sticky position scenario z-index" src="https://codepen.io/Mistar_codepen/embed/ExEYWgV?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/ExEYWgV">
  Sticky position scenario z-index</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Giving the blue nav bar a positive z-index value produces the result below.

<iframe height="300" style="width: 100%;" scrolling="no" title="sticky z-index property scenario (b)" src="https://codepen.io/Mistar_codepen/embed/GRxKXEy?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/GRxKXEy">
  sticky z-index property scenario (b)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

## Conclusion 
A recap of what has been discussed in this article. We talked about the five different CSS position properties, their various behaviors on the web page, and how they are used to position elements. We talked about the similarities between the fixed and sticky positions, likewise the different behaviors the sticky position can exhibit. We also found out that the sticky position property isn't supported by Safari and will use a prefix as a fallback. Lastly, we discussed the z-index property and how it can be used.
Just in case you had a tough time battling how to use these position properties, I hope that this article is useful to you, to help understand the topic better.

If you have any questions, you can leave them in the comments section below.



 






