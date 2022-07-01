## How To Add CSS To Your HTML Files

CSS, the Cascading Style Sheets is known for its beauty. It brings the content and structure of your HTML page to life. Have you ever seen your web page without CSS? You tend to cringe, right? Not having to style your web page with CSS is like looking at a rainbow in black and white. It will definitely not be an amazing sight we are used to. The moment you add one style to your web page, even if it means adding a text color to your heading, you begin to experience something called "Love at first sight." :)

In this article, I will be breaking down the **3 ways** to Insert CSS into your HTML page, from the least preferred way to the most recommended way.

## Prerequisites

This tutorial assumes that you have the following:

- A text editor (Notepad, Visual Studio Code, Atom, Sublime Text, etc)

- A basic understanding of HTML and how to structure the contents of a web page.

- A basic understanding of CSS, styling a web page and giving declarations to various selectors. 


## Three Ways to Insert CSS

There are three ways in which you can insert a style sheet to your HTML page:

- Inline CSS

- Internal CSS

- External CSS

## Inline CSS
An inline style is a type of CSS styling that is usually applied to a **single element.**
An element is styled using inline CSS by adding the "style" attribute to the element's opening tag.

You can apply any CSS property within the style attribute and the corresponding value of the property. 

Styles are applied to the element in double quotes, separated by a colon and ended with a semi-colon, for each property name and its corresponding value.

## Example

