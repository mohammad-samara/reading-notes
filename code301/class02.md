## jQuery

![image of jQuery](https://cdn.educba.com/academy/wp-content/uploads/2019/05/what-is-jquery-1.png)

it is javaScript library used to do common tasks in javascript without the need for a callback code for each browser.  
it needs less code lines to perform the same task in javascript  
sellecting elements by CSS-style selector which is easier than using the DOM queries.  

![image of jQuery](https://mobilunity.com/wp-content/uploads/2018/05/jquery-vs-javascript.jpg)


#### **how to use it?**
first include it in the html file by either using CDN or by installing the file and link it as you do to the .js files.
second you need to select element/s by using `jQuery()` with the CSS selector as parameter
   - you can also use `$()` as a shorthand for the `jQuery()`.

third work on the selected element by adding the period sympol followed by the method as the following:  
`$('css-selector').method();` , remember to insert parameter for the method when needed.
   * there is no need to loop over the selected elements since method will affect all of them in the jQuery.

#### get and set data
- if the selection have more than one element and you used a method to get it's information (EX: `.html()`) it will give you the information for the first matching element only
- if the selection have more than one element and you used a method to update content(like the `.html()`) it will update the content of all matching elements.

### jQuery objects
when you select element/s using jQuery, it stores a reference to the corresponding nodes in the DOM and you can store this references in ***jQuery objects*** inorder to wasly access them when you need them more than once.  
   - EX: `$jQueryObjectName = $(css-selector);`

#### chaining
The process of placing several methods in the same selector by using dot notation between the methods.
   * the methods that retrieve information from the DOM cannot be chained.  
EX: `$( 'l i [i d!="one"] ') . hide() .delay(SOO) . fadeln(1400);`

### checking if the page finished loading
use the following syntax to let your code runs after the page finishes loading:
```
$(document).ready(function() {
    // your script goes here
});
```
or use the following shorthand:
```
$(function() {
    // your script goes here
});
```
### getting content
`.html()` method retrieves only the HTML inside the first element in the matched set, along with any of its descendants.  
`.text()` method returns the content from every element in the jQuery selection, along with the text from any descendants.
### updating content
`.html()` gives every element in the matched set the same new content.The new content may include HTML markup.  
`.text()` gives every element in the matched set the same new text content. Any markup would be shown as text.  
`.replaceWith()` replaces every element in a matched set with new content. It also returns the replaced elements.  
`. remove()` removes all of the elements in the matched set.  
### insering elements
first create the new element by assigning it's html code to a jQuery variable. EX:`var $newltem = $('<li class="new">item</ li>');`.  
then add the new element to the page using one of the following methods:  
`.before()` inserts content before the selected element/s.  
`.after()` inserts content after the selected element/s.  
`.prepend()` inserts content inside the selected element/s, after the opening tag.  
`.append()` inserts content inside the selected element/s, before the closing tag.  
### working on attributes
`.attr()` get or set a specified attribute and its value. to get the value of an attribute.  
`.removeAttr()` removes a specified attribute (and its value).  
`.addClass()` adds a new value to the existing value of the class attribute.
   * It does not overwrite existing values.  

`.removeClass()` removes a value from the class attribute, without deleting the other values within the class attribute.  
### working on css properties
use the `.css ()` method to retrieve and set the values of CSS properties.  
to set one css property use `$('cssSelector').css('cssProperty', 'propertyNewValue');` but to set multiple css properties use:  
```
$('cssSelector').css({
'cssProperty1': 'value1',
'cssProperty2': 'value2'
});
```  
### looping over selections
use `.each()` method to perform statements on every item in the selection, you place these statements in a function and use that function as a parameter for the `.each()`. and you can refer to the selection with `this` or `$(this)` in the statements.  
### adding event
use the following syntax to add an event on an element: `$(css-selector).on('eventName',theFunction())`  
