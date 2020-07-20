# css layout
## Flexbox

![flexbox](https://i1.wp.com/www.cssscript.com/wp-content/uploads/2018/12/Tiny-Flexbox-Grid-Layout-In-Pure-CSS-infinity-css-grid.png?fit=565%2C376&ssl=1)

it is a method that could offer space distribution between items and powerful alignment capabilities. used to easly create a layout for the page.  
you can use it by setting some css properties to the container element and it's child element.  
### Properties for the Parent element(container)

**display**: set it's value to ***flex***. EX: `containerElement {display: flex;}`  

**flex-direction**: defines in which direction the container wants to stack the flex items. can have the following values:
1. **column**: stacks the flex items vertically (from top to bottom).
2. **column-reverse**: stacks the flex items vertically (but from bottom to top).
3. **row**: stacks the flex items horizontally (from left to right).
4. **row-reverse**: stacks the flex items horizontally (but from right to left).

**wrap**: by default all flex items will be on one line but you can let them wrap onto multiple lines. it can have the following values:
1. **nowrap**: all flex items will be on one line and their width will decrease in a smaller window or screen.
2. **wrap**: the flex items will wrap onto multiple lines when there is not enough space in the line. and the flex items will maintain their width even if you changed the window dimentions it will just create a new line.
3. **wrap-reverse**: flex items will wrap onto multiple lines in a reversed order.

**flex-flow**: a shorthand property for setting both the `flex-direction` and `flex-wrap` properties.  

**justify-content**: to align the flex items along the main axis that have been set using *flex-direction*.it allows you to controll 

![justify-content](https://user.oc-static.com/upload/2018/06/14/15289918266602_2.png)

the spacing and position of the flex items. it can have the following values:
1. **flex-start**: aligns the flex items at the beginning of the container.(default)
2. **flex-end**: aligns the flex items at the end of the container.
3. **center**: aligns the flex items at the center of the container.
4. **space-between**:  displays the flex items with space between the lines, but there is no space before the first flex item nor after the last one.
5. **space-around**: it will be like the remaining space will be destributed as margins for all flex items or you can say that items are evenly distributed in the line with equal space around them.
6. **space-evenly**: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

**align-items**: to align the flex items along the axis that is perpendicular to the main-axis. it can have the following values:
1. **stretch**: the flex items to fill the container (this is default).
2. **flex-start**: aligns flex items at the start of the cross axis(usually at the top of the container).
3. **flex-end**: aligns flex items at the end of the cross axis(usually at the bottom of the container).
4. **center**: aligns the flex items in the middle of the cross-axis (usually centers the flex items vertically in the container).
5. **baseline**: aligns the flex items such as their baselines aligns.  

![align-items](https://flexbox.tech-academy.co.uk/files/2017/10/align-items.png)

**align-content**: to align the flex lines. it can have the following values:
1. **flex-start**: displays(stacks) the flex lines at the start of the container,(usually at the top of the container).
2. **flex-end**: displays(stacks) the flex lines at the end of the container,(usually at the bottom of the container).
3. **center**: displays(stacks) the flex lines at the middle of the container.
4. **space-between**: displays the flex lines with equal space between them. but there is no space before the first flex line nor after the last one.
5. **space-around**: flex lines are distributed so that the spacing between any two lines (and the space to the edges) is equal.
6. **stretch**: stretches the flex lines to take up the remaining space (this is default).
7. **space-evenly**: items are evenly distributed with equal space around them.

![align-content](https://miro.medium.com/max/1205/1*VmfjtWiRcM1u1MlaPhka0g.gif)

### Properties for the Children (flex items)

**order**: specifies the order of the flex items.

**flex-grow**: specifies how much a flex item will grow(get bigger) relative to the rest of the flex items.(0 by default)
  * If all items have flex-grow set to 1, the remaining space in the container will be distributed equally to all children.

**flex-shrink**: specifies how much a flex item will shrink(reduce width when reducing the window width) relative to the rest of the flex items.(1 by default)
  * if an item have a flex-shrink value = 0 it will not shrink and will maintain it's width.  

**flex-basis**: specifies the initial length of a flex item before the remaining space is distributed.

**flex**: a shorthand property for the flex-grow, flex-shrink, and flex-basis properties.

**align-self**: specifies the alignment for the selected item inside the flexible container.and its overrides the default alignment set by the container's **align-items** property.