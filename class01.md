# HTML:
## Introduction:
HTML uses elements to describe the structure of pages.

![image of html element](/images/class01/HTML-element.png)

In HTML webpage there are several different elements. Each element has an opening tag and a closing tag. Tags acts like containers, they tell you some thing about the information that lies between their opening and closing tags.
Attributes provide additional information about the contents of an element, they appear on the opening tag of the element and are made up of two parts: a **name** and a **value**, separated by an equal sign.
Every HTML file is devided into two main parts **head** and **body**.
* body: everything inside this element is shown inside the main browser window.
* head: contains information about the page, you will find a `<title>` element inside the `<head>` element.
  * title: the content of the `<title>` element are either shown in the top of the browser, above where you usually type the URL of the page you want to visit, or on the tab for that page.

# Extra markup
#### how to make a comment in HTML?
if you want to add a comment to your code that will not be visible in the user's browser, you can add the text between these characters:
`<!-- comment goes here -->`
- id attribute
  - used to uniquely identify that element from other elements on the page (usually to style it differently than any other instance of the other element on the page using css)
  - its value should start with a letter or an underscore
- class attribute to identify several elements as being different from other elements (usually all elements with the same class attribute value will have the same style)
- Block elements: elements will always appear to start on a new line in the browser window.
   - EX: `<h1>`, `<p>`, `<ul>`, and `<li>`.
Inline element: elements will always oppear to continue on the same line as their neighboring elements.
   - EX: `<a>`, `<b>`, `<em>`, and `<img>`.
- div: the `<div>` element allows you to group a set of elements together in one block-level box.
- span: the `<span>` element acts like an inline equavilant of the `<div>` element.
   - usually used to contain a section of text or to contain a number of inline elements for styling it differently from the surrounding.
- iframe: an iframe is like a little window that has been cut into your page, and in that window you can see another page.
- meta: the `<meta>` element livew inside the `<head>` element and contains information about that webpage such as the describtion and keywords to make the page appears on search engines results when the users search for the mentioned keywords.
- Escape characters: allows to show some characters that are reseved by html code on the web browser window by typing a special code for each character.
  - EX: to write a left angled bracket, you can use either `&lt`; or `&#60`;

# HTML5 Layout
For a long time, web page authors used `<div>` elements to group together related elements on the page, Authors used class or id attributes to indicate the role of the `<div>` element in the structure of the page.
HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them
   - EX: `<header>`, `<nav>`, `<aside>`, `<footer>`, `<article>`, `<section>`, `<hgroup>`.
Each of the previous elements acts like a block level element like the `<div>` but also describes the content inside them.
`<header>`: appears on the top of page. Also can be set for individual section or article, usually contains the title, the logo and the navigation bar.
`<footer>`: appears on the bottom of page, could be set for individual article or section, and usually contains the copyright and terms of policies.
`<nav>`: contain the major navigational blocks on the site like links to each page on the site.
`<article>`: acts as a container for any section of a page that could stand alone and potentially be syndicated.
`<aside>`:
  - When the `<aside>` element is used inside an `<article>` element, it should contain information that is related to the article but not essential to its overall meaning. For example, a pullquote or glossary.
  - When it is used outside of an `<article>` element, it acts as a container for content that is related to the entire page. Such as containing links to other sections of the site, a list of recent posts, a search box.
`<section>`: groups related content together, and typically each section would have its own heading, or used to divide an element into parts.
`<hgroup>`: to group together a set of one or more `<h1>` through `<h6>` elements so that they are treated as one single heading.
`<figure>`: used to contain any content that is referenced from the main flow of an article. But usually used to contain images or videos and add a text under them to describe them using `<figcaption>`.
`<div>`: to group a set of elements together in one block-level box, and used where there is no suitable element to group a set of elements.
Linking around block level element: to turn an entire block into a link by placing an `<a>` element around a block level element that contains child elements, usually used to redirect the user into an advertising webpages.
### How to make a better website surfing experience?
- Design your website by answering each question below to determine what needs to appear on your site:
  1. who are your visitors?
   - Every website should be designed for the target. It is therefore very important to understand who your target audience is. Like what’s their ages, countries, gender, average income, …
   - Does the website targets individuals or companies?
   - make a category of people who visit your site and collect information about them.
  2. why they visit your website?
   - Are they looking for some entertainment or they need to achieve a specific goal?
   - are they after a general information or they want them specific?
   - Do they need to be introduced to the service or product you offer?
   - Do they need to contact you?
  3. make a list of reasons why people would visit your website by collecting information.
  4. what information visitors need in order to achieve their goals quickly and effectively?
   * Make sure that all the provided information and products or services are relevant to the visitor goals
  5. determine which parts of the site will be updated frequently (like latest news)

