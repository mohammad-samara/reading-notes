# CSS Grid Layout
## Grid

![CSS Grid Layout](https://miro.medium.com/max/860/1*FifZUGz97Onmb7RUOairbg.png)

it is a method that could offer space distribution between items and powerful alignment capabilities. used to easly create a layout for the page.  
you can use it by setting some css properties to the container element and it's child element. 

### Properties for the Parent (Grid Container)

**display**: An HTML element becomes a grid container when its display property is set to grid or inline-grid.

**grid-template-columns**:defines the number of columns in your grid layout, and it can define the width of each column. The value is a space-separated-list, where each value defines the width of the respective column.

**grid-template-rows**: defines the number of columns in your grid layout,and the height of each row. The value is a space-separated-list, where each value defines the height of the respective row.
  * the values could be in px ar auto or in ***fr*** which is a fraction of the remaining free space.

**grid-template-areas**: defines a grid template by giving each cell a name.the value is multiple content between quotations each quotation represents a row and holds a values.The value is a space-separated-list, where each value is a name you choose(called grid-area) ,or a period( . ) which represents an empty cell ,or "none" which means that no grid area is defined.  
cause the cells with the same name will combine to produce a big cell.  
then you can assign element for each cell by selecting that element in css and give it `grid-area: the-name-of-the-cell/s;`  
ex:  
```
.container {
  display: grid;
  grid-template-columns: 50px 50px 50px 50px;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
}
.item-a {
  grid-area: header;
}
.item-b {
  grid-area: main;
}
.item-c {
  grid-area: sidebar;
}
.item-d {
  grid-area: footer;
}
```  

![grid-template-areas](data:image/jpeg;base64,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)

**grid-template**: A shorthand for setting grid-template-rows, grid-template-columns, and grid-template-areas.

**column-gap**: Specifies the size of the gap between the columns (does not include the space between edges and grid items)  
**row-gap**: Specifies the size of the gap between the rows (does not include the space between edges and grid items)  
ex:  
```
.container {
  grid-template-columns: 100px 50px 100px;
  grid-template-rows: 80px auto 80px; 
  column-gap: 10px;
  row-gap: 15px;
}
```  

**gap**: A shorthand for setting column-gap and row-gap. where it have two values space-separated, the first for row-gap.  
ex:`gap: 15px 10px;`.  

**justify-items**: Aligns grid items along the inline (row/x-axis) axis within the cell. can have the following values:  
1. **start**:aligns(stack) the items at the beginning of the cell
2. **end**:aligns(stack) the items at the end of the cell
3. **center**:aligns(stack) the items at the center of the cell
4. **stretch**: fills the whole width of the cell (this is the default)  

**align-items**: to align the items along the axis that is perpendicular to the main-axis(y-axis) within the cells. it can have the following values:  
1. **start**:aligns(stack) the items at the top of the cell
2. **end**:aligns(stack) the items at the bottom of the cell
3. **center**:aligns(stack) the items at the center of the cell
4. **stretch**: fills the whole height of the cell (this is the default)  

**justify-content**: aligns the grid along the inline (row/x-axis) axis, when the total size of your grid might be less than the size of its grid container because of using px units. can have the following values:  
1. **start**: displays(stacks) the grid at the start of the container,(to the left-side).
2. **end**: displays(stacks) the grid at the end of the container,(to the right-side).
3. **center**: displays(stacks) the grid at the middle of the container.(centers it horizontally)
4. **space-between**: places an even amount of space between each grid item, with no space at the far ends
5. **space-around**: places an even amount of space between each grid item, with half-sized spaces on the far ends
6. **stretch**: stretches the grid to take up the remaining space (this is default).
7. **space-evenly**: places an even amount of space between each grid item, including the far ends.  

**align-content**:  aligns the grid along the block (column/y-axis) axis ,when the total size of your grid might be less than the size of its grid container because of using px units. can have the following values: 
1. **flex-start**: displays(stacks) the grid rows at the start of the container,(usually at the top of the container).
2. **flex-end**: displays(stacks) the grid rows at the end of the container,(usually at the bottom of the container).
3. **center**: displays(stacks) the grid rows at the middle of the container.(centerde virtecally)
4. **space-between**: displays the grid rows with equal space between them. but there is no space before the first grid row nor after the last one.
5. **space-around**: grid rows are distributed so that the spacing between any two rows (and the space to the edges) is equal.
6. **stretch**: stretches the grid rows to take up the remaining space
7. **space-evenly**: grid rows are evenly distributed with equal space around them.