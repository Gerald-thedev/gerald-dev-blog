## CSS Grid For Absolute Beginners

Aren't you just tired of using margins, paddings, floats, and CSS position properties like relative for your layouts? The relative position property isn't even your relative, so why so attached to it? Eventually, things fall apart once you reduce the size of your viewport. Well, It's time to "float" away from such properties. You'll be amazed by the power of the grid system. The Grid system is one of the most commonly used tools for building layouts in CSS. If you want to build more complex layouts for a web page, the CSS grid is a reliable tool to use. It is more than just a brunch of lines going across each other.

Unlike flexbox, which is one-dimensional for either the horizontal or vertical axis, CSS grid is a two-dimensional layout system for both the horizontal and vertical axis. It is certain that there are limitations to using flexbox. Grid gives you more flexibility and freedom in placing items where you choose on a web page. You are always in control of how you want your layouts to look.

In this article, we shall be discussing how to make proper use of the grid system in a simple way that you'll enjoy making use of it for building layouts. We shall also discuss all the different methods in which the grid property can be applied and the different techniques for creating amazing grid layouts in CSS.

## Grid containers & items

First, let's try to understand what grid containers and grid items are.

- **Grid containers** - are elements that contain all the child elements within them, also referred to as the parent element. This is where the **display: grid;** property will be set, including the row heights and column widths.

- **Grid items** - these are the child elements of the grid container, i.e the elements within the grid container. Any grid item within the main grid container can also become a grid container, therefore having its own child elements which becomes a grid item of the nested grid. Yes, a grid can be nested within another grid.

So, we set a **display: grid;**  to the grid container like this: `#container {display: grid;}`

## Grid template columns

You will expect to see some magic happen when you apply this property. You might think that the grid will automatically be created with only that single line of code. The truth is, nothing will happen until we define the width of the columns by making use of the **grid-template-columns** property. Let's say we want 3 columns, of different column sizes in percentages, we can use the **grid-template-columns** property to define their sizes.

<iframe height="300" style="width: 100%;" scrolling="no" title="The Grid System" src="https://codepen.io/Mistar_codepen/embed/BarRGON?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/BarRGON">
  The Grid System</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Let's walk through the code:

- In the HTML section of the code, we have defined a grid container having an id of  container `<div id="container">`

- We have created 6 divs named item1 - 6 within the grid container. These are the grid items.

- In the CSS section of the code, we applied styles to the grid container (the id selector named container), applying a **display: grid;** property to it. Even as we have applied the display grid property to the grid container, the grid items (div items) will still be stacked on one another because of the default behavior of block-level elements.

- We will only see the effect of the grid taking shape when we include the **grid-template-columns** property. We said initially that we want 3 columns so we gave the grid-template-columns property values of 20% 40% and 40%. 

- We set a grid gap of 5px for both columns and rows using the **grid-gap** property. If we wanted to set a gap between rows only, then we can use the **row-gap** property, likewise, we can also use the **column-gap** property to set only gaps between columns. The width of the grid container is 500px and the height is 200px.  

- For clarity on how the columns have been divided, we gave both items 1 and 4 a background color of blue, items 2 and 5 with background colors of white, and items 3 and 6, with background colors of red.

- You'll notice that we used the **overflow-x** property and set its value to **hidden** because the use of percentages can bring about inconsistent results with grid items having to overflow the grid container. Be cautious while using these kinds of values. There are better values to use called **fractional units (fr)**. We will explain what they mean and how to use them later on.

## Grid template rows

We have been talking about grid template columns using percentages, well, you can also use pixel values to set the column widths, likewise the row heights of the grid. We make use of the **grid-template-rows** property to set the row heights.

<iframe height="300" style="width: 100%;" scrolling="no" title="Grid system(px and rows)" src="https://codepen.io/Mistar_codepen/embed/ZExKNeg?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/ZExKNeg">
  Grid system(px and rows)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We have created 10 grid items, we also created 5 columns and 2 rows. The rows were created using the **grid-template-rows** property. The first row has a row height of 200px while the second row has a row height of 100px. 

Although we created those 5 columns by writing 100px five times. So imagine we wanted 10 columns, does it mean we are going to write 100px ten times? I don't think we want to be doing that, let alone if we wanted 20 or 30 columns, that will be a lot tedious doing that with the way we just did. There is a shorter way of defining the number of columns we want and we use something called the repeat function.

## The repeat Function

To avoid repetition of code, let us try and create a single row with 5 columns using the repeat function rather than writing 100px five times as we did earlier.

