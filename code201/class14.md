# advanced web development  
at this webpage I will tell you about what I have learnt today about **css**

## Transforms
used to position and alter (change the appearance) elements.  
**general syntax**  
```
div {
  -webkit-transform: transformType(specific amount);
     -moz-transform: transformType(specific amount);
       -o-transform: transformType(specific amount);
          transform: transformType(specific amount);
```  
### transform Types:  
**2D Rotate**  
`transform: rotate(20deg);` the value from 0 to 360 degree, a positive value rotates element clockwise, while a negative value rotates element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically.  
**2D Scale**  
used to change the appeared size of an element. a value between 0.99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger. the default value is 1.  
`transform: scale(.75);`  
use `transform: scaleX(number);` to scale the width and use `transform: scaleY(number);`to scale the height and use `transform: scale(X-value, Y-value);` to scale both width and height each with a didderent scal value.
**2D Translate**  
works like *relative positioning*. Positive values will push an element down and to the right while negative values will pull an element up and to the left.  EX:
```
transform: translateX(-10px);             // will pull the element the left by 10px
transform: translateY(25%);               // will push an element down by 25%
transform: translate(-10px, 25%);         //works as a combination  of the two previous lines
```  
**2D Skew**  
used to deform elements on the horizontal axis, vertical axis, or both. the acceptable values unit is only in degrees.  
```
transform: skewX(5deg);             //deformed horizontally
transform: skewY(-20deg);           //deformed virtically
transform: skew(5deg, -20deg);      //deformed both horizontally and virtically
```  
positive value for x-axis will deform it horizontally counterclockwise. but a positive value for y-axis will deform it virtically on clockwise  
**Combining Transforms**  
Using multiple transform declarations will not work, the last one will be applied only.  
To combine transforms, list the transform values within the transform property one after the other without the use of commas. ex:  
```
transform: rotate(25deg) scale(.75);                //rotate and scale
transform: skew(10deg, 20deg) translateX(20px);     //skew and translateX
```  

**Transform Origin**  
it is not inside the transform property(it is a property itself)
The default point of transform(transform origin) is the center of the element. use the transform-origin property to change it. EX:  
```
transform-origin: 0 0;            // the transform origin is top left of the element
transform-origin: 100% 100%;      // the transform origin is bottom right of the element
transform-origin: top left;       // the transform origin is top left of the element
transform-origin: 20px 50px;      // the transform origin is located 20px to the right and 50px down from the top left of the element
```  
**Perspective**  
In order for three-dimensional transforms to work the elements need a perspective from which to transform.  
you may apply it on the element itself within the transform property or on it's containing element as an idividual property(not inside the transform property)  
`transform: perspective(200px) rotateX(45deg);  // uesd on the the element itself to transform it uniquely.`  
```
.group {                        //the containing element
  perspective: 200px;
}
.box {                          // an element within the containing element
  transform: rotateX(45deg);
}
```  
The perspective value can be set as none or a length measurement. the higher the value, the further away the perspective appears, and a small three-dimensional change.  
**Perspective Origin**  
 identifies the coordinates of the vanishing point of a transform  
```
perspective-origin: 0 0;
perspective-origin: 75% 75%;
perspective-origin: 20px 40px;
```  

## Transitions & Animations
### Transition
transition: alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.  
   * There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay.   
EX:   
```
.box {
  background: #2db34a;
  transition-property: background,property2 , ....;          // the property that will be changed
  transition-duration: 1s;                                   // the duration of the transition process
  transition-timing-function: linear;
}
.box:hover {                                                 // the element with the pseudo class
  background: #ff7b29;                                       // the property that changes with the new value
  property2: value;
}
```   
   * use **all** keyword instead of the property name to apply transition to all properties.   
   * transition-duration could have multiple values separated with commas for each transitioned property.  
   * The transition-timing-function property is used to set the speed in which a transition will move. it's most popular vaslues are linear, ease-in, ease-out, and ease-in-out.   
      * linear: transition moving in a constant speed from one state to another.
      * ease-in: starts slowly and speeds up throughout the transition.
      * ease-out: starts quickly and slows down throughout the transition.
      * ease-in-out: starts slowly, speeds up in the middle, then slows down again before ending.   

**transition shorthand**  
`transition: background .2s linear, border-radius 1s ease-in 1s;`   

the properties that can be transfered are:   
```
background-color,background-position,border-color,border-width,border-spacing,bottom,clip,color,crop,font-size,font-weight,height,left,letter-spacing,line-height,margin,max-height,max-width,min-height,min-width,opacity,outline-color,outline-offset,outline-width,padding,right,text-indent,text-shadow,top,vertical-align,visibility,width,word-spacing,z-index
```  

### Animation
Animation: set multiple points of transition upon different keyframes.  