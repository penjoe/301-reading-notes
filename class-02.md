# Code Fellows 301d61 Reading Notes

[Table of Contents](https://penjoe.github.io/301-reading-notes/)

## **Class 02**:

### **JavaScript and jQuery book by Jon Duckett: Chapter 7**

jQuery offers a simple way to achieve a variety of common JavaScript (JS) tasks quickly and consistently, across all major browsers and without any fallback code needed. jQuery is a lightweight, "write less, do more", JS library. Some of the areas where jQuery is especially handy are selecting HTML elements and manipulating the DOM, handle events and perform tasks such as animating elements, updating the DOM and looping through a set of elements. Where traditional 'vanilla' JS would sometimes take several lines of code, jQuery can sometimes perform these tasks in one or two lines. This versatility is easier to read, takes less time for the developer and has better built in functionality than using pure JS.

To access jQuery, first you need to add the jQuery library to your HTML. This can be done similarly as you would with a local JS file by adding it to the bottom of the HTML document. You can also load jQuery from a CDN. When using a CDN to load jQuery, it's a good idea to also have a local version handy in case the CDN is not available.

So what is jQuery and how do you use it? `$()` is the most common way to start a jquery command. Say we want to find a specific HTML element. We could use `$('li.hot')` to select any `<li>` with the class name `hot`. Once we have selected an element, you can use jQuery to do something to that element. For example:
```
$('li.hot').addClass('complete');
```
This grabs the `<li>` elements with the class `hot` and adds the class `complete` to them. There are many different jQuery selectors that can be used to easily grab any element needed. Many of these selectors are CSS-style, things like `.class`, `#id`, `parent>child` and any others. After using a selector to find an element, jQuery has a large number of built in methods used for manipulating those elements. To name a few:

- `.html` and `.text` both are used to get and/or change content of the HTML.
- `.before` and `.after` both append to the DOM.
- `.attr` and `.removeAttr` both add and remove, respectively, attributes to an HTML element

There are many more methods jQuery has to offer that can easily help you accomplish tasks in JS. One of the most basic and a very important one is the jQuery 
```
$(document).ready(function() {
  //JS script
});
``` 
function. This runs to make sure that the browser page has loaded the elements needed for the jQuery to run. Since this is such a basic jQuery function, it is often shortened to 
```
$(function() {
  //JS script
});
```
Running this at the beginning of a jQuery script will ensure that the page loads properly before the script is executed.

jQuery can also be used to directly add, change or remove CSS properties and rules using the `.css()` method. So for example, if you wanted to add CSS to a specific element, you could use something like this:
```
$('#random-div').css('background-color', 'blue');
```
Multiple CSS properties can be added using object literal notation:
```
$('#random-div').css({
  'background-color': 'blue'),
  'font-size': '16px',
  'display': 'inline-block'
});
```
When working with multiple elements returned with jQuery, using the `.each()` method gives you loop-like functionality. While in the `.each()` method, you can use the `this` keyword to refer to the current element.
Here's an example:
```
$(function() {
  $('li').each(function() {
    var ids = this.id;
    $(this).append(' <span class="order">' + ids + '</span>');
  });
});
```
This example will take all of the `<li>` elements and add a `<span>` element to them that has the class of `order` and the content of the added element will be its `id attribute` which was obtained and stored in the `var ids` variable.

Another things that jQuery is good at is handling events. Using the `.on()` method, jQuery can easily handle adding events and handlers to elements. This method takes two parameters. The first is the event you want to respond to. The second is the code that needs to run when that event occurs. There are several jQuery events that a built in such as:
- input
- keydown
- click
- hover
- submit

and many others. Here is a simple example of how jQuery handles events:
```
$('li').on('click', function() {
  $(this).addClass('complete');
});
```
This will add a class of `complete` to the `<li>` element that is clicked on.

jQuery can also easily add effects and CSS animations to enhance the look and feel of your web page. Here are a few effects:
- `.show()` displays the selected elements.
- `.hide()` hides the selected elements.
- `.fadeIn()` fades in the selected elements, making them opaque.
- `.fadeOut()` fades out the selected elements, making them transparent.
- `.slideUp()`  shows selected elements with a sliding motion.
- `.slideDown()` hides selected elements with a sliding motion.

Similar to effetcs, jQuery can add animations by manipulating CSS properties. Check out the official documentation [HERE](https://api.jquery.com/animate/) to learn more about the jQuery `.animate()` method! There are tons of more features that jQuery has to offer. It's an extremely efficient tool to add to your JavaScript arsenal that will allow you to "write less, do more".

The official jQuery site with full documentation on all of it's functionality can be found [HERE](https://jquery.com/).