<iframe height="300" style="width: 100%;" scrolling="no" title="Inline Css" src="https://codepen.io/Mistar_codepen/embed/gOeYQMP?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/Mistar_codepen/pen/gOeYQMP">
  Inline Css</a> by Gerald Ofokansi (<a href="https://codepen.io/Mistar_codepen">@Mistar_codepen</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### An explanation of what is happening in the code above...
The word "style" within the opening tag of the h1 and p elements is called an **Attribute name**, while the equals sign "=" is known as an **Assignment**, assigning values to the attribute name (style). 

Within the quotes on the left-hand side, we have the **property name**, then a colon, and after the colon is the **property value** ending with a semi-colon.

For example, **color**, is a property name, while **blue**, is a property value. Each property's name and value are separated by a colon and ended with a semi-colon.

We used rem as a unit of measurement because it is a **Relative value**. So 1rem is equivalent to 16px, therefore 2rems is equivalent to 32px(16px multiplied by 2).


- First, we set the body's background color to black.

- We have set the heading which is **h1** to have a text color of blue, which has also been aligned to the right-hand side of the web page.

- As for the first paragraph just below the main heading element, we set a border around it, which has a border thickness of 2px, solid and the color of the border is white. 

We also set a background color of red around the paragraph with a width of 25rems and a height of 15rems. No alignment was given to the paragraph, so it stays at its default position (on the left-hand side of the web page). We also increased the font size of the paragraph to 2rems.

- As for the second paragraph, we gave it a font size of 3rems which is **3 times** larger than the default font size (1rem or 16px), that is, 3rems multiplied by 16px. We also changed the text color to orange.

"Please note that this method of styling a web page is highly **NOT** recommended." This method of styling is mostly used for developing email templates.

## Internal CSS

This method of styling is used for a **single** web page that has a unique style to it. The internal style is done within the head section of the HTML page, using the style element, where you have the meta tags and the title element. 

## Example

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>How To Add Css to your HTML Files</title>
    <style>
        body {
            background-color: yellow;
        }

        h1 {
            font-family: serif;
        }

        p {
            text-align: center;
            font-size: 2rem;
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>This is an internal CSS Style</h1>
    <p>Internal CSS Example.</p>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corrupti, inventore!</p>
</body>
</html>
```
As you can see, the internal CSS style method is different from the inline CSS style. The styling of the web page is done within the head section of the HTML page.

- We have changed the background color of the body to yellow.

- The heading element has a font family of serif and is no longer aligned to the right, back to its default position, compared to the inline style example.

- Both paragraphs have been aligned to the center of the web page, with font sizes of 2rems and a font style of Italic. 

Note that the p elements being styled affect both paragraphs, unless you want to differentiate them with different styling, then you can use either a **class** or an **ID**.

Classes and IDs are different topics entirely. I would not want to get you carried away. Let's save that topic for another day.
For now, our focus is on the different ways of adding CSS to our HTML page.

## Result

![A web page with a yellow background color, a heading, and two paragraphs](https://cdn.hashnode.com/res/hashnode/image/upload/v1655772585109/2WWxIcAkz.png align="left")

By now, you should know the difference between inline CSS and internal CSS. The former is done within the opening tag of the individual elements, while the latter is done within the head section of the HTML page, usually, if the entire web page has unique styling. 

## External CSS
With this method of styling, the look of an entire website can be altered and changed just from a **single file**. 

We use the **link element** to create a connection between our style sheet and the HTML page.

The link element should be in the head section of the HTML page just like how you would apply styles to an HTML page using the internal CSS method of styling. 
The only difference between the two is that rather than using the style element, we use the **link element**.

The link element is an empty element, meaning it does not have a closing tag.

The link element should have these three attribute names and their corresponding values:

- **href**- this attribute specifies the **path** to the external CSS file, which is usually placed in a folder called CSS, styles, or stylesheet. Although you can name it whatever you like, it is only reasonable to assign the folder, a name that corresponds with what will be within the folder.


- **rel**- this specifies the **relationship** between the external CSS file that has been created and the HTML page it is being linked to. The attribute value should be **stylesheet** when linked to the external CSS file.


- **type**- this specifies the **type of document** that is to be linked with the HTML page. The attribute value should be **text/css**.

## Example

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>How To Add CSS to your HTML Files</title>
    <link rel="stylesheet" href="css/style.css" type="text/css">
</head>
<body>
    <h1>This is an External CSS Style</h1>
    <h2>External CSS Example.</h2>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias autem laboriosam provident consectetur commodi sed quaerat vel repellendus mollitia hic!</p>
</body>
</html>
```
Above, is our HTML page which has our external CSS file linked to it. It is within the head section of the page, beneath the title element.

As you can see, it includes the three main attributes we talked about earlier, the **rel** attribute name and the corresponding value of **stylesheet** showing the relationship between both files.

The **href** attribute specifies the path to the CSS file with the corresponding value of **css/style.css**.

Lastly, the **type** attribute with a value of **text/css**.

### Below is the External CSS file, which the above HTML file is linked to

```
body {
    background-color: crimson;
}

h1 {
    text-align: center;
}

h2 {
    color: white;
    background-color: black;
    width: 10rem;
    margin: 0 auto;
    text-align: center;
    border: 1px solid white;
    padding: 4rem;
}

p {
    font-family: 'Times New Roman', Times, serif;
    font-style: italic;
    color: white;
    font-size: 2rem;
}
``` 
The external CSS file is on its own, separate from the HTML file. We only use the link element with the attributes within the head section of the HTML file to connect both files together.

This is so that changes can be easily made on the entire project just by altering the contents of a single file. 

**NOTE** that this is the **most recommended** way of applying styles to a web page. The reason is that the structure of your HTML files looks **cleaner** and it is **smaller in size**. You can use the same CSS file to style **multiple pages** of your website.

## Result

![An image showing the use of External CSS](https://cdn.hashnode.com/res/hashnode/image/upload/v1655816593122/hzahoig39.png align="left")

## Conclusion

In this tutorial, we have learned about the different ways of adding CSS styles to an HTML page.
Let us recap what has been covered in this tutorial. We talked about Inline CSS, Internal CSS, and External CSS. External CSS is said to be the most recommended way of styling web pages. We also looked at the various attributes used to link an external CSS file with an HTML file. Just in case you were using both inline CSS which is bad practice and internal CSS, with this tutorial, I am certain you now know better, which way is the best of all the methods that have been discussed. 

If you have any questions, you can leave them in the comments section below.













 