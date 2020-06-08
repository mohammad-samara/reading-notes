# advanced web development  
at this webpage I will tell you about what I have learnt today about **html**, **css**, and **javascript**.
## html
### lists:
HTML provides us with three different types:  
1. Ordered lists : a list where each item in the list is numbered.
  - in order to create an ordered list use `<ol> </ol>` tag and to add items to it use `<li> </li>` tag inside the `<ol>` tag for each list item
2. Unordered lists : lists that begin with a bullet point (rather than characters that indicate order).
  - in order to create an unordered list use `<ul> </ul>` tag and to add items to it use `<li> </li>` tag inside the `<ul>` tag for each list item
3. Definition lists : made up of a set of terms along with the definitions for each of those terms.
  - The definition list is created with the `<dl>` element. Inside the `<dl>` element you will usually see pairs of `<dt>` and `<dd>` elements. where `<dt>` used to contain the term being defined, and `<dd>` is used to contain the definition.
- nested lists: You can put a second list inside an `<li>` element to create a sublist or nested list.
## css
### boxes:
CSS treats each HTML element as if it lives in its own box, and you will learn how to set several properties that affect the appearance of these boxes.

#### box dimentions
* To set your own dimensions for a box you can use the "height" and "width" properties, the dimentions values could be in pixels,as a pesentage (of the size of the browser window or of the size of the containing box),and in "ems"(which is relative to the size of the text within that box)
* you can specify a smallest or the largest size a box can be displayed at the browser window by using `min-width` and `max-width` properties to specify the minimum and the maximum width for a box, and use `min-height` and `max-height` properties to specify the minimum and the maximum height for a box.
* The ***overflow*** property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values:
1. **hidden**: hides any extra content that does not fit in the box.
2. **scroll**: adds a scrollbar to the box so that users can scroll to see the missing content.

#### box border
Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.
##### border width
* use `border-width` property to control the width(thickness) of the border, it's value could be specified in pixels or using one of the following values:(*thin*, *medium*, *thick*). 
You can also specify different widths for the four border values in one property,like this:`border-width: 2px 1px 1px 2px;`
where The values here appear in clockwise order: top, right, bottom, left.
* You can control the style of a border using the ***border-style property***. This property can take the following values:
value          | effect on border
---------------|---------------
solid          | a single solid line
dotted         | a series of square dots
dashed         | a series of short lines
double         | two solid lines
groove         | appears to be carved into the page
ridge          | appears to stick out from the page
inset          | appears embedded into the page
outset         | looks like it is coming out of the screen
hidden or none | no border is shown |
<!-- 
1. **solid**: a single solid line.
2. **dotted**: a series of square dots.
3. **dashed**: a series of short lines.
4. **double**: two solid lines.
5. **groove**: appears to be carved into the page.
6. **ridge**: appears to stick out from the page.
7. **inset**: appears embedded into the page.
8. **outset**: looks like it is coming out of the screen.
9. **hidden** or **none**: no border is shown. -->
* You can specify the color of a border using either RGB values, hex codes or CSS color names by using `border-color` property.
It is also possible to use a shorthand to control all four border colors in the one property, like this:
`border-color: #bbbbaa #111111 #ee3e80 #0088dd;`

###### shorthand
The border property allows you to specify the width, style and color of a border in one property (and the values should be coded in that specific order).
- EX: `border: 3px dotted #0088dd;`

#### padding
The ***padding*** property allows you to specify how much space should appear between the content of an element and its border.
 * EX: `padding: 10px 5px 3px 1px;` , the padding values could also be specified as percentage or ems.

#### margin
The margin property controls the gap between boxes. Its value is commonly given in pixels, although you may also use percentages or ems.
EX1: `margin: 1px 2px 3px 4px;`, the values here appear in clockwise order: top, right, bottom, left.
EX2: `margin: 10px 20px;`, the first value specifies left and right margins,while the second value specifies top and bottom margins.

#### centering content
If you want to center a box on the page (or center it inside the element that it sits in), you can **set the left-margin and right-margin to _auto_**, but first you should specify the width of the box (otherwise it will take up the full width of the page).

