# how to add markup to the text that appears on your pages
### Structural markup:

#### HEADINGS:
heading are used usually as a title of paragraphs or as a subheading for another heading.
* HTML has six "levels" of headings:from `<h1>` to `<h6>`, where `<h1>` is used for main headings. 
* The font size of the text of an `<h1>` element is the largest, and in `<h6>` element is the smallest.
#### Paragraphs
To create a paragraph, surround the words that make up the paragraph with an opening `<p>` tag and closing `</p>` tag.
- the paragraph could also contain images beside text.
- each paragraph will start on a new line
#### Bold & Italic
By enclosing words in the tags `<b>` and `</b>` we can make characters appear bold.
- EX: `<b>hello</b>` will give you the next result: <b>hello</b>
By enclosing words in the tags `<i>` and `</i>` we can make characters appear italic.
- EX: `<i>hello</i>` will give you the next result: <i>hello</i>
#### Superscript & Subscript
The `<sup>` element is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power such as `2<sup>2</sup>` will give you: ( 2<sup>2</sup> )
The `<sub>` element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as `H<sub>2</sub>O` will give you: ( H<sub>2</sub>O )
#### White Space
it is used to make code easier to read, but toy should notice that when the browser come across two or more spaces next to each other, it only displays one space.
#### Line Breaks & Horizontal Rules
to add a line break inside the middle of a paragraph you can use the line break tag `<br />`.
To create a horizontal line to break betwean sections use the `<hr />` tag.
EX:
end of section 1
<hr />

### Visual Editors
HTML editors such as Dreamweaver usually have two views of the page you are creating: a **visual editor** and a **code view**.
Visual editors often resemble word processors which allows you to create an html webpage without coding
how to use visual editors:
- Headings are created by highlighting text then using a drop-down box to select a heading.
- Bold and italic text are created by highlighting some text and pressing a b or i button.
- New paragraphs are created using the return or the enter key.
- Line breaks are created by pressing the shift key and the return key at the same time.
- Horizontal rules are created using a button with a straight line on it.
Code views:
show you the code created by the visual editor so you can manually edit it, or so you can just enter new code yourself.

### Semantic Markup
text elements that add extra information to the pages without affecting the structure of the webpage
The use of the `<strong>` element indicates that its content has strong importance.
  - the contents of a `<strong>` element will be in bold.
The `<em>` element indicates emphasis that subtly changes the meaning of a sentence.
  - the contents of a `<em>` element will be in italic.
The `<blockquote>` element is used for longer quotes that take up an entire paragraph.
  - Browsers tend to indent the contents of the `<blockquote>` element.
The `<q>` element is used for shorter quotes that sit within a paragraph
  - the content in the `<q>` element will be shown inside a double quotation marks, and doesn't start on a new line.
If you use an *abbreviation* or an *acronym*, then the `<abbr>` element can be used. A title attribute on the opening tag is used to specify the full term.
  - the content of the title attribute will be shown when the user hover over the `<abbr>` content.
When you are referencing a piece of work such as a book, film or research paper, the `<cite>` element can be used to indicate where the citation is from.
  - the contents of a `<cite>` element will be in italic.
The `<dfn>` element is used to indicate the defining instance of a new term.
The `<address>` element is used to contain contact details for the author of the page.

#### Changes to Content
The `<ins>` element can be used to show content that has been inserted into a document, while the `<del>` element can show text that has been deleted from it.
  - The content of a `<ins>` element is usually underlined, while the content of a `<del>` element usually has a line through it.
The `<s>` element indicates something that is no longer accurate or relevant (but that should not be deleted).
  - the content of an `<s>` element will usually be displayed with a line through the center.

# Introduction to CSS

CSS allows you to create rules that specify how the content of an element should appear. For example, you can specify that the background of the page is cream, all paragraphs should appear in gray using the Arial typeface, or that all level one headings should be in a blue, italic, Times typeface.

- CSS allows you to create rules that control the way that each individual box (and the contents of that box) is presented.
- css associates style rules with html elements. the rules govern how the content of specified elements should be displayed.


a **css cod** contains of two parts: **selectors** & **declaration**

![image of css-rule](/images/class02/css-rule.png)

  * the selector indicates which element the rule applies to.
  * the declaration indicates how element should be styled.
  * the declaration contains off two parts separated by a clone(:) sympol

     1. property: affects how elements are displayed, and indicates the aspects of the element you want to change, such as color, font-size, background-color, width, height,...
     2. value: specifies the setting you want to use for the choosen property.

most important **selectors types** :
1. type selector : matches element names
  - ex: `h1, h2{}` targets h1 and h2
2. class selector: Matches an element whose class attribute has a value that matches the one specified after the dot symbol
  - ex: `.firstList{}` targets any element whose class attribute has a value of "firstList"
  - ex: `p.firstList{}` targets any `<p>` element whose class attribute has a value of "firstList"
3. id selector: Matches an element whose id attribute has a value that matches the one specified after hash symbol
  - ex: `#intro{}` Targets the element whose id attribute has a value of "intro"
