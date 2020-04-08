# Code Fellows 301d61 Reading Notes

[Table of Contents](https://penjoe.github.io/301-reading-notes/)

## **Class 01**:

### **Article: Shay Howe’s intro to RWD**

RWD, or Responsive web design, is increasingly more important as more and more users are on mobile phones, tablets laptops and desktops, all with their own specific display size. Unlike traditional web design practices where page layouts were made with fixed sizes, RWD allows a page to adapt in real time to the size of a device's viewport. RWD is broken down into three main categories:

- flexible layouts
- media queries
- flexible media

First let's talk about <u>Flexible Layouts</u>. CSS3 has added new relative length units specifically for sizing a webpage to meet different device viewport sizes. Flexible layouts advocate for the use of relative measurement units like `ems` and `percentages` because they can easily allow for adaptability. There is a handy formula that is used to identify good proportions for element width and heights. 
```
Flexible Grid Formula:
target / context = result
```
This simple formula takes the target width of an element and divides it by the width of it’s parent element resulting in the relative width of the target element. Applying the flexible grid formula to all parts of a grid layout will create a fully dynamic webpage that will scale to whatever size device it's being viewed on.

Next up, <u>Media Queries</u>. Media queries are used to add different styles for different browser and device circumstances. This allows for greater control when working with RWD. Media queries can be done in a few different ways:
- The `@media` rule: This is used inside an existing style sheet.
- The `@import` rule: This imports a new style sheet
- You can also link to a separate style sheet from within the HTM document.

Media queries use a type, followed by one or more expressions. Some common media types are:
- all
- screen
- print
- tv
- braille

You can also use a logical operator withing the media query, allowing for powerful expressions and greater control. Once media query syntax and logical operators are understood, you can use media features to exert control over the layout and responsiveness of a web page. Media features are things like `height` and `width` and can have modifiers like `min` and `max`. Here's an example of all of these concepts brought together:
```
@media all and (min-width: 320px) and (max-width: 780px) {style}
```
The above media query selects the media type of `all` and selects any viewport width between 320px and 780 px and applies a specific style to anything meeting those criteria. There are many more media features that can be used to customize your responsive layout.

A popular, and increasingly more important, technique with media queries is called *mobile first*. This approach to RWD prioritizes smaller viewport first, like those found on smart phones. Since trends are quickly pointing toward mobile being the primary medium for viewing web pages, catering to mobile first is a great way to keep traffic to your web page. Media queries can also be used to limit certain CSS3 styles from loading on smaller, less powerful devices to keep pages from loading too slowly.

To help account for the growing array of different viewport sizes, specifically mobile viewports, Apple invented the `viewport` meta tag. This can be used with its own modifiers to more easily determine viewport/device height and width. A few of the primary modifiers for the `viewport` meta tag are:
- Height and width
- Scale
- Resolution

The last main area of RWD is <u>Flexible Media</u>. As you change the size of a viewport, it is important that the size of media changes along with the size of various HTML elements. A simple way to add scalability to media, such as images and video, is by using the `max-width` property. By using `max-width: 100%;` on an image, it will always scale to size of its parent container.

### **Article: All About Floats**

`Float` is a CSS positioning property. Using float will tell an HTML element to 'float' to the left or right of the page, allowing text to wrap around it. Elements tha are floated stay within the overall flow of the page. Aside from floating images for text wrapping, you can also float HTML container elements such as `sections` or `asides`. While there are better tools out there for overall layout of a page, float is still very useful, especially in small settings such as placing an image in a box and having text placed next to it, as you might do with an author's bio picture and description. As opposed to absolute positioning, floating elements allows for dynamic movement when a page is resized.

When an element is floated, elements that follow will naturally want to move adjacent to the floated element, as is the purpose of float. That's why it is important to use the `clear` property on elements that come after floated elements so that the float is 'cleared' away after it is used. Clear is used after the floated elements in the container but before the close of the container.