- Site Map: a diagram of the pages that will be used to structure the site, and it will show how those pages can be grouped.
 * Organize the information on your website into sections or pages so that it would be easier for visitors to navigate and find the information they seek
- wireframes: a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require.
- Organizing and prioritizing information on a page helps users understand its importance and what order to read it in.
By making parts of the page look distinct from surrounding content, designers draw attention to (or away from) those items.
create something known as a visual hierarchy to help users focus on the key messages that will draw people's attention, and then guide them to subsequent messages.
Grouping together related content into blocks or chunks makes the page look simpler (and easier to understand).
You can differentiate between pieces of information using size, color, and style.
You can use grouping and similarity to help simplify the information you present.
- design navigation bar:
It should be concise (quick and easy to read), clear (Users should be able to predict the kind of information that they will find on the page before clicking on the link), selective (only reflect the sections or content of the site), context (lets the user know where they are in the website at that moment. Using a different color or some kind of visual marker to indicate the current page is a good way to do this), interactive, and consistent.
<hr />

# java script

![image of javascript](https://hackernoon.com/hn-images/1*bxEkHw1xewxOFjmGunb-Cw.png)

### Introduction:
java script allows you to make web pages more interactive by accessing and modifying the content and markup used in web page while it is being viewed in the browser.
- you can use java script to select any element like h1 or any elements with a specific class attribute or Id attribute
- you can use java script to add elements, attributes, text, and images to the page, or remove them.
- you can specify a set of steps (script) for the browser to follow, which allows it to access or change the content of the page.
- You can specify that a script should run when a specific event has occurred.
### The abc of programming
##### What is script in java script?
**A script is a series of instructions that a computer can follow to achieve a goal.**
* scripts are made up of instructions a computer can follow step by step.
* the browser could run different parts of the script depending on how the user interacts with the webpage.
#### How to write a script?
1. define the goal you want to achieve
2. split the goal out into a series of tasks
3. code each step
* Often scripts will need to perform different tasks in different situations. You can use flowcharts to work out how the tasks fit together. The flowcharts show the paths between each step.
#### Computers create models of the word using data
A computer has no predefined concept of what kind of real -world object each model represents so programmers create a very different kind of model using data because the data is all the computer needs in order to follow the instructions you give it to carry out its tasks.
- objects: In computer programming, each physical thing in the world can be represented as an object and each object can have its own properties, events, and methods
  - Each property has a name and a value, and each of these name/value pairs tells you something about each individual instance of the object.
  - Event: people interact with objects. These interactions can change the values of the properties in these objects. a script will state which events the programmer wants to respond to, and what part of the script should be run when each of those events occur
  - method: Methods represent things people need to do with objects. They can retrieve or update the values of an object's properties. In general, it represents a task.
All of the previous relate to each other: events can trigger methods, and methods can retrieve or update an object's properties.
#### web browsers are programs built using objects
Web browsers create similar models of the web page they are showing and of the browser window that the page is being shown in.
- window object: The browser represents each window or tab using a window object.
- document object: The current web page loaded into each window is modelled using a document object which represents an HTML page.
  - Using the document object, you can access and change what content users see on the page and respond to how they interact with it.
##### how a browser sees a webpage? how a browser interprets the HTML code and applies styling to it?
1. receive a page as an HTML code
2. create a model of the page and store it in the memory
3. use a rendering engine to show the page on screen
##### how do I write a script for a webpage?

![image of html, css , and js](https://www.10bestdesign.com/blog/content/images/2018/03/30.png)

Web developers usually talk about three languages that are used to create web pages: HTML, CSS, and JavaScript. usually kept in separate files. Each language forms a separate layer with a different purpose:
1. content layer (.html files): This is where the **content** of the page lives. The HTML gives the page structure and adds semantics.
2. presentation layer (.css files): applies **styling** to the content
3. behavior layer (.js files): adding **interactivity** and changes the page behaves
** JavaScript is written in plain text, just like HTML and CSS, so you do not need any new tools to write a script.
#### linking to a java script file from an html page
use the HTML `<script>` element to tell the browser it is coming across a script. Its src attribute whose value is the path to the script tells the browser where the JavaScript file is stored.
  - you can also put your scripts in the `<script>` element without defining any source or using an external java script file.
** scripts are usually added just before the closing `</body>` tag (this is often considered a better place to put your scripts).
##### how to use objects and methods?

![image of javascript line](/images/class01/js-line.png)

* the **document** object represents the entire web page.
* **the write()**method of the **document** allows new content to be written into the page ***where the `<script>`element sits.***
* parameter: a piece of information required by the **method** in order to work.
* member operator: used to access the members of an object (using the dot between the object name and the member you want).
  * members: **methods and properties** for a specific object.
** When the browser comes across a <script> element, it stops to load the script and then checks to see if it needs to do anything.