4.  descendent selector: Matches an element that is a descendent of another specified element
  - ex: `p a{}` Targets any `<a>` elements that sit inside a `<p>` element
# how to apply styles from css to html:

- external file: there will be an external file for css rules with the extension .css that is separated from the html file and you can link it with the html file by typing the next code at the < head > in the html file:
`<link rel="stylesheet" href= "the path of the css file">`
  - it is the best way to place a css code because all of your webpages can share the same style sheet so there is no need to edit every page to change the styling only edit the style sheet, also it makes the pages load faster.
- style tag at the < head > in the html file like this:
`<style>css codes</style>`
- inline styling: using style attribute in side the opening tag of an element.
![image of css effects](/images/class02/css-effect.jpg)

# basic javascript instructions:
**statement**: an individual instruction or step in the script. and each statement ends with a simicolon.

![image of js-statement](/images/class02/js-statement.png)

##### Comments: to write a comment in javascript use the following :
  - for multi-line comment: `/* your comment goes here */`
  - for single-line comment: `// yor comment `

**variable** : a place in memory used to temporary store information in order to run the script
##### declaring a variable:
`var variableName;` such as `var userName;` where the variable name is "userName"
  * the variable name must begin with a letter, dollar sign ($),or an underscore (_)
##### assighn a value to the variable
`variableName = variableValue;` such as `userName=sam` where "sam" is the variable value
  * you need to declare the variable before assighning any value to it
  * the variable value could be from any type of data(numbers, characters,symbols,or a mix of them)
##### change the value of a variable:
just re-assighn the new value to the variable
EX: `var x=5;
x=8;`
#### data types:
1. numeric: handles numbers
2. string: consists of letters and other characters.
  * when assinghning a value to a string make sure it is inside a quotation symbol
3. boolean: have one of two va lues: true or false.
* there are others data type such as array, null,object, and undefined

##### Array: 
a special type of variable. It doesn't just store one value; it stores a list of values
* you can declare it as the following:
`var arrayName = [value1, value2, value3,...];` where the values could be from any type,but remember to put any string between quotations.
* every value in the array is given a number called ***index*** which is used to access specific items in the array, where **the first index values start at 0 (not 1)**
  * ex: `var colors = ['white', 'black','red']; colors[2]= green;` here we have changed the third value of the array from 'red' to 'green'

### Expresions:
An expression evaluates into (results in) a single value. Broadly speaking there are two types of expressions:
1. EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE.
   * EX: var color = 'beige';
2. EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE
    EX: var area = 3 * 2;


### OPERATORS:
Expressions rely on things called operators; they allow programmers to create a single value from one or more values.
- ASSIGNMENT OPERATORS: Assign a value to a variable (**=**)
- ARITHMETIC OPERATORS: Perform basic math (*,-,/,++,--,%)
- STRING OPERATORS: Combine two strings (**+**)
- COMPARISON OPERATORS: Compare two values and return true or false
- LOGICAL OPERATORS: Combine expressions and return true or false


-------------------------------------------------------------------------

#### Comparison operators:
evaluating conditions

- you can evaluate a situation by comparing one value in the script to what you expect it might be. the result will be a Boolean: *true or false*

* (==) : is equal to
   * compares between two values(numbers, strings, or booleans) to see if they are the same
* (===) : strict equal to
   * compares to values to check that both the data type and value are the same
* (!=) : is not equal to
   * compares between two values(numbers, strings, or booleans) to see if they are not the same
* (!==) : strict not equal to
   * compares to values to check that both the data type or the value are not the same
* (>) : greater than
   * checks if the number on the left is greater than the number on the right
* (<) : less than
   * checks if the number on the left is less than the number on the right
* (>=) greater than or equal to
   * checks if the number on the left is greater than or equal to the number on the right
* (<=) : less than or equal to
   * checks if the number on the left is less than or equal to the number on the right

------------------------------------------
#### Logical Operators

Comparison operators usually return single values of **true** or **false**, logical operators allow you to compare the results of more than one comparison operator.

![image of logical operator sentence](/images/class02/logical.png)



1. logical and (&&) : if both expressions evaluate to true then the expression returns true. if just one of these returns false, then the expression will return false.
2. logical or (`||`) : if either expression evaluates to true, then the expression returns true. if both false, then the expression will return false.
3. logical not (!) : reverses the state of an expression. if it was false (without the ! before it) it would return true. if the statement was true, it would return false>

![image of T-F table](https://1.bp.blogspot.com/-E3z93RXYCGc/XfXd0T8x3FI/AAAAAAAAE04/zNAwwEov8cw-t353RBQ4rAq59znfY0C5QCLcBGAsYHQ/s1600/Screenshot%2B%2528455%2529.png)

----------------------------------------------------------------------------------------------------------------

## if statement 

the if statement checks a condition. if it returns true, any statement in the subsequent code block are executed.

![image of if-statement](/images/class02/if-statement.png)

## if...else statement

the if...else statement checks a condition. if it returns true, the first code block is executed, otherwise the second code block is executed.

![image of if-else-statement](/images/class02/if-else-statement.png)