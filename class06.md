# advanced web development  

**DOM**(document object module): a set of rules implemented by internet browsers to specify how an html page loads and how javascript access and edit the html page content.  

**dom tree**: when the browser load the page it creates a model of that page and store it in the memory. it consists of nodes, each represents an hatm tag or an attribute, and it links between them as the family tree.  

![image of DOM tree](/images/class06/DOM-tree.png)

ther are 4 types of nodes:  
1. document node : represents the entire page.
2. element node: represents an element
3. attribute node: represents an attribute of an element.
4. text node: represents the text within an element(between it's openning & closing tags).
* each node is an object, and cript access and do changes to the DOM tree not the original HTML file, and all changes will be shown on the browser.

to update element you need first to **access the node** that represents it:  
A. select an individual element node: use `getElementById()` which uses the id value of the element to access it's node, or `querySelector()` which uses a css selector to return the first matching element.  
B. select multiple elements: use the `getElementsByClassName()` to select all elements with the mentioned class value, or `getElementsByTagName()` to select all elements with the mentioned tag name, or `querySelectorAll()` which uses a css selector to select all matching elements.  
C. traversing between element nodes: `parentNode` to select the parent element, `previousSibling`/`nextSibling` to select the previous or next sibling, `firstChild`/`lastChild` to select the first or last child of the current element.  

work with the selected element/s:  
A. acceess/update **text** nodes: first access the element node which contains the desired text, then use `firstChild` to get the text node, use `nodeValue` to get the text.  
  * `nodeValue` lets you access or update contents of a text node.
 
B. work with **HTML content**: use `innerHTML` to access child elements and text content(access the htlm code between the opening & closing tags of a specific element), `textContent` access to the text content only.
  * you can create new nodes, add nodes to a tree, and remove node using `create Element()`,`createTextNode()`,`appendChild()`/`removeChild()`

C. access or update **attribute** values: use `className`/`id` to update the value of the class and id attributes. in general `attributeName` to update the value of attributeName.
  * `hasAttribute()` checks if the mentioned attribute exist, `getAttribute()` gets an attribute value, `setAttribute()` updates the attribute value, `removeAttribute()` removes the mentioned attribute.

DOM queries: methods that finds elements in the DOM tree, may rturn one element or a NodeList(collection of nodes) depending on the used method.
  * when you need to work on an element multiple times, use a variable to store the result of this query.
  * when storing element in variable you actually storing the location of the element node within the DOM tree in the variable.(like linking the element with the variable)
  * when a DOM query return a nodeList, you can select one element from a nodeList using `item()` method with the ***index number*** which is given for each element node within the nodeList(starts from 0) or `varName[index-number];` where varName is the name of the variable used to store the element node.
  * to apply the same set of statements for all node loops(especially for loop) to repeat the same statements for each node within the nodeList.
    *EX:
    ```
    var redParag = document.querySelectorAll('p.red-background')
    for (var i = 0; i < redParag.length; i++) {
    redParag[i].className = 'blue-background';
    }
    ```