<iframe height="300" style="width: 100%;" scrolling="no" title="grid system(repeat)" src="https://codepen.io/Mistar_codepen/embed/qBomeZv?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/qBomeZv">
  grid system(repeat)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We have used the repeat function to say we would like a column width of 100px repeated 5 times within a single row height of 200px. The code is written like this `grid-template-columns: repeat(number of times to repeat, dimension);` That was a lot easier and quicker than writing 100px five times. 


## Fractional Units
We should always run away from pixel units and percentage values because these kinds of values will affect us in terms of responsive web design (creating designs for small screen devices like tablets or mobile)

To prevent such issues that have to do with responsive web design, it is highly recommended to make use of fractional units. You are probably wondering what fractional units are. Well, it just means occupying the available space within a particular area. 

Let's assume we try to define 2 columns of a grid and we will like to make use of fractional units also known as **"fr"**, we can say the first column can occupy only 1fr of the available space, while the second column can occupy 2fr of the remaining space, which will be 2 times the first column. 1fr unit can represent 25% of the available space, while 2fr will represent 50% of the available space.

The repeat function can be used with fractional units just like how they'll work with pixel units. Here is an example using fractional units.

<iframe height="300" style="width: 100%;" scrolling="no" title="grid system(Fractional units)" src="https://codepen.io/Mistar_codepen/embed/oNqWKQX?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/oNqWKQX">
  grid system(Fractional units)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Since we used the repeat function and said the columns should be repeated twice, with the first column occupying 1fr of the available space while the second column occupies the remaining space.
From the example above, column 1 is occupying a smaller portion compared to column 2. Columns 3 and 4 are just a repetition of columns 1 and 2 since we indicated by using the repeat function to repeat the pattern twice.

## The minmax () function
When we try to define the height of the grid, we might be tempted to use the **grid-template-rows** property, but you will soon realize that doing this will only make the content of the grid area overflow out of its surrounding.

Here is an example of how the content of our grid would look if we use the **grid-template-rows** property and give it a fixed height of 150px.

<iframe height="300" style="width: 100%;" scrolling="no" title="grid row(overflow)" src="https://codepen.io/Mistar_codepen/embed/qBojWpq?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/qBojWpq">
  grid row(overflow)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

You can see that in column 2, row 1, some of our texts are being cut off.

In contrast to the example above, we will look at how to prevent our content from getting cut off by making use of the **grid-auto-rows** property and also using the **minmax() function** by setting a minimum row height of 100px and setting the max to auto so that our content can stretch no matter how long our content may be.

Here is an example of using the minmax function so as to accommodate our content properly without any issues of overflowing text or content.

<iframe height="300" style="width: 100%;" scrolling="no" title="grid system(grid-auto-rows)" src="https://codepen.io/Mistar_codepen/embed/GRxEKWO?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/GRxEKWO">
  grid system(grid-auto-rows)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We can see that the difference is quite clear and the issue of overflowing content has been fixed.

## Gridlines
Gridlines are referred to as numbered horizontal and vertical lines that separate different column and row cells. Every column has a gridline to its left and to the right, likewise rows, every row has a gridline placed at the top and bottom of the row. These gridlines separate each row or column from the next.
Here is a representation of gridlines within a grid system.

<iframe height="300" style="width: 100%;" scrolling="no" title="grid system(gridlines)" src="https://codepen.io/Mistar_codepen/embed/xxWrVQR?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/xxWrVQR">
  grid system(gridlines)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

The white lines between each column and between each row are referred to as gridlines. Although, there are invisible gridlines that you can't see at both ends of the entire grid columns and grid rows. To better understand gridlines, just know that since we have 5 columns, there will be 6 vertical gridlines. The first gridline starts from the left-hand side of column 1 row 1, while the last gridline on the first row ends on the right-hand side of column 5 row 1.

Same for the rows, we can see that there is only one white gridline separating the first and second rows. Just like the columns, we have invisible gridlines both on the top of the first row and the bottom of the second row. Since there are 2 rows, then we have 3 horizontal gridlines from top to bottom. The best way to understand gridlines is to add 1 to the number of columns or rows you have. So, if you have 8 columns then you know that there are 9 vertical gridlines, and if you have 4 rows, then there are 5 horizontal gridlines.

## Placing items using Gridlines
The position of a grid item can be changed in regards to where it occupies in the grid system with the use of gridlines. We can always change the structure of our grid items and where they are placed. Assuming we would like a grid item to take up an entire row, like creating a header for our web page, we could make use of the **grid-column** property and indicate what gridline we would like the grid item to start from and what gridline we would like it to end at. 

