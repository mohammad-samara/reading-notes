# advanced web development  
at this webpage I will tell you about what I have learnt today about **css**  
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
  ```
  position: relative;
  top: 20px;
  left: 50px;
  ```
3. absolute positioning (`absolute`):specify where the element should appear in relation to its containing element.
  - syntax:  
  ```
  position: absolute;
  top: 20px;
  left: 500px;
  ```
4. fixed positioning (`fixed`):specify where the element should appear in relation to the browser window, so you will see the element even if you scroll down like it is pinned on the screen.
  - syntax:  
  ```
  position: fixed;
  top: 20px;
  left: 500px;
  ```

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

#### layout grid
A grid is the division of a layout with vertical and/or horizontal guidelines to incorporate margins, spaces and columns in order to position items on the page. which creates continuty between different pages that use the same grid system.  
* there are many latout grids for each desired webpage width, the most comon is the 960 pixel grid.
#### css framework
A CSS framework is a library making it easier to create webpage design using the css language. Most of these frameworks contain at least a grid.
* they provide the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages...  
