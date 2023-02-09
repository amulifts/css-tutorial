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
        * [CSS Positioning](#positioning)
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
        * [CSS Animation Libraries ( Animate.css, Bounce.js, Hover.css )](#animationlibraries)
        * [CSS Frameworks ( Bootstrap, Foundation )](#frameworks)
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

CSS selectors are used to target HTML elements in the DOM(Document Object Model). DOM is a tree-like structure that represents the HTML elements in a web page. They are used to select the elements you want to style. Selector can be based on element type (e.g. `h1`, `p`, `div`), class (e.g. `.class-name`), ID (e.g. `#id-name`), attribute (e.g. `[attribute-name]`), pseudo-class (e.g. `:hover`), pseudo-element (e.g. `::first-line`), or descendant (e.g. `div p`).

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

/* Selects all elements with attribute "attribute-name" */
[attribute-name] {
    color: red;
}

/* Selects all elements with attribute "attribute-name" that has value "attribute-value" */
[attribute-name="attribute-value"] {
    color: red;
}

/* Selects all elements with pseudo-class "hover" */
:hover {
    color: red;
}

/* Selects all elements with pseudo-element "first-line" */
::first-line {
    color: red;
}

/* Selects all elements with class name "class-name" that are descendants of elements with class name "parent-class-name" */
.parent-class-name .class-name {
    color: red;
}
```

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

<a name="positioning"></a>

### CSS Positioning

The CSS position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky). It is a very important property in CSS as it is used to control the layout of multiple elements on a web page.

The position property can have one of the following values:

- **static** - This is the default value. An element with position: static; is not positioned in any special way; it is always positioned according to the normal flow of the page.

- **relative** - An element with position: relative; is positioned relative to its normal position. Setting the top, right, bottom, and left properties of a relatively positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

- **fixed** - An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. A fixed element does not leave a gap in the page where it would normally have been located.

- **absolute** - An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed). However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

- **sticky** - An element with position: sticky; is positioned based on the user's scroll position. A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).

Here are some examples of CSS positioning:

```css
div {
    position: static;
}
```

You can try out other values of position property.

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

The CSS clear property specifies on which sides of an element floating elements are not allowed to float. The clear property can have one of the following values:

- **left** - This specifies that no floating element should be to the left of the element.

- **right** - This specifies that no floating element should be to the right of the element.

- **both** - This specifies that no floating element should be to the left or to the right of the element.

- **none** - This specifies that floating elements can be on either side of the element.

- **inherit** - This specifies that the clear value should be inherited from the element's parent.







<a name = "conclusion"></a>

## Conclusion

CSS is the web's styling language, allowing you to customize the look and feel of your HTML content. CSS provides a range of styling options for text, color, backgrounds, borders, margins and padding, and more. By using CSS, you can create visually appealing web pages that are responsive and dynamic, adjusting their layout and appearance based on different screen sizes and devices.

This study guide has covered everything from the basics of CSS selectors and the box model, to intermediate topics like flexbox and grid, to advanced topics like preprocessors and animation libraries. With a solid understanding of CSS, you'll be able to create websites that are aesthetically pleasing and accessible, with an eye towards performance optimization and browser compatibility. CSS is an essential skill for any web developer, and we hope this study guide has given you the knowledge you need to start styling the web with confidence.

# Author

- [@amulifts](https://www.github.com/amulifts)