# advanced web development  
at this webpage I will tell you about what I have learnt today about **html**, **css**, and **javascript**.
## html
### links
##### site links:
![image of site links](http://www.webfuel.ca/wp-content/uploads/WebFuel-Google-Canada-Sitelinks.jpg)
links are a clickable elements that takes you to another page or to another part of the same page.
to create a link we use the `<a>` tag as the following example:
`<a href="http://www.google.com/">Google</a>` where the content of href is the ***URL*** of the targeted webpage, and the text between the two `<a>`and`</a>` tag will appear on your website as a clickable link with defult blue color and underlined.
* if your link redirect the user to another website use the *absolute URL* in href, and if it is redirects to another page of your website use the *relative URL*.
  - absolute URL: the **full web address** for the site (starts with `http://` then the domain then the path of the page)
  - relative URL: the **path** of the webpage (doesn't start with `http://`)
##### Email links:
links that when user click on them it opens his email program filling the "mail to" section with a specic email you choose as the following `<a href="mailto:a.b@gmail.com/">mail me</a>` where the content of the href is `"mailto:"`next to it place your email.
##### how to let the link opens in a window
add the attribute target to the opening `<a>`tag and assign the value "_blank" ti it as:  
`<a href="http://www.google.com/" target="_blank">Google</a>`
##### link to a specific part of the same part
use the `#` symbol followed by the ***id*** of the targeted part as: `<a href="#intro">Introduction</a>` which will directs you to the element with id attribute with the value intro.

## CSS
### layout :
![image of html boxes](https://complete-concrete-concise.com/wp-content/uploads/2018/04/17-css-flow.png)
each html element sets inside a block that could be a *block-level box* or an *inline box*
  - block-level box: starts on a new line.
    - EX: `<div>`, `<li>`, `<p>`,`<ul>`
  - inline box: could be placed at a line with another element side by side or flows betwwen surrounding text
    - EX: `<img>`, `<i>`, `<input>`
* Containing element: a block-level element that contains another block-level element.
  - EX: `<div><h1>Intro</h1><p>text1</p></div>` the `<div>` elemnt is sayed to be a containing element.
#### controlling the position of elements:
to change the element position use one of the following positioning schemes:

1. normal flow (`static`): each block-level element will start on a new line(won't share any lines with another element)
  - syntax: `position: static;`
2. relative positioning (`relative`): moves an element with respect to it's position at normal flow
  - syntax:  
  ```position: relative;
  top: 20px;
  left: 50px;```
3. absolute positioning (`absolute`):specify where the element should appear in relation to its containing element.
  - syntax:  
  ```position: absolute;
  top: 20px;
  left: 500px;```
4. fixed positioning (`fixed`):specify where the element should appear in relation to the browser window, so you will see the element even if you scroll down like it is pinned on the screen.
  - syntax:  
  ```position: fixed;
  top: 20px;
  left: 500px;```

##### overlapping elements
to determine which element should be shown of two elements overlap use the z-index property with a numeric value, so that the element with the highest z-index value will be shown over the other element
  - syntax: `z-index: 10;`
##### floating elements
to moves an element to Far right or far left of the Containing element use `float` property with left or right as a value.
  - anything else inside the same Containing element will flow around the floated element
  - syntax: `float: right;`
* you can create a multi-coloum layout by using `<div>` element to represent each column then specify it's width and margin(not necessary) and set it to `float: left`

#### screens
* screens with different sizes shows different amount of informations, so make sure that your design is flexible over different screen sizes
* not all the screens have the same resolution wich affects the size of text, so take it in consideration.
  - resolution: number of dots a screen shows per inch.
* *above the fold*:The area of the page that users would see without scrolling,so use it wisely to let the user know what the site is about.

#### fixed width latout vs liquid layouts
![image of fixed layout vs liquid layout](https://image.slidesharecdn.com/beautifulwebdesign-150328144915-conversion-gate01/95/beautiful-web-design-21-638.jpg?cb=1427554523)
##### fixed width latout
* a fixed width layout will remain it's size when the users change the browser window size.
* measurements are specified using pixels
* it will give you better control over the appearance, position,and sizes of elements.
* in small screens the user will see small amount of the information on the page without scrolling.In higher resolution screens the page will look smaller.
##### liquid layouts
* A liquid-width layout expands and contracts to fill the available space.
* are based on percentages of the current browser window's size
* it is harder to control the appearance, position,and sizes of elements.
![image of liquid layout](https://www.markupbox.com/blog/wp-content/uploads/2015/10/fluid_website_layout.jpg)

## javascript
### functions,methods, and objects
* we use them to organise our code, to shorten the code, and make it easier to follow.
Function: a series of statements that have been grouped together in one code block in order to perform a specific task.
  * the function won't be executed unless it have been called.
- To create a function, you give it a name and then write the statements needed to achieve its task inside the *curly bracec*, this is known as **function declaration**.
  * you can call the same function as many times as you want.

![image of function declaration](https://raddevon.com/wp-content/uploads/2019/07/function-declaration-diagram-1024x282.png)

- Having declared the function, you can excute all of the of the statements between its curly bracec by typing the function name followed by paretheses, this is known as **calling the function**
  * if the function requires specific information(values or variables) to work, just put them inside the paretheses when calling the function with a comma between them.
`functionName();`
## getting a single value out of a function
some functions return information to the code that called them, by using the **return** keyword inside the function.
  * to return more than one value use arrays inside the function.

If you put a function where the interpreter would expect to see an expression, then it is treated as an expression, and it is known as a ***function expression***