<iframe height="300" style="width: 100%;" scrolling="no" title="Grid system(Placing items)" src="https://codepen.io/Mistar_codepen/embed/eYMRdmy?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/eYMRdmy">
  Grid system(Placing items)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We have changed the title of the grid item having a class of **.item1** to **HEADER** and in the CSS section of the code, we used the **grid-column** property and indicated that we want the grid item (HEADER) to start at gridline 1, occupying the entire columns of the first row which ends at gridline 6. Remember, since there are 5 columns then there will be 6 gridlines. 

Same thing we did for the Grid item2. We placed the item starting at gridline 1, then ending on gridline 4, making it occupy 3 columns of the second row. If you feel confused, use grid items 5 - 9 to guide you on where these grid items are being placed with the use of the gridlines.   

We could also make use of the **grid-row** property to make grid items occupy multiple rows. 

<iframe height="300" style="width: 100%;" scrolling="no" title="grid system(placing items rows)" src="https://codepen.io/Mistar_codepen/embed/gOeRwRr?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/gOeRwRr">
  grid system(placing items rows)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

In the example above, we used the grid-row property and made Grid item 2 occupy the second and the third row. We placed Grid item2 starting on gridline 2(of the row gridline), spanning across two rows, and ending on gridline 4. Again, let grid items 4 and 6 be your guide on the gridlines. This layout might be different from what you're used to, this is because we only made use of the **border-radius** property to give the grid items those curved edges. 

We can recreate the above layout with the use of **span** and the combination of gridlines like this: `grid-column: 1 / span 5;`

<iframe height="300" style="width: 100%;" scrolling="no" title="Grid system(Span)" src="https://codepen.io/Mistar_codepen/embed/WNzOGYd?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/WNzOGYd">
  Grid system(Span)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

In the layout above, we said for the grid column, let the header (grid item1) start from gridline 1 and span across 5 columns. For grid item 2, we also said that the grid column should start from gridline 1 and span across 3 columns, while the grid row started from gridline 2 and spanned across 2 rows. In the CSS section of the code, you'll see how we placed the Grid items 3 and 4.

## Grid template areas 
This property is used to specify the areas of grid items within a grid layout. With the use of the **grid-template-areas** property, each row is defined using quotation marks **("")**. We define this property like this: `grid-template-areas: "header header header";` This has created one row with three columns. It might seem confusing at first, but not to worry, it will make sense. Let's take a look at a typical example of using the grid-template-areas property.

<iframe height="300" style="width: 100%;" scrolling="no" title="Grid system(Template areas)" src="https://codepen.io/Mistar_codepen/embed/BarZQPO?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/BarZQPO">
  Grid system(Template areas)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

We have used the **grid-template-areas** property to structure the entire layout of the page. This is the structure of the web page
```
grid-template-areas: "header header header header"
                     "aside main main main"
                     "aside main main main"
                     "footer footer footer footer";
``` 
We have indicated that the header section should take up 4 columns of the first row, the aside section should take up the first column of the second and third rows, and the main section should start on the second column and span across the third and fourth columns, likewise occupying the second and third rows, then we have also indicated that the footer section should start on the first column of the last row and span across the second, third and fourth columns.

We also made use of the **grid-area** property to place these grid items, matching them with the names we used on our **grid-template-areas** property. For example, the header section was given a grid area of header, aside matched with aside, etc... You can name the grid template areas anything but it is only reasonable they match accordingly so that you don't get confused.

## Ordering of Grid items
We can change the order in which grid items are arranged, using the **order** property. For example, making the first grid item become last or moving the second grid item to become the first grid item, and so on.   
Here's an example of using the order property to rearrange grid items.  

<iframe height="300" style="width: 100%;" scrolling="no" title="grid system (Order)" src="https://codepen.io/Mistar_codepen/embed/gOeRgdN?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/gOeRgdN">
  grid system (Order)</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

The last grid item has become the first, the fourth has become the second, and so on...

## Conclusion
The grid system is an ultimate layout tool in CSS as we have discussed a lot about its use. Let's recap what has been discussed in this tutorial. We defined what grid containers and items are, we looked at some of the various properties used like the grid template columns and rows. The repeat and minmax functions were also discussed, and we saw how items are being placed using gridlines and the grid template areas property. Lastly how grid items can be re-ordered from their initial positions. Constant practice while using this tool and its properties will help you understand all its quirks soon enough. Just play with all the properties. 

You can always leave your questions and comments in the comments section below. 

 

























