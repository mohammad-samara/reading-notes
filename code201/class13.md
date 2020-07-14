# advanced web development  
at this webpage I will tell you about what I have learnt today about **webpages**.

sometimes we need to store data for the website in the user's local storage inorder to save customized data for each user.  
***cookies*** where the first try to solve that. but they have many disadvantages:
1. it is send with every HTTP request which will slow the website
2. also cookies usually are unencrypted which could lead to security danger
3. it's size is small about 4KB which is not handy.

#### HTML5 Storage

![image of if-statement](https://techglimpse.com/wp-content/uploads/2013/04/xml-parsing-and-storing-on-localstorage1.jpg)

it is a way for webpages to store data as key/value pairs localy whithin the user's browser, and this data will be persist saved even if you close the browser and this data won't be sent to the web server.  
the entered data will be saved as a string, so when you whant to retrieve a number you need to use functions like `parseInt` or `parseFloat` to transfer the stored data into a number when retrieving.  
**how to write or update the key/value data pairs**  
first, you’ll access HTML5 Storage through the localStorage object on the global window object then use it to write or update the key/value pairs:  
there are many ways for that:
1. use `localStorage.setItem("key", value)` to store a value for key, and `ocalStorage.getItem("key")` to retrieve the value stored for the specified key.
    * calling the `setItem()` with a named key that already exists will overwrite the previous value. Calling getItem() with a non-existent key will return null
2. `localStorage["key"]` to retrieve the value stored for the specified key, and `localStorage["bar"] = value;` to store a value for key.  

to delete a value and clear the whole starage area use:  
```
interface Storage {
  removeItem(key);             // delete a value for a key
  clear();                     // clear the whole starage area
};
```   
to get the total number of values in the storage area, and to iterate through all of the keys by index:   
```
interface Storage {
  readonly attribute unsigned long length;
   key(in unsigned long index);
};
```  
for tracking changes use the **storage event** in javascript which will fires whenever the HTML5 storage area is modified.  
`window.addEventListener("storage", handle_storage, false);` the `handle_storage` callback function will be called with a **StorageEvent object** that have the following properties:  
| property | describtion |
| ---------------|--------------- |
| key | the named key that was added, removed, or modified |
| oldValue Error | the previous value (now overwritten), or null if a new item was added |
| newValue | the new value, or null if an item was removed |
| url | the page which called a method that triggered this change |  

