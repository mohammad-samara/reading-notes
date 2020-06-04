# HTML:
## Introduction:
HTML uses elements to describe the structure of pages
![image of html element](/images/class01/HTML-element.png) <br />
In HTML webpage there are several different elements. Each element has an opening tag and a closing tag. Tags acts like containers, they tell you some thing about the information that lies between their opening and closing tags.
Attributes provide additional information about the contents of an element, they appear on the opening tag of the element and are made up of two parts: a **name** and a **value**, separated by an equal sign.
Every HTML file is devided into two main parts **head** and **body**.
* body: everything inside this element is shown inside the main browser window.
* head: contains information about the page, you will find a <title> element inside the <head> element.
  * title: the content of the <title> element are either shown in the top of the browser, above where you usually type the URL of the page you want to visit, or on the tab for that page.

# Extra markup
#### how to make a comment in HTML?
if you want to add a comment to your code that will not be visible in the user's browser, you can add the text between these characters:
<!-- comment goes here -->
- id attribute
  - used to uniquely identify that element from other elements on the page (usually to style it differently than any other instance of the other element on the page using css)
  - its value should start with a letter or an underscore
- class attribute to identify several elements as being different from other elements (usually all elements with the same class attribute value will have the same style)
- Block elements: elements will always appear to start on a new line in the browser window.
   - EX: <h1>, <p>, <ul>, and <li>.
Inline element: elements will always oppear to continue on the same line as their neighboring elements.
   - EX: <a>, <b>, <em>, and <img>.
- div: the <div> element allows you to group a set of elements together in one block-level box.
- span: the <span> element acts like an inline equavilant of the <div> element.
   - usually used to contain a section of text or to contain a number of inline elements for styling it differently from the surrounding.
- iframe: an iframe is like a little window that has been cut into your page, and in that window you can see another page.
- meta: the <meta> element livew inside the <head> element and contains information about that webpage such as the describtion and keywords to make the page appears on search engines results when the users search for the mentioned keywords.
- Escape characters: allows to show some characters that are reseved by html code on the web browser window by typing a special code for each character.
  - EX: to write a left angled bracket, you can use either &lt; or &#60;

# HTML5 Layout