#### change Inline/Block display behavior
The ***display*** property allows you to turn an inline element into a block-level element or vice versa.This property can take the following values:

value | effect on border
-----------|-----------
inline | causes a block-level element to act like an inline element
block | causes an inline element to act like a block-level element
inline-block | causes a block-level element to flow like an inline element, while retaining other features of a block-level element
none | This hides an element from the page sithout leaving an empty space in it's place |

  - EX: `display: inline;`

#### hiding boxes
The ***visibility*** property allows you to hide boxes from users but It leaves a space where the element would have been. This property can take two values:
1. **hidden**: This hides the element.
2. **visible**: This shows the element.

#### box shadow
The ***box-shadow*** property allows you to add a drop shadow around a box.
EX1: `box-shadow: 5px 5px 5px 5px #777777;` the first value indicates how far to the left or right the shadow should fall, where the second value indicates the distance to the top or bottom that the shadow should fall. The third value is optional and specifies the amount of blur that should be applied to the drop shadow (If omitted, the shadow is a solid line like a border). the fourth value if used, a positive value will cause the shadow to expand in all directions, and a negative value will make it contract.. The fifth value is the color of the drop shadow.
EX2: `box-shadow: inset 0 0 10px #777777;` The inset keyword can also be used before these values to create an inner-shadow.

#### round corners
using a property called **_border-radius_**. The value indicates the size of the radius in pixels.
EX: `border-radius: 10px;`

## javascript
#### switch statement
A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.

![image of switch](/images/class03/switch-work.png)

ex: the following example compares the value of the variable `level` with each case:
```
var level = 'two';
switch (level) {
case 'One ':
title= 'Level 1 ' ;
break;
case 'Two':
tit1e = ' Level 2 ' ;
break;
case ' Three' :
title = 'Level 3' ;
break ;
default :
title= 'Test';
break;
```
#### type coercion and weak type
* JavaScript can convert data types behind the scenes to complete an operation. This is known as **type coercion**.
* JavaScript is said to use **weak typing** because the **data type for a value can change**.
  * Some other languages require that you specify what data type each variable will be. They are said to use **strong typing**.
#### **truthy** and **falsy** values
* every value in JavaScript can be treated as if it were true or false.
* Falsy values are treated as if they are fa 1 se. The table to the left shows a hi ghScore variable with a series of va lues, all of which are falsy.

![image of switch](/images/class03/falsy-table.png)

* Truthy values are treated as if they are true. Almost everything that is not in the falsy table can be treated as if it were true.
* the presence of an object or an array is usually considered truthy, too. This is commonly used when checking for the presence of an element in a page.
```
if (document.getElementByid('header')) {
// Found: do something
} else {
// Not found: do something else
}
```
## loops 

loops check a condition. if it returns true, a code block will run, then the condition will be checked again and if it still return true, the block code will run again. it repeats until the condition returns false.

1. **for**: if you need to run code a specific number of times, use a *for* loop, in a *for loop*, the condition is usually a **counter** which is used to tell how many times the loop should run.

![image of logical operator sentence](/images/class03/for-statement.png)

   * a ***for* loop uses a *counter* as a condition**
   this instructs the code to run a specific number of times
   **the condition in the *for loop* is made up of three statements:**
     - initializing : create a variable and set it to 0 (or any value you want) (var i =0;)
     - condition : the loop should continue to run untill the counter reaches a specific number. EX: (i <10 ;)
     - update : every time the loop run the statement in the curly braces, it adds one (or any value you choose) to the counter



2. **while** : if you don't know how many times the code should run, you can use a *while* loop, and the condition can be something other than a counter, and the code will continue to loop for as long as the condition is true.

![image of logical operator sentence](/images/class03/While-Loop.png)

3. **do while** : very similar to *while loop*, but has one key difference: it will always run the statements inside the curly braces at least once, even if the condition evaluates to false.

![image of logical operator sentence](/images/class03/do-while-Loop.png)

you can find more about logical loops at the click me below:

[click me](https://www.freecodecamp.org/news/the-complete-guide-to-loops-in-javascript-f5e242921d8c/)