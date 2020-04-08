# Code Fellows 301d61 Reading Notes

[Table of Contents](https://penjoe.github.io/301-reading-notes/)

## **Class 03**:

### **Article: Templating with Mustache**

Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. The template is HTML markup, with added templating tags that will either insert variables or run programming logic.
The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.

Mustache is a template syntax. It doesn't use any type of conditional logic, just a series of tags. mustache.js is a specific JavaScript version of the Mustache syntax format. One of the benefits of using mustache for JavaScript templating is that mustache supports multiple other languages, so it's cross-compatible when used on various servers and with various other programs. While mustache is used to write templates, it is not itself a template engine. The template is written with mustache, given input, then funneled though a templating engine where it is then compiled into a workable output. The input data used with mustache is JSON data which is used inside of the mustache template.

Official mustache.js documentation can be found [HERE](https://github.com/janl/mustache.js).

### **Article: A Complete Guide to Flexbox**

Flexbox, or the Flexbox Layout (Flexible Box) module was designed in the hopes of creating an easier, more efficient way to lay out. align and distribute space among items in a container. Flexbox was designed primarily for the purpose of dynamic web design, helping size containers and their items for various screen sizes. Flexbox layouts are best with small components of an application, unlike the Grid layout which is best for large scale layouts. 

Flexbox is more than a simple CSS property. It is a full module, with properties for both the parent container, or flex container, and and child elements, or flex items. Traditional layouts use block and inline-block flow directions. Flexbox uses its own `flex-flow directions`. Check out this diagram to see how flexbox flow works.

![flex-flow](images/flex-flow.svg)

With flexbox, items are laid out on either the `main axis` or the `cross axis`. Here is some of the layout flow terminology with flexbox: 
- main axis – The main axis of a flex container is the primary axis along which flex items are laid out. Beware, it is not necessarily horizontal; it depends on the flex-direction property (see below).
- main-start / main-end – The flex items are placed within the container starting from main-start and going to main-end.
- main size – A flex item’s width or height, whichever is in the main dimension, is the item’s main size. The flex item’s main size property is either the ‘width’ or ‘height’ property, whichever is in the main dimension.
- cross axis – The axis perpendicular to the main axis is called the cross axis. Its direction depends on the main axis direction.
- cross-start / cross-end – Flex lines are filled with items and placed into the container starting on the cross-start side of the flex container and going toward the cross-end side.
- cross size – The width or height of a flex item, whichever is in the cross dimension, is the item’s cross size. The cross size property is whichever of ‘width’ or ‘height’ that is in the cross dimension.

Once we understand the general flow of the flexbox layout, all thats left are its CSS properties. These are split between `flex container` and `flex items`.

<u>Starting with the flex container</u>, the `display` property defines the flex container, either `display: flex;` or `display: inline-flex;`. Once we define the flexbox, next is to decide the direction in which the flex items will flow. This is done with the `flex-direction` property. `Flex-property` has 4 values:
- row
- row-reverse
- column
- column-reverse

Flex items naturally all want to stay in one line. This can be changed with the `flex-wrap` property. `Flex-wrap` tells the flex items to either force into a single line or to flow into multiple lines to fit within a specific container.

The `justify-content` property will align the flex items within a flex container along its main axis. This can be used to left-align, right-align, center or space out items within the flex container. Counterpart to  the `justify-content` property is the `align-items` property. This aligns items along the cross axis. It can be used to place items at the top, bottom or center of the container or even to stretch vertically and fill the container. As a failsafe, the `safe` and `unsafe` keywords can be used when aligning flex items to prevent the content from becoming inaccessible. Similar to `align-items`, `align-content` also will align flex items along the cross axis. The difference is that `align-content` determines thr spacing between lines, whereas `align-items` determines how the items as a whole are aligned withing the flex container. 

Now that we understand the basics of the flex container's properties, we can take a look at the <u>properties used on the flex items</u>. First, the `order` property will allow you to specify which flex item appears in which order using an integer as it's value. Items are assigned an integer. The items are then put in order based on that integer, with lowest values being displayed first. If multiple items are given the same integer value, they are placed according to their source order.

Next, we have the `flex-grow` property. This property will allow the flex item to grow proportionately as needed. It accepts an integer as its value. Setting all flex items to a `flex-grow` value of 1, the space within the container will be taken up evenly. Setting one item to a value of 2 will make that item grow twice as much space as the others with a value of 1.

`Flex-shrink` allows a flex item to shrink as needed. Again, an integer is passed as its value.

The `flex-basis` property defines the default size of an element before the space is redistributed. It accepts either a length, such as 20% or 5em, or a keyword as its value. The keywords used with `flex-basis` are:
- auto: refers to the elements width or height properties
- content: sizes based on the elements content

Next, we have the `flex` property. This property is shorthand for the `flex-grow`, `flex-shrink` and `flex-basis` properties all in one. It can take up to three parameters, the last two being optional. This is the recommended method rather than setting each property individually. The `flex` property looks like this:
```
.flex-item {
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis>']
}
```
The last property used with flex items is the `align-self` property. This overrides the default alignment for specific flex items.

It's important to note that the `float`, `clear` and `vertical-align` CSS properties have no effect on flex items.

MDN documentation on the Flexible Box layout can be found [HERE](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout).