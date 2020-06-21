# advanced web development  
at this webpage I will tell you about what I have learnt today about **Charts**, and **JavaScript**.

### canvas element
- the `<canvas>` element has only two attributes, width and height. you can add id attribute to it.
  - ex: `<canvas id="tutorial" width="150" height="150"></canvas>`
- any content between the `<canvas>`&`</canvas>` tags will consider to be a fall back in case the browser does not support the `<canvas>` element, which means it won't appear if your browser support the `<canvas>`.
- To display something, a script first needs to access the rendering context and draw on it. using the following code:
  ```
  function draw() {
  var canvas = document.getElementById('tutorial');
  var ctx = canvas.getContext('2d'); }
  ```
- it has a method called `getContext()`, used to obtain the rendering context and its drawing functions and this method have one parameter which is *the type of context* mostly `2d` for 2D graphics.
- the origin point for the coordinates of this element is the top-left corner

to draw a `rectangular` put the following in the `draw()` function below the rendering context line:
```
fillRect(x, y, width, height)            //Draws a filled rectangle.
strokeRect(x, y, width, height)          //Draws a rectangular outline.
clearRect(x, y, width, height)           //Clears the specified rectangular area, making it fully transparent.
```
drawing **paths**:
paths are a group of points connected together with lines or curve lines using code statements. use the foolowing to draw a triangle:  
```
ctx.beginPath();             //start the path
    ctx.moveTo(75, 50);     // the first point coordinates moveTo(x,y)
    ctx.lineTo(100, 75);    // draw a line from the previous point the the point with the specified coordinates lineTo(x,y)
    ctx.lineTo(100, 25);
    ctx.fill();            // it will close the path and fill the area between the drawn shape
```
if you don't want to fill the shape replace the last line with `closepath` to close the path without filling the shape.  
use the `stroke()` method to draw the shape by stroking its outline. (draws the border of the shape) it comes after `closepath`  

to draw **arcs use the following**:  
`arc(x, y, radius, startAngle, endAngle, anticlockwise)`
Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).  
or use `arcTo(x1, y1, x2, y2, radius)`  
Draws an arc with the given control points and radius, connected to the previous point by a straight line.  



--------------------------------------------------------------------------
### charts:
The concept of a library is that it allows you to borrow code from one file and use its functions, objects, methods, and properties in another script. Once you have included the script in your page, you can use their functions.
one of those library is **Chart.js** which is a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page.
#### how to use chart.js
first, you need to downloaded and link it to your html page like you link any jacascript file.
second, create a `canvas` element in the html page, so you can draw the chart inside it
`<canvas id="" width="" height=""></canvas>`  
**to draw a line chart add the foolowing code line:**  
```
<script>
    var anyNameData = {
	labels : ["label1","label2","label3","label4","label5","label6"],  // labels for the base of the chart
	datasets : [
		  {
			fillColor : "rgba(172,194,132,0.4)",    //for styling purpose
			strokeColor : "#ACC26D",                //for styling purpose
			pointColor : "#fff",                    //for styling purpose
			pointStrokeColor : "#9DB86D",           //for styling purpose
			data : [203,156,99,251,305,247]       // datasets to describe values on the chart (labl's y-coordinates)
		  }
	  ]
   }
    var anyName = document.getElementById('canvas element id').getContext('2d');
    new Chart(canvas element id).Line(anyNameData);  // for drawing a line chart
</script>
```  
**to draw a pie chart add the foolowing code line instead:**  
```
<script>
    var pieData = [
	  {
		value: 20,                    // value1 (represent the percentage of the area of the pie chart)
		color:"#878BB6"               // color1 (the color of that area)
	  },
	  {
		value : 40,                   // value2
		color : "#4ACAB4"             //color2
	  },
	  {
		value : 10,                   // value3
		color : "#FF8153"             // color3
	  },
	  {
		value : 30,                   // value4
		color : "#FFEA88"             // color4
	  }
    ];
    var pieOptions = {
	segmentShowStroke : false,        // remove the stroke from the segments
	animateScale : true               // animate the scale of the pie so that it zooms out from nothing
    }
    var anyName = document.getElementById('canvas element id').getContext('2d');
    new Chart(canvas element id)..Pie(pieData, pieOptions);        // for drawing a pie chart
</script>
```  
**to draw a bar chart add the foolowing code line instead:**  
```
<script>
    var anyNameData = {
	labels : ["label1","label2","label3","label4","label5","label6"],  // labels for the base of the chart
	datasets : [
	 	    {
			  fillColor : "#48A497",                      //for styling purpose
			  strokeColor : "#48A4D1",                    //for styling purpose
			  data : [456,479,324,569,702,600]            //dataset to describe values on the chart(each value for a label)
		    },
		    {
			  fillColor : "rgba(73,188,170,0.4)",         //for styling purpose
			  strokeColor : "rgba(72,174,209,0.4)",       //for styling purpose
			  data : [364,504,605,400,345,320]            //dataset to describe values on the chart(each value for a label)
		    }

	    ]
    }
    var anyName = document.getElementById('canvas element id').getContext('2d');
    new Chart(canvas element id).Bar(anyNameData);  // for drawing a bar chart
</script>
```  