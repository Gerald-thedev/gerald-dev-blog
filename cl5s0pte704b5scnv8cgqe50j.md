## Grid vs. Flexbox

Have you ever wondered about the difference between Flexbox and the Grid system?  Why you would need to learn both of them and not just choose one over another? While starting out, most developers said something along the lines of "Errmm... I am only going to use the grid system." Or "Hmmm...Flexbox is cool, I am sticking with only flexbox for my projects, I don't need to know the grid system." There were several other opinions and I must confess, I was once there, wanting to learn one over the other and not seeing the need of learning both. 

Although, when I took my time and did a lot of research on the use of both the grid system and flexbox, I instantly felt this power within. At this point, I thought I was Thanos from the Avengers :) I suddenly understood the difference and how I could utilize them to my advantage, and apply both to the projects I was working on. They had to become best friends, rather than enemies in terms of building layouts and neatly arranging items. 

The Grid system and Flexbox work together, and in this article, we shall be looking at them individually, their differences, and how to combine both of them when building layouts in CSS. 

### Prerequisities 
It is advised that you understand the basics of CSS layouts, this includes:

- The basics of the grid system.

- Some knowledge about flexbox.

## The Grid System
What is the grid system, you may ask? Well in simple terms, it is a layout tool used in CSS for a single page. It is mostly used for a two-dimensional layout, i.e; for both the horizontal **AND** vertical axis (rows and columns) at the **same time**. Assuming you want to build a layout for an entire page that comprises the header, the navigation bar, the main content, the aside, and the footer, this is where using the Grid system will come in handy. Let's look at a typical example of the grid system, and try to recreate a Rubix. 

### Example of the Grid system
<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/Mistar_codepen/embed/bGvBwbK?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/bGvBwbK">
  Untitled</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

You can see our multi-colored grid system in which we recreated a Rubix. Remember Grid system is used for both horizontal **AND** vertical axis(two-dimensional layout). If you don't apply the property name and value, i.e; **display: grid;** to the parent element(the main container), all the boxes will line up in a single column to the left-hand side of the container and overflow beyond the fixed height given to the parent element. This is because a div is a block-level element and will always start on a new line.

We have also used **grid-template-columns: repeat(4, 1fr)** to say we need 4 columns and each column should occupy only a fraction of the available space. Same thing we did for the rows, **grid-template-rows: repeat(3, 1fr)**. Lastly, we used a pseudo-class **.box:nth-child(number)** to style all the colored boxes numbering them from 1 to 12. We could have easily used the second class name, i.e .box1, .box2, .box3...etc but we just felt like showing you a different way of applying styles to the boxes.

We will not be going in-depth on how to create a grid system because that is an entire topic on its own.
Let's not get carried away and focus on the difference between the Grid system and Flexbox and knowing how to utilize both layout systems within our projects.   

Here is a typical example of how you can use the Grid system to create a page layout.
### The Grid System (Desktop view)

<iframe height="300" style="width: 100%;" scrolling="no" title="Untitled" src="https://codepen.io/Mistar_codepen/embed/abYBppM?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/abYBppM">
  Untitled</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Now, we can see how the grid system has been used to create an entire page layout which includes the header section, the aside section, the main content, and the footer section of the page.
We made use of **the grid-template-areas** property and assigned grid areas to the different sections of the page. 

Using the **grid-template-areas** property is the easiest way to create a page layout that makes sense to the eyes, although it's a personal preference. You can manipulate the layout and change how it should look on mobile view, tablet, and desktop view. Again, we shall not be going in-depth on how this layout was created.

We can create a mobile view by manipulating the **grid-template-areas** property and changing the layout to a single-column view.

### The Grid System(Mobile view)
<iframe height="300" style="width: 100%;" scrolling="no" title="Grid(Mobile view)" src="https://codepen.io/Mistar_codepen/embed/OJvWJEp?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/OJvWJEp">
  Grid(Mobile view)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Although, there seems to be an issue. We can see how the sections' titles are stacked in the top left-hand corner of each section, and we would like them to be centered in the middle of each section. Usually, we would try to use text-align, center, margins, paddings, and position properties like relative positioning to hack our way to the middle of each section(I was once guilty of this :) ) but this is where the use of Flexbox comes into play.

Before we dive into what flexbox is and how to use it, here's an example of how you'd align the titles of each section to the center with just three lines of code.
<iframe height="300" style="width: 100%;" scrolling="no" title="flexbox alignment" src="https://codepen.io/Mistar_codepen/embed/OJvpRqZ?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/OJvpRqZ">
  flexbox alignment</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

If you compare this with the previous layout just above, you will be able to tell the difference. The use of Flexbox is the difference. The titles of the former are all aligned to the top left-hand corner of each section, while the titles of the latter are all aligned to the center of each section.


