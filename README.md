# HTML Tutorial

A comprehensive guide to CSS, covering topics from the basics of selectors and box model to advanced topics like flexbox, grid, transitions and animations, media queries, and performance optimization. Perfect for anyone looking to learn or improve their CSS skills.

# Table of Contents

 * [CSS](#css)
 	* [History](#history)
	* BASIC
      * [Basic CSS structure](#structure)
      * [CSS Selectors](#selectors)
      * [CSS Box Model](#boxmodel)
      * [CSS Display and Visibility](#displayandvisibility)
      * [CSS Floats and Clearfix](#floatsandclearfix)
      * [CSS Text and Font Properties](#textandfontproperties)
      * [CSS Colors and Backgrounds](#colorsandbackgrounds)
      * [CSS Borders](#borders)
      * [CSS Margins and Padding](#marginsandpadding)
      * [CSS Units of Measurement](#units)
	* INTERMEDIATE
      * [CSS Flexbox](#flexbox)
      * [CSS Grid](#grid)
      * [CSS Transitions and Animations](#transitionsandanimations)
      * [CSS Media Queries](#mediaqueries)
      * [CSS Pseudo-classes and Pseudo-elements](#pseudo)
      * [CSS Positioning](#positioning)
      * [CSS Overflow](#overflow)
      * [CSS Shadows and Gradients](#shadowsandgradients)
      * [CSS Transforms](#transforms)
	* ADVANCED
      * [CSS Variables](#variables)
      * [CSS Preprocessors ( Sass, Less, Stylus )](#preprocessors)
      * [CSS Postprocessors ( PostCSS )](#postprocessors)
      * [CSS Animation Libraries ( Animate.css, Bounce.js, Hover.css, etc. )](#animationlibraries)
      * [CSS Frameworks ( Bootstrap, Foundation, Materialize, etc. )](#frameworks)
      * [CSS Performance Optimization](#performance)
      * [CSS Architecture](#architecture)
      * [CSS Testing and Debugging](#testinganddebugging)
 * [Conclusion](#conclusion)

<a name="css"></a>

## CSS

CSS stands for **Cascade Style Sheets**. It is a language that is used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG or XHTML). In short, CSS gives web developers the ability to create visually engaging and well-structured websites that are optimized for a wide range of devices and screen sizes.

<a name="history"></a>

## History

CSS was originally developed by Håkon Wium Lie and Bert Bos in 1994. It was originally a proprietary language developed by Netscape for their web browser Netscape Navigator. It was later standardized by the World Wide Web Consortium (W3C) in 1996.

Here's a brief overview of the major versions of HTML:

`CSS 1.0 (1996)` - The first version of CSS was introduced and it provided basic styling capabilities such as font control, text alignment, and background color.

`CSS 2.0 (1998)` - The second version of CSS added support for media types, downloadable fonts support, and improved positioning capabilities.

`CSS 2.1 (2006)` - This version of CSS made minor corrections to the previous version, but it was largely the same.

`CSS 3.0 (1999)` - CSS 3 brought many new features to the table, including rounded corners, shadows, and text shadows, and it also introduced new selectors and media queries. The CSS3 modules were released incrementally and are still in development as of 2023.

It's important to note that while these are the major releases of CSS, there are also minor releases that are released on a regular basis. These minor releases are called **CSS Level 3** and **CSS Level 4**. These are not to be confused with the major releases of CSS, which are called **CSS 3** and **CSS 4**.

# BASIC

<a name="structure"></a>

### Basic CSS structure

Basic CSS structure refers to the way CSS styles are written and organized in a stylesheet. The basic structure of a CSS stylesheet includes the following components:

- **Selectors** - Selectors are used to target HTML elements in the DOM(Document Object Model). DOM is a tree-like structure that represents the HTML elements in a web page. They are used to select the elements you want to style. Selector can be based on element type (e.g. `h1`, `p`, `div`), class (e.g. `.class-name`), or ID (e.g. `#id-name`).

- **Properties** - Properties defines what aspects of the selected elements you want to change (e.g. `color`, `background-color`, `font-size`)

- **Values** - Values are the actual settings you want to use for the selected properties (e.g. `red`, `blue`, `20px`)

Here's an example of a basic CSS structure:

```css
selector {
    property: value;
}
```

<a name="selectors"></a>

### CSS Selectors

CSS selectors are used to target HTML elements in the DOM(Document Object Model). DOM is a tree-like structure that represents the HTML elements in a web page. They are used to select the elements you want to style. Selector can be based on element type (e.g. `h1`, `p`, `div`), class (e.g. `.class-name`) or ID (e.g. `#id-name`).

Here are some examples of CSS selectors:

```css
/* Selects all elements of type h1 */
h1 {
    color: red;
}

/* Selects all elements with class name "class-name" */
.class-name {
    color: red;
}

/* Selects all elements with id "id-name" */
#id-name {
    color: red;
}
```

There are so many other selectors available. Here are some of the most commonly used CSS selectors:

- **Universal selector** - `*`
- **Element Type selector** - `h1`, `p`, `div`
- **Class selector** - `.class-name`
- **ID selector** - `#id-name`
- **Attribute selector** - `[attribute]`, `[attribute=value]`, `[attribute~=value]`, `[attribute|=value]`
- **Pseudo-class selector** - `:hover`, `:active`, `:focus`, `:first-child`, `:last-child`, `:nth-child()`
- **Pseudo-element selector** - `::first-letter`, `::first-line`, `::before`, `::after`

We will learn more about these later in this tutorial.

<a name="boxmodel"></a>

### CSS Box Model

The CSS box model is a concept that describe the layout of HTML elements on a web page. It is made up of the following components:

- **Content** - The content of the box, where text and images appear.

- **Padding** - Clears an area around the content. The padding is transparent.

- **Border** - A border that goes around the padding and content.

- **Margin** - Clears an area outside the border. The margin is transparent.

![CSS Box Model](https://github.com/amulifts/css-tutorial/blob/main/images/boxmodel.png)

In the image above,

- Top left section has CSS properties of the P element.
- Bottom left section has HTML code of the P element.
- Top right section shows, Box model diagram of the P element (copied from chrome browser’s developer tool section).
- Bottom right section shows, actual output of this HTML code.

It's important to note that the width and height properties only apply to the content area. The padding, border, and margin are not included in the width and height of an element.

<a name="displayandvisibility"></a>

### CSS Display and Visibility

The CSS display property specifies the type of rendering box used for an element. The display property can have one of the following values:

- **block** - This generates a block element box that starts on a new line and stretches out to the left and right as far as it can. It is used for elements such as headings (`h1`, `h2`, `h3`, `h4`, `h5`, `h6`), paragraphs (`p`), divs (`div`), and more.

- **inline** - This generates a one-line box that does not start on a new line and stretches out as far as it can in both directions. It is used for elements such as images (`img`), spans (`span`), and more.

- **inline-block** - This generates a one-line box that does not start on a new line and stretches out as far as it can in both directions. It is used for elements such as images (`img`), spans (`span`), and more.

- **none** - This generates no box at all. It is used for elements such as scripts (`script`), meta (`meta`), and more.

The CSS visibility property specifies whether or not an element is visible. The visibility property can have one of the following values:

- **visible** - This makes the element visible.

- **hidden** - This makes the element invisible, but it still takes up space in the layout.

- **collapse** - This makes the element invisible, and it does not take up space in the layout.

Here's an example of CSS display and visibility:

```css
/* This makes the element invisible, but it still takes up space in the layout */
.hidden {
    display: none;
}

/* This makes the element invisible, and it does not take up space in the layout */
.collapsed {
    visibility: collapse;
}
```

<a name="floatsandclearfix"></a>

### CSS Floats and Clearfix

In CSS, floating elements are used to allow elements to float to the left or right of their parent container, with text and other elements flowing around them. This can be useful for creating multi-column layouts or for positioning elements such as images and captions. The float property can have one of the following values:

- **left** - This floats the element to the left of its container.

- **right** - This floats the element to the right of its container.

- **none** - This makes the element not float.

- **inherit** - This specifies that the float value should be inherited from the element's parent.

Here are some examples of CSS floats:

```css
/* Floats the image to the left */
img {
    float: left;
}

/* Floats the image to the right */
img {
    float: right;
}
```

And here's an example of a multi-column layout using floats:

```html
<div class="column">
    <img src="image1.jpg" alt="Image 1">
    <p>Some text.</p>
</div>
```

However, floating elements can sometimes cause unexpected behavior and layout issues, such as elements being moved out of their parent container or text overlapping floating elements. To fix these issues, a clearfix solution is often used.

The CSS clear property specifies on which sides of an element floating elements are not allowed to float. The clear property can have one of the following values:

- **left** - This specifies that no floating element should be to the left of the element.

- **right** - This specifies that no floating element should be to the right of the element.

- **both** - This specifies that no floating element should be to the left or to the right of the element.

- **none** - This specifies that floating elements can be on either side of the element.

- **inherit** - This specifies that the clear value should be inherited from the element's parent.

The clearfix solution uses a clear property to clear both the left and right float values, effectively making the parent container aware of the floated elements. This can be done by adding a clearfix class to the parent container, like this:

```css
.clearfix:after {
    content: "";
    display: table;
    clear: both;
}
```

And then adding the clearfix class to the parent container, like this:

```html
<div class="clearfix">
    <div class="element">Element 1</div>
    <div class="element">Element 2</div>
</div>
```

<a name="textandfontproperties"></a>

### CSS Text and Font Properties

A wide range of CSS properties can be used to style text and fonts. Here are some of the most commonly used properties:

| Property | Description |
| --- | --- |
| font-size | Specifies the size of the text |
| font-family | Specifies the font family for the text |
| font-weight | Specifies the weight of the text |
| color | Specifies the color of the text |
| text-align | Specifies the horizontal alignment of the text |
| text-decoration | Specifies the text decoration (e.g. underline, overline, line-through) |
| text-shadow | Specifies the shadow effect of the text |
| text-transform | Specifies the capitalization of the text |
| letter-spacing | Specifies the spacing between characters in the text |
| line-height | Specifies the line height of the text |
| word-spacing | Specifies the spacing between words in the text |

These properties can be used to style text in a variety of ways. Here are some examples:

```css
/* Sets the font size to 20px */
p {
    font-size: 20px;
}
```

You can try out other text and font properties.

<a name="colorsandbackgrounds"></a>

### CSS Colors and Backgrounds

A wide range of CSS properties can be used to style colors and backgrounds. Here are some of the most commonly used properties:

| Property | Description |
| --- | --- |
| background-color | Specifies the background color of an element |
| background-image | Specifies an image to use as the background of an element |
| background-repeat | Specifies whether the background image should be repeated |
| background-position | Specifies the starting position of a background image |
| background-attachment | Specifies whether a background image should scroll with the rest of the page, or be fixed |
| background-size | Specifies the size of the background image |
| background | A shorthand property for setting all the background properties at once |

These properties can be used to style colors and backgrounds in a variety of ways. Here are some examples:

```css
/* Sets the background color to red */
div {
    background-color: red;
}
```

You can try out other color and background properties.

<a name="borders"></a>

### CSS Borders

A wide range of CSS properties can be used to style borders. Here are some of the most commonly used properties:

| Property | Description |
| --- | --- |
| border | A shorthand property for setting all the border properties at once |
| border-width | Specifies the width of the border |
| border-style | Specifies the style of the border |
| border-color | Specifies the color of the border |
| border-radius | Specifies the radius of the border |

These properties can be used to style borders in a variety of ways. Here are some examples:

```css
/* Sets the border width to 5px */
div {
    border-width: 5px;
}
```

You can try out other border properties.

<a name="marginsandpadding"></a>

### CSS Margins and Padding

`Margin` is the space outside the border of an element, while `padding` is the space between the border of an element and its content. Both can be controlled using CSS, and they can be set using specific values for each of the four sides of an element (top, right, bottom, left). Here are some examples:

```css
p {
    margin: 20px;
    padding: 10px;
}
```

In this example, a margin of 20 pixels has been set for all four sides of the p element, and a padding of 10 pixels has been set for all four sides of the p element. This will create 20 pixels of space outside the p element, and 10 pixels of space inside the p element.

The above example can also be written like this:

```css
p {
    margin: 20px 20px 20px 20px;
    padding: 10px 10px 10px 10px;
}
```

<a name="units"></a>

### CSS Units of Measurement

CSS uses a variety of units of measurement to specify the size and length of elements in a web page. These units can be divided into two categories: absolute and relative. `Absolute units` are fixed, and do not change based on the size of the screen or the browser window. `Relative units` are relative to the size of the screen or the browser window, and will change based on the size of the screen or the browser window.

Here are some of the most commonly used units of measurement:

- **px** - Pixels are absolute units of measurement. One pixel is equal to one dot on the screen. This is the default unit of measurement for CSS.
- **em** - Ems are relative units of measurement. One em is equal to the current font size. For example, if the current font size is 16px, then 1em is equal to 16px.
- **rem** - Rems are relative units of measurement. One rem is equal to the font size of the root element. For example, if the font size of the root element is 16px, then 1rem is equal to 16px.
- **%** - Percentages are relative units of measurement. One percent is equal to 1% of the size of the parent element. For example, if the width of the parent element is 1000px, then 50% is equal to 500px.
- **vh** - Viewport height is a relative unit of measurement. One viewport height is equal to 1% of the height of the browser window. For example, if the height of the browser window is 1000px, then 50vh is equal to 500px.
- **vw** - Viewport width is a relative unit of measurement. One viewport width is equal to 1% of the width of the browser window. For example, if the width of the browser window is 1000px, then 50vw is equal to 500px.
- **vmin** - Viewport minimum is a relative unit of measurement. One viewport minimum is equal to 1% of the smaller of the height or width of the browser window. For example, if the height of the browser window is 1000px and the width of the browser window is 500px, then 50vmin is equal to 250px.
- **vmax** - Viewport maximum is a relative unit of measurement. One viewport maximum is equal to 1% of the larger of the height or width of the browser window. For example, if the height of the browser window is 1000px and the width of the browser window is 500px, then 50vmax is equal to 500px.

# INTERMEDIATE

<a name="flexbox"></a>

### CSS Flexbox

CSS Flexbox is a layout mode in CSS that makes it possible to arrange elements in one-dimensional, either row or column, layouts and also distribute space between elements in a more flexible and efficient way than traditional layout methods, such as block or inline-block.

With Flexbox, you can control the direction of elements (row or column), their alignment (start, end, center, space between, etc.), their order, and how they grow or shrink to fill available space.

Here's an example of a Flexbox layout:

```html
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
</div>
```

```css
.container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.item {
  flex: 1;
}
```

In this example, the `.container` class sets the container to use Flexbox as its layout mode. The **flex-direction** property sets the direction of elements to be in a row. The **align-items** property aligns all child elements to the center of the container. The **justify-content** property distributes space between the child elements evenly.

The `.item` class sets the **flex** property to 1, which means that each item will take up an equal amount of space within the container.

With these basic Flexbox properties, you can create a range of layouts with ease. However, there are many other properties you can use to control the behavior of Flexbox elements, and you can find more information in the official `Flexbox documentation`. Some of the more commonly used properties are listed below:

- **flex-direction** - Sets the direction of elements to be in a row or column.
- **align-items** - Aligns all child elements to the start, end, center, or stretch of the container.
- **justify-content** - Distributes space between the child elements evenly, or to the start, end, or center of the container.
- **flex-wrap** - Sets whether child elements wrap to the next line or not.
- **flex-flow** - A shorthand property for the flex-direction and flex-wrap properties.
- **order** - Sets the order of child elements.
- **flex-grow** - Sets the amount of space child elements should take up within the container.
- **flex-shrink** - Sets the amount of space child elements should take up within the container when the container is smaller than the sum of the child elements.
- **flex-basis** - Sets the initial size of child elements.
- **align-self** - Aligns a single child element to the start, end, center, or stretch of the container.
- **align-content** - Aligns all child elements to the start, end, center, or stretch of the container when there is extra space in the cross-axis.

<a name="grid"></a>

### CSS Grid

CSS Grid is a layout system that allows developers to create a grid structure for their web pages. It provides a way to define rows and columns in a web page, making it possible to place elements into specific grid cells and arrange them in a specific way.

CSS Grid works by defining a grid container that holds all of the grid items. The grid container has properties such as **grid-template-rows**, **grid-template-columns**, and **grid-template-areas** that allow the developer to specify the number of rows, columns, and their sizes. Then, each item in the grid is assigned to a specific row and column using the grid-row and grid-column properties.

Some of the benefits of using CSS Grid include the ability to create complex grid structures, control the size and position of grid items, and the ability to control the flow of content in the grid. Additionally, CSS Grid allows for responsive design, so the grid can be adapted to different screen sizes and devices.

Here's an example of a CSS Grid layout:

```html
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
</div>
```

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  grid-gap: 10px;
}

.item {
  background-color: #eee;
  border: 1px solid #ccc;
  text-align: center;
}
```

In the above example, the grid container has a `display` property of `grid`, which creates a grid structure. The **grid-template-columns** property specifies that there should be three columns, each with a fraction of the available space (1fr). The **grid-template-rows** property specifies two rows, each with a specific height (1fr and 1fr). Finally, the **grid-gap** property sets the gap between grid items to 10px.

Each grid item is given a class of **grid-item** and has a background color, border, and centered text. By using CSS Grid, you can easily create a grid structure that organizes and aligns your content in a flexible and responsive way.

The above example can be written in a more concise way using the **grid-template** property:

```css
.container {
  display: grid;
  grid-template: 1fr 1fr / 1fr 1fr 1fr;
  grid-gap: 10px;
}
```

The **grid-template** property is a shorthand property for the **grid-template-rows**, **grid-template-columns**, and **grid-template-areas** properties.

The above example can be further simplified by using the **repeat** function:

```css
.container {
  display: grid;
  grid-template: repeat(2, 1fr) / repeat(3, 1fr);
  grid-gap: 10px;
}
```

The **repeat** function takes two parameters: the number of times to repeat the value, and the value to repeat. In the above example, the **repeat** function is used to repeat the **1fr** value twice for the **grid-template-rows** property, and three times for the **grid-template-columns** property.

<a name="transitionsandanimations"></a>

### CSS Transitions and Animations

CSS Transitions allow you to change the properties of an element smoothly from one state to another. For example, you can use CSS transitions to smoothly change the background color of a button when it is hovered over by the mouse cursor. Transitions are defined using the transition property, which takes several parameters such as the property to be transitioned, the duration of the transition, and the type of transition (e.g., linear, ease-in, ease-out).

Here's an example of a `CSS transition`:

```html
<button class="button">Click Me</button>
```

```css
.button {
  background-color: #eee;
  border: 1px solid #ccc;
  padding: 10px;
  transition: background-color 0.5s ease-in-out;
}

.button:hover {
  background-color: #ddd;
}
```

CSS Animations, on the other hand, allow you to create more complex animations, such as a bouncing ball or a rotating wheel. Animations are defined using the @keyframes rule, which specifies the intermediate states of the animation and the styles for those states.

Here's an example of a `CSS animation`:

```html
<div class="ball"></div>
```

```css
/* CSS for the bouncing ball animation */
.ball {
  width: 50px;
  height: 50px;
  background-color: #eee;
  border: 1px solid #ccc;
  border-radius: 50%;
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(100px);
  }
  100% {
    transform: translateY(0);
  }
}
```

```css
/* CSS for the left-to-right moving ball animation */
.ball {
    width: 100px;
    height: 100px;
    background-color: red;
    border-radius: 50%;
    position: relative;
    animation: move 2s infinite;
}
@keyframes move {
    0% {
        left: 0;
    }
    50% {
        left: 300px;
    }
    100% {
        left: 0;
    }
}
```

<a name="mediaqueries"></a>

### CSS Media Queries

CSS Media Queries is a technique for adapting the presentation of a website based on different conditions such as screen size, device type, and orientation. It allows you to create different styles for different devices, making your website more responsive and accessible.

A media query consists of a media type, and zero or more expressions that check for the conditions of specific media features. For example, you can use a media query to specify styles only for devices with a screen width of at least 720 pixels:

```css
@media screen and (min-width: 720px) {
  /* Styles for devices with a screen width of at least 720px */
}
```

You can also use media queries to specify styles based on other conditions such as device type, orientation, and aspect ratio. This makes it possible to create a single HTML document that can be displayed optimally on a wide range of devices, from desktop computers to smartphones and everything in between.

Here's an example of a `CSS media query`:

```css
/* Default styles for all devices */
body {
  font-size: 16px;
  background-color: lightgrey;
}

/* Media query for smaller screens */
@media screen and (max-width: 720px) {
  body {
    font-size: 14px;
    background-color: lightblue;
  }
}
```

In the above example, the default styles for the body element are defined first. Then, a media query is used to specify styles for devices with a screen width of 720 pixels or less. In this case, the font size and background color of the body element are changed.

<a name="#pseudo"></a>

### CSS Pseudo-classes and Pseudo-elements

CSS pseudo-classes and pseudo-elements are special keywords added to selectors that allow you to apply styles to elements based on their state or location within the document.

Pseudo-classes are keywords added to selectors that specify a special state of the selected element. For example, the :hover pseudo-class can be used to specify a style for when the mouse cursor is hovering over an element.

Here's an example of a `CSS pseudo-class`:

```html
<button class="button">Click Me</button>
```

```css
.button {
  background-color: #eee;
  border: 1px solid #ccc;
  padding: 10px;
}

.button:hover {
  background-color: #ddd;
}
```

The above example uses the **:hover pseudo-class** to specify a style for when the mouse cursor is hovering over the button.

Pseudo-elements are keywords added to selectors that allow you to style a specific part of the selected element. For example, the ::first-letter pseudo-element can be used to specify a style for the first letter of a paragraph.

Here's an example of a `CSS pseudo-element`:

```html
<p class="paragraph">
  Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</p>

```

```css
.paragraph {
  font-size: 16px;
}

.paragraph::first-letter {
  font-size: 24px;
  font-weight: bold;
}

/* Or */
```

The above example uses the **::first-letter pseudo-element** to specify a style for the first letter of the paragraph.

There are many other pseudo-classes and pseudo-elements that you can use to style your web pages.

Some of the most commonly used `pseudo-classes` are:

| Pseudo-class | Description |
| --- | --- |
| :hover | Specifies a style for when the mouse cursor is hovering over an element |
| :active | Specifies a style for when an element is being activated by the user |
| :focus | Specifies a style for when an element has focus |
| :visited | Specifies a style for links that have already been visited |
| :link | Specifies a style for links that have not yet been visited |
| :first-child | Specifies a style for the first child of an element |
| :last-child | Specifies a style for the last child of an element |
| :nth-child(n) | Specifies a style for every nth child of an element |
| :not(selector) | Specifies a style for all elements that are not matched by the selector |

Some of the most commonly used `pseudo-elements` are:

| Pseudo-element | Description |
| --- | --- |
| ::first-letter | Specifies a style for the first letter of a paragraph |
| ::first-line | Specifies a style for the first line of a paragraph |
| ::before | Inserts content before an element |
| ::after | Inserts content after an element |
| ::selection | Specifies a style for the selected text |
| ::placeholder | Specifies a style for the placeholder text |
| ::value | Specifies a style for the value of an input element |

These are some of the most commonly used pseudo-classes and pseudo-elements. There are many more that you can use to style your web pages.

<a name="positioning"></a>

### CSS Positioning

CSS positioning is the way to control the layout and position of elements on a web page. It helps to specify the exact location of an element in the context of the parent container. There are several position values in CSS, including `static`, `relative`, `fixed`, `absolute` and `sticky`.

The position property can have one of the following values:

- **static** - is the default position value and means that the element will be positioned according to the normal flow of the document.

- **relative** - positioning allows you to specify the position of an element relative to its default position. For example, you can use `top`, `right`, `bottom`, and `left` properties to move an element away from its default position.

- **fixed** - positioning is used to fix an element to a specific location on the screen, regardless of scrolling. For example, you can use the `top` and `right` properties to specify the location of the element on the screen.

- **absolute** - positioning is similar to fixed positioning, but it positions the element relative to its nearest positioned ancestor, rather than the viewport.

- **sticky** - positioning is used to position an element relative to the viewport, but it will stick to its default position until a specified offset position is reached.

Here are some examples of CSS positioning:

```css
div {
  position: absolute;
  top: 20px;
  right: 20px;
}
```

You can try out other values of position property.

<a name="overflow"></a>

### CSS Overflow

The CSS overflow property is used to control how content that exceeds the boundaries of an element is displayed. The overflow property can have one of the following values:

- **visible** - The content is not clipped and will be visible outside the element's box. This is the default value.

- **hidden** - The content is clipped, and the rest of the content is hidden and not visible.

- **scroll** - A scrollbar is added to the element to enable the user to scroll through the content that exceeds the element's boundaries.

- **auto** - A scrollbar is added only if the content exceeds the element's boundaries.

Here are some examples of CSS overflow:

```html
<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec
  euismod, nisl sit amet ultricies lacinia, nunc nisl lacinia
  torto
</p>
```

```css
p {
  width: 200px;
  height: 100px;
  overflow: scroll;
}
```

In the above example, the `div` element has a width of **200px** and a height of **100px**. The overflow property is set to scroll, which means that a scrollbar will be added to the div element if the content inside it exceeds the boundaries of the div element.

<a name="shadowsandgradients"></a>

### CSS Shadows and Gradients

CSS shadows and gradients are used to add shadows and gradients to elements. `CSS shadows` are used to add shadows to elements, while CSS `gradients` are used to add gradients to elements.

`CSS shadows` are created using the box-shadow property. You can specify the size, color, and direction of the shadow, as well as its blur radius and spread radius by using the following list of properties respectively:

- **offset-x** - specifies the horizontal distance from the element to the shadow.

- **offset-y** - specifies the vertical distance from the element to the shadow.

- **blur-radius** - specifies the blur radius of the shadow.

- **spread-radius** - specifies the spread radius of the shadow.

- **color** - specifies the color of the shadow.

Here are some examples of CSS shadows:

```css
.shadow-box {
  box-shadow: 10px 10px 5px #888888;
}
```

```css
.shadow-box {
  box-shadow: 10px 10px 5px 5px #888888;
}
```

The above examples show how to add shadows to elements using the box-shadow property.

`CSS gradients`, on the other hand, are created using the background-image property and the linear-gradient function. You can specify the start and end colors of the gradient, as well as its direction by using the following list of properties respectively:

- **start-color** - specifies the start color of the gradient.

- **end-color** - specifies the end color of the gradient.

- **direction** - specifies the direction of the gradient.

Here are some examples of CSS gradients:

```css
.gradient-box {
  background-image: linear-gradient(to right, #FF0000, #FFFF00);
}
```

The above example shows how to add a gradient to an element using the **background-image** property and the **linear-gradient** function.

With CSS shadows and gradients, you can add visual interest to your web pages and make them stand out.

<a name = "transforms"></a>

### CSS Transforms

CSS Transforms allow you to change the **shape**, **size**, and **position** of an element in a web page. This can be useful for creating animations, visual effects, and responsive designs. You can use CSS transforms to `translate`, `rotate`, `scale`, and `skew` elements.

- **scale** - specifies the size of the element.

- **rotate** - specifies the rotation of the element.

- **translate** - specifies the position of the element.

- **skew** - specifies the skewing of the element.

Here are some examples of CSS transforms:

```html
<div class="box"></div>
```

```css
.box {
    width: 100px;
    height: 100px;
    background-color: blue;
    transform: translate(50px, 50px); 
  }
```

The above code will move the **.box** element 50 pixels to the right and 50 pixels down from its original position. You can try out other values such as `scale`, `rotate`, and `skew`.

# ADVANCED

<a name = "variables"></a>

### CSS Variables

CSS Variables, also known as CSS Custom Properties, allow you to define variables for CSS values. They are similar to variables in programming languages, and they provide a way to store and reuse values across multiple CSS rules.

While `making CSS variables`, you need to prefix the variable name with two dashes (**--**). The (**--**) is used to differentiate CSS variables from other CSS properties. 

While `accessing CSS variables`, you need to use the **var()** function. The **var()** function takes the name of the variable as its argument.

Here are some examples of CSS variables:

```css
:root {
  --main-color: #ff0000;
  --main-font: Arial, Helvetica, sans-serif;
}

h1 {
  color: var(--main-color);
  font-family: var(--main-font);
}
```

In the above example, a variable named **main-color** and **main-font** is defined on the :root pseudo-class, which is the highest level element in the CSS document. The **main-color** variable is used to set the color of the **h1** element, while the **main-font** variable is used to set the font of the **h1** element.

By using CSS variables, you can centralize the values that you use in multiple places, making it easier to manage and maintain your CSS. Additionally, if you need to change the value of a variable, you only need to make the change in one place, and it will be automatically updated everywhere it's used.

<a name = "preprocessors"></a>

### CSS Preprocessors ( Sass, Less, Stylus )

CSS Preprocessors are scripting languages that extend CSS and provide a more convenient and dynamic way of writing and maintaining CSS code. There are many CSS preprocessors available but the most popular ones are `Sass`, `Less`, and `Stylus`.

| Preprocessor | Description |
| --- | --- |
| [Sass](https://sass-lang.com/) | Sass is the most popular CSS preprocessor. It is a scripting language that is compiled into CSS. |
| [Less](http://lesscss.org/) | Less is a CSS preprocessor that is compiled into CSS. |
| [Stylus](http://stylus-lang.com/) | Stylus is a CSS preprocessor that is compiled into CSS. |

All three CSS preprocessors provide a way for developers to write more advanced CSS code, but each has its own unique features and syntax. When choosing a CSS preprocessor, it is important to consider the specific needs of your project, as well as your personal preference and experience with the different options.

Example of `Sass` code:

```scss
$primary-color: #4d4d4d;

body {
  background-color: $primary-color;
}

h1 {
  color: $primary-color;
}
```

Example of `Less` code:

```less
@primary-color: #4d4d4d;

body {
  background-color: @primary-color;
}

h1 {
  color: @primary-color;
}
```

Example of `Stylus` code:

```stylus
primary-color = #4d4d4d

body
  background-color: primary-color

h1
  color: primary-color
```

As you can see, in all three preprocessors, variables are used to store a value that can be reused throughout the stylesheet. This helps to keep your styles organized, maintainable and easier to update.

I have provided the official documentation links for each CSS preprocessor in the table above. You can read through the documentation to learn more about the features and syntax of each preprocessor.

<a name = "postprocessors"></a>

### CSS Postprocessors ( PostCSS )

CSS Postprocessors are tools that allow you to use CSS variables and other features that are not natively supported by CSS. These tools allow you to write code that is easier to maintain, faster to execute, and more efficient. They also provide a range of other features that can help you write better CSS, such as mixins, functions, and extendable libraries.

The most popular CSS postprocessor is `PostCSS`. PostCSS allows you to write CSS using modern syntax, and then converts it into browser-compatible code. This can be especially useful for writing code that uses features that are not yet supported by all browsers.

Here is an example of PostCSS code:

Suppose you have the following CSS code:

```css
.example{
  color: darken(#ff69b4, 20%);
  background: lighten(#ff69b4, 20%);
}
```

The above code uses the `darken()` and `lighten()` functions, which are not supported by all browsers. To convert this code into browser-compatible code, you can use PostCSS. PostCSS will convert the above code into the following code:

```css
.example{
  color: #e6007a;
  background: #ff99cc;
}
```

As you can see, PostCSS has converted the `darken()` and `lighten()` functions into browser-compatible code. This allows you to write modern CSS code that is compatible with all browsers. You can read more about PostCSS [here](https://postcss.org/).

<a name = "animationlibraries"></a>

### CSS Animation Libraries

CSS Animation Libraries are pre-made collections of animations that you can apply to elements on your website. These libraries typically include a variety of animation types and styles, making it easy to find the right animation for your project without having to write all the CSS code from scratch. Some of the most popular CSS Animation Libraries include:

| Library | Description |
| --- | --- |
| [Animate.css](https://animate.style/) | Animate.css is a library of ready-to-use, cross-browser animations for use in your web projects. |
| [Hover.css](https://ianlunn.github.io/Hover/) | Hover.css is a collection of CSS3 powered hover effects to be applied to links, buttons, logos, SVG, featured images and so on. |
| [Magic Animations](https://minimamente.com/example/magic_animations/) | Magic Animations is a library of ready-to-use, cross-browser animations for use in your web projects. |
| [Bounce.js](http://bouncejs.com/) | Bounce.js is a JavaScript library that allows you to create beautiful CSS3 powered animations. |
| [WOW.js](https://wowjs.uk/) | WOW.js is a JavaScript library that allows you to create beautiful CSS3 powered animations. |

To use a CSS Animation Library, you simply need to include the library's CSS file in your HTML document, and then add the appropriate classes to the elements that you want to animate. For example, to use the Animate.css library, you would include the following code in your HTML document:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
```

Then, to animate an element, you would add the `animate__animated` and `animate__bounce` classes to the element. For example:

```html
<h1 class="animate__animated animate__bounce">Hello World!</h1>
```

The above code will animate the `h1` element with the `bounce` animation. You can read more about the Animate.css library [here](https://animate.style/).

Similarly, to use the Hover.css library, you would include the following code in your HTML document:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/hover.css/2.3.1/css/hover-min.css"/>
```

Then, to animate an element, you would add the `hvr-bounce-to-right` class to the element. For example:

```html
<h1 class="hvr-bounce-to-right">Hello World!</h1>
```

The above code will animate the `h1` element with the `bounce-to-right` animation. You can read more about the Hover.css library [here](https://ianlunn.github.io/Hover/).

Similarly, You can use other CSS Animation Libraries by including their CSS files in your HTML document, and then adding the appropriate classes to the elements that you want to animate. Make sure to read the documentation for each library to learn more about how to use it.

<a name = "frameworks"></a>

### CSS Frameworks

CSS Frameworks are pre-made collections of CSS code that you can use to style your website. These frameworks typically include a variety of styles and components, making it easy to find the right styles and components for your project without having to write all the CSS code from scratch. Some of the most popular CSS Frameworks include:

| Framework | Description |
| --- | --- |
| [Bootstrap](https://getbootstrap.com/) | Bootstrap is a free and open-source CSS framework directed at responsive, mobile-first front-end web development. |
| [Materialize](https://materializecss.com/) | Materialize is a modern responsive CSS framework based on Material Design by Google. |
| [Bulma](https://bulma.io/) | Bulma is a free, open source CSS framework based on Flexbox and used by more than 200,000 developers. |
| [Foundation](https://get.foundation/) | Foundation is a responsive front-end framework. |
| [Semantic UI](https://semantic-ui.com/) | Semantic is a development framework that helps create beautiful, responsive layouts using human-friendly HTML. |
| [Tailwind CSS](https://tailwindcss.com/) | Tailwind CSS is a utility-first CSS framework for rapidly building custom user interfaces. |
| [UIKit](https://getuikit.com/) | UIKit is a lightweight and modular front-end framework for developing fast and powerful web interfaces. |

These are just a few of the most popular CSS Frameworks. There are many more CSS Frameworks available, you can find more lists surfing the web.

To use a CSS Framework, you simply need to include the framework's CSS file in your HTML document, and then add the appropriate classes to the elements that you want to style. For example, to use the Bootstrap framework, you would include the following code in your HTML document:

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"/>
```

Then, to style an element, you would add the `btn` and `btn-primary` classes to the element. For example:

```html
<button class="btn btn-primary">Click Me!</button>
```

The above code will style the `button` element with the Bootstrap `btn-primary` class. You can read more about the Bootstrap framework [here](https://getbootstrap.com/).

Similarly, to use the Materialize framework, you would include the following code in your HTML document:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css"/>
```

Then, to style an element, you would add the `btn` and `waves-effect` classes to the element. For example:

```html
<button class="btn waves-effect">Click Me!</button>
```

The above code will style the `button` element with the Materialize `waves-effect` class. You can read more about the Materialize framework [here](https://materializecss.com/).

Similarly, You can use other CSS Frameworks by including their CSS files in your HTML document, and then adding the appropriate classes to the elements that you want to style. Make sure to read the documentation for each framework to learn more about how to use it.

<a name="performance"></a>

### CSS Performance Optimization

CSS Performance Optimization involves making changes to your CSS code to improve its performance and speed. There are many different ways to optimize your CSS code, including:

- `Minifying your CSS` : This means removing all whitespace, comments, and unnecessary characters from your CSS code to reduce its size.
- `Using CSS Preprocessors` : CSS Preprocessors are tools that allow you to write CSS code using a different syntax, which is then compiled into regular CSS code. This allows you to use features like variables, mixins, and functions to write more efficient CSS code.
- `Using CSS Frameworks` : CSS Frameworks are pre-made collections of CSS code that you can use to style your website. These frameworks typically include a variety of styles and components, making it easy to find the right styles and components for your project without having to write all the CSS code from scratch.
- `Reducing the number of HTTP requests` : Minimizing the number of images and other external resources you use in your CSS can reduce the number of HTTP requests your website makes, which can improve its performance.
- `Using CSS sprites` : CSS sprites are a way to combine multiple images into a single file, which can reduce the number of HTTP requests your website makes and improve its performance.
- `Avoiding the use of @import` : The use of the @import rule in CSS can slow down your website, so it's best to avoid using it whenever possible.
- `Using CSS transitions and animations wisely` : Using CSS transitions and animations can add visual interest to your website, but they can also slow it down. To avoid this, be mindful of how many and how often you use them.

<a name="architecture"></a>

### CSS Architecture

CSS Architecture refers to the organization and structuring of CSS code within a website or web application. A well-designed CSS architecture can make it easier to maintain and scale the styling of a project over time, as well as improving its performance by reducing the size of stylesheets and avoiding conflicts between styles.

There are several approaches to CSS architecture, including **Object-Oriented CSS (OOCSS)**, **Block Element Modifier (BEM)**, and **Atomic CSS**. Each of these approaches has its own set of principles and practices, but they all aim to create a modular and scalable structure for CSS code.

Some key benefits of using a CSS architecture include:

- Maintaining a consistent look and feel across a project
- Making it easier to work with large, complex stylesheets
- Improving the performance of a project by reducing file size and minimizing HTTP requests
- Making it easier to maintain and update styles over time

Examples of CSS architecture practices include:

- Breaking down styles into modular components that can be reused across a project
- Using naming conventions, such as BEM, to make it clear what each class does
- Avoiding the use of overly specific selectors that can make it difficult to update styles later on
- Minifying and compressing stylesheets to reduce file size and improve performance.

<a name="testinganddebugging"></a>

### CSS Testing and Debugging

CSS Testing and Debugging refers to the process of ensuring that your CSS code is free of errors, bugs and meets the design requirements. There are a number of tools and techniques that can be used to perform CSS testing and debugging, including:

- `Browser Developer Tools` : Browser Developer Tools are built-in tools that allow you to inspect and debug the HTML and CSS code of a website. These tools can be used to identify and fix errors in your CSS code.

- `CSS Validators` : CSS Validators are online tools that check your CSS code for syntax errors and other issues. Some popular CSS validators include W3C CSS Validator, Jigsaw CSS Validator and CSS Lint.

- `CSS Unit Testing` : CSS Unit Testing involves writing automated tests to verify that your CSS styles behave as expected. There are a number of CSS unit testing frameworks available, including Jest, Mocha, and Chai.

- `Cross-Browser Testing` : Cross-browser testing involves testing your CSS styles on different web browsers to ensure compatibility. This can be done manually by testing your site on multiple browsers or automatically using tools like BrowserStack or Sauce Labs.

By following best practices for CSS testing and debugging, you can ensure that your CSS code is reliable, maintainable, and free of errors.

<a name = "conclusion"></a>

## Conclusion

CSS is the web's styling language, allowing you to customize the look and feel of your HTML content. CSS provides a range of styling options for text, color, backgrounds, borders, margins and padding, and more. By using CSS, you can create visually appealing web pages that are responsive and dynamic, adjusting their layout and appearance based on different screen sizes and devices.

This study guide has covered everything from the basics of CSS selectors and the box model, to intermediate topics like flexbox and grid, to advanced topics like preprocessors and animation libraries. With a solid understanding of CSS, you'll be able to create websites that are aesthetically pleasing and accessible, with an eye towards performance optimization and browser compatibility. CSS is an essential skill for any web developer, and we hope this study guide has given you the knowledge you need to start styling the web with confidence.

# Author

- [@amulifts](https://www.github.com/amulifts)