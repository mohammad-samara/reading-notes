# advanced web development  
at this webpage I will tell you about what I have learnt today about **html** and **javascript**.
## html
### Tables
tables allow us to organise and display comlex data to make it easier to understand them.
#### how to create table:
```
<table>
  <tr>
    <td>15</td>
    <td>15</td>
    <td>30</td>
  </tr>
  <tr>
    <td>45</td>
    <td>60</td>
    <td>45</td>
  </tr>
</table>
```
where `<tr>` represents table row ,withinit you see multiple of `<td>` (table data) which is a **cell** in the row.
there is also `<th>` which works just like the `<td>` but the text within it would be bold and centerd to represent a **table heading**.
  * you can use `scope` attribute with a value of `row` or `col` to indicate whether the heading is for a row or a column.

#### spanning columns:
to let a cell take a space of multiple cells use `colspan` or `rowspan` attributes with a numeric value to indicate how many columns or rows the cell should run across.
#### long tables
in long tables you will need to organise your table row and put them in different tags as the following:  
* `<thead>` : put the first row of the table here to indicate that it is a heading of the table.
  * it will be under-lined.
* `<tbody>` : all the rows bettween the first and the last row sits here.
* `<tfoot>`: the last row sits here.
  * it will be over-lined.

## JavaScript
### Objects:
#### creating object using consructor notation:
```
var objectName = new Object();
    property1.objectName = property1-value;
    property2.objectName = property2-value;
    property3.objectName = property3-value;
    methodName1.objectName = function() {
        code-statements of the function
    };
```
* the first line creates an empty objects then we add properties and methods to the object.
* to update properties value `objectName.propertyKey = theNewValue` or `objectName['propertyKey']=theNewValue`
* to delete property use `delete objectName.propertyKey;` or you can set the value to an empty string.  
* to create multiple objects use an object constructor wich is a function work as a template for objects.  
EX:  
```
function FunctionName(property1,property2,...){
    this.property1=property1;
    this.property2=property2;
    ...etc
}
```
then to create new objects using that function do as following:  
`var object1Name = new functionName(property1Value,property2Value,...);`
#### `this` keyword
used inside functions that are in object to indicate the ObjectName that it is inside like `this.name` refers to the containig object name property (not for another object).
#### array vs objects
arrays are special type of objects since they have related data pairs(index and the corresponding data);  
* arrays can store a series of objects ,and objects can have an array as a value for a property.  

### Built-in objects
it objects come by browser's inorder to get helpful informations without any need to create new objects and methods to do a task. and they are devided into a 3 main types:
1. browser object model: contain objects that represnts the current browser tab. and each object have important properties.
2. global javascript objects: represent things that javascript need to create a model of. like time&date.
3. document object model: creates a representation of the current page(an object for each element and attributes and text).

#### browser object model properties and methods
|property|describtion|\*\*\*\*\*|method|describtion|
|--------|-----------|----------|------|-----------|
|window . innerHeight|Height of browser's window|\ \ \ \ |window. alert()|Creates dialog box with message|
|window.innerWidth|Width of browser's window|\ \ \ \ |window.print()|Tells browser that user wants to print contents of current page|
|window.location|Current URL of window object|\ \ \ \ |window.open ()|Opens new browser window with URL specified as parameter|
|window.screen.width|the width of the device screen|  |   |
|window.screen.height|the height of the device screen|  |   |
|window.pageXOffset|Distance document has been scrolled horizontally|  |   |
|window. pageYOffset|Distance document has been scrolled vertica lly|  |   |
|window.screenX|X-coordinate of pointer|  |   |
|window.screenY|y-coordinate of pointer|  |   |
||||


#### document object model properties and methods:
|property|describtion|\*\*\*\*\*|method|describtion|
|--------|-----------|----------|------|-----------|
|document.title|Title of current document| |document.write()|Writes text to document|
|document .URL|Returns string containing URL of current document| |document . getElementByld()|Returns element matching the specific id|
|document.lastModified|Date on which document was last modified| |document.createElement()|Creates new element|
|document.domain|Returns domain of current document| |document.createTextNode()|Creates new text node|
| | | |document. querySe1ectorA11 ()|Returns list of elements that match a CSS selector|
| | | | | |

#### global javascript objects
devided into 4 sub-types:  
1. string object: has properties and methods to modify texts.
2. number object: has properties and methods to work with numbers.
3. math object: has properties and methods that works as a math functions.
4. date & time objects: has properties and methods to set and retrieve the time and date.