## Flexbox
Flexbox, as opposed to the grid system, is simply a layout tool in CSS that is very useful in smaller areas of a webpage, especially within grid areas. The main feature of flexbox is to align items on a horizontal **OR** vertical axis, i.e; one-dimensional. Floats were once used for making layouts. Although it is believed that it has been replaced by flexbox to a certain degree and flexbox is here to stay. The use of flexbox has made the lives of developers a lot easier and we will show you how.

### Items Aligned Horizontally Using Flexbox
<iframe height="300" style="width: 100%;" scrolling="no" title="Flexbox1" src="https://codepen.io/Mistar_codepen/embed/dymOWbe?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/dymOWbe">
  Flexbox1</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Once the parent element is given a **display: flex;** property, this property's default behavior is to arrange the child elements in a row from left to right. No matter how many child elements you have, there will always be provision for another child element within that row. If you scroll to the CSS section of the code, you will realize that we commented out the **flex-wrap: wrap;** property.

Once we uncomment the flex-wrap property, we get exactly the same layout we got when we recreated the Rubix using the grid system.
<iframe height="300" style="width: 100%;" scrolling="no" title="Flexbox 2(flex-wrap)" src="https://codepen.io/Mistar_codepen/embed/abYBWNV?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/abYBWNV">
  Flexbox 2(flex-wrap)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Now, the **flex-wrap** property is used to determine whether the flex items (colored boxes) should be forced into a single line or if they should flow onto the next available row. Flexbox items (Boxes 5, 6, 7, and 8) are wrapped on the next row (2nd row), leaving the first row. Same as boxes 9, 10, 11, and 12 wrapped themselves on the third row of the container. For clarity, let's remove some of the colored boxes from our HTML files so that there will be less than 12 boxes. Let's leave 7 colored boxes so that you can clearly see how the flex-wrap property works.
<iframe height="300" style="width: 100%;" scrolling="no" title="flexbox3(7 boxes)" src="https://codepen.io/Mistar_codepen/embed/mdxOmBY?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/mdxOmBY">
  flexbox3(7 boxes)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We can see how the flex-wrap property works and just a side **note** unless you include the **align-content** property and set its value to **start**, you might see a gap between each row. Again, we are not going to go in-depth with all the properties you can find in flexbox. You can always explore different properties while learning the use of flexbox.

If you scroll to the CSS section of the code, you will notice that we applied **display: flex;** **justify-content: center;** and **align-items: center;** to the **.box** class so as to align the title of the boxes to the center of each box.

Now, let's look at a typical example of how you can combine both the Grid system and flexbox layouts on a web page. 

## Grid + Flexbox
<iframe height="300" style="width: 100%;" scrolling="no" title="Grid+Flexbox" src="https://codepen.io/Mistar_codepen/embed/KKoNmEq?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/KKoNmEq">
  Grid+Flexbox</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Let's just say the background colors of each section represent the layouts done using the grid system, i.e; the red, blue, green, and yellow backgrounds were derived using the grid system. The contents of each colored section have been aligned with the use of flexbox. 

For example, within the red section(Header section), **Code Bootcamp**, **Login**, and **Sign up** have been aligned with the use of flexbox creating that space between them. Same as for the images in the **Coding challenges** section, if we didn't have the **flex-wrap: wrap;** on the main-container class, the images would have been aligned on a single row, from left to right. Levels 3 and 4 wouldn't have wrapped on the second row, likewise levels 5 and 6, on the third row. The footer section also used the display flex property to align the social links horizontally.

Now, our webpage might not win a hackathon award but it sure passes across the message, which is, understanding how flexbox and the grid system can work together to create a nice layout for your webpage.
The layout for the different sections was created using the grid property, while the items that were placed within each grid area were aligned using the flex property(flexbox), besides the aside section.

As you can see, grid and flexbox work together and they complement each other. Using both of them gives you more power and "flexibility". I might be wrong but most developers, while starting out, used only the grid system and relied on it for building layouts. Some were probably skeptical about the use of flexbox and felt the need to only use the grid system in building projects. Once you get the hang of flexbox, you will begin to implement the flex property in your projects.

We recommend you go to this website, [flexbox froggy](https://flexboxfroggy.com/) to learn more about flexbox in a very interactive way. It's a game you can play and learn at the same time. The game is fun and it will solidify your knowledge and teach you the basics of flexbox and how to align items within an enclosed area.     

## Conclusion 
With this tutorial, we are sure that you will be able to differentiate between the use of the grid system and flexbox, and how they can be combined to create layouts of a webpage. It's totally okay to have knowledge of just the grid system. The main aim is to master it and be fluent in its application to your projects. Although, once you play the Flexbox froggy game, you'll soon realize the power of flexbox. Always keep this in mind, the grid system is for a two-dimensional layout mostly used for creating the layout of an entire page, both horizontal and vertical layouts at the same time. As for Flexbox, it is used for aligning items within an enclosed area. Flexbox is considered one-dimensional for either horizontal or vertical layouts.

Let us know your preference in the comments section below. Which would you prefer to use in your projects now you know the difference between the Grid system and Flexbox or would you rather use both?

  








