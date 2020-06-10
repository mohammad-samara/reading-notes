# advanced web development  
at this webpage I will tell you about what I have learnt today about **html**, **css**, and **javascript**.
## html
### Images

* if you want to add an image to your site make in consederation that it should be relevant to the other content of the web page.
* it is better to keep all images in a separate folder to keep your site files organised.
* for adding image use the following syntax: 
`<img scr="path or URL of image" alt="image describtion"> title="additional information" />`
  * any text inside the `alt` attribute will be shown only if there is an error in loading the image.
  * use the attributes `width` and `height` inside the `<img>` tag to specify the dimensions of the image.
* note that `<img>` is an **inline element** which means that If the `<img>` element is surrounded by a text or other inline elements it will flow around the image.
#### alighning image:
in HTML use the attribute `align` with a value of `<left>`or`<right>` inside the `<img>` tag to controll how the text flow around the image, and you can align an image vertically to controll the vertical position of the first line of the paragraph that the image is nested inside it, by using `align` with one of the next values: `top`,`bottom`,`middle`.
* it is unpreferable to use the `alighn` attribute in html to alighn the image,but instead use the ***flow*** property in **css** to achieve that.
#### pro-advice:
* save the image at resolution of 72 pixels per inch wich most computer screen use, because a higher resolution image will slow down the page loading.
* make sure that the image has the same dimension as it is specified in the code, otherwise it could be stretched or become unclear with low quality.
* if you want to cut out(crop) some parts of the image ,do it in a way that doesn't affect the main content of the image.
* smaller images means less loading time.
* use images with one of the following formats: JPEG or GIF or PNG which are supported by most browsers.
* add a describtion below the image by using `<figure>`and `<figcaption>`as the following:
  ```
  <figure>
  <img scr="path or url" alt="describe the image">
  <br />
  <figcaption>the capyion(additional information) of the image</figcaption>
  </figure>
  ```
## css
### colors
* The **color property** allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:
  - rgb values: These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)
  - hex codes: These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80
  ![image of hex codes](https://htmlcolors.com/img/hex-color.jpg)
  - color names: There are 147 predefined color names that are recognized by browsers. For example: DarkCyan
EX: `p{color: DarkCyan;}` or `p{color: #ee3e80;}` or `p{color: rgb(100.100.90);}`.
**Background Color**: You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color names. use `background-color` property for that.
EX: `body{background-color: #ee3e80}` and `h2{color: red}`

#### Contrast: 
make sure that there is enough contrast between background and the foreground(text) colors, so that the text will be easy to read.
  * when there is a low contrast between foreground and background colors,the text will be harder to read.
#### opacity
you can sepicify the opacity of an element and any element nested inside it by using `opacity` property with a value from 0.0 to 1.0, or you can use the ***rpga*** property to specify colors just like using **rgb** but you add a fourth value called *alpha value* represents the opacity wihch have a value from 0.0 to 1.0
#### hsl & hsla
a new way to describe colors using hue, saturation and lightness valuess
EX: `body{background-color: hsla(0,100%,100%,.5)}` where the first value represents the **HUE**, the second represents the **saturation**, the third represents the **lightness**, and the last value represents the **opacity**.
### Text
#### specifying typefaces

![image of typefaces](https://3v6x691yvn532gp2411ezrib-wpengine.netdna-ssl.com/wp-content/uploads/2018/12/A.GoodTypeface.png)

Typeface: the overall design of lettering, the design can include the design can include variations, such as extra bold, bold, regular, light, italic, condensed, extended.
* **font-family**: use this property with a value of the typeface to specify the typeface to be used for texts.
EX: `h2{font-family: Arial, Verdana, sans-serif;}`
  - as you see there are more than one typeface as a value of the font-family, if the user browser don't have the first typeface then the second will be applied, and if the browser doesn't support the second it will moves to the third and so on.
  * **font-size**: use this property to specify the size of the font using *pixels* or *percentage* or *ems*.
  EX: `h1{font-size: 12px;}` and `h2{font-size: 150%;}`
* `@font-face`: to allow the user to use a font even if it isn't installed on his computer
EX: `@font-face{font-family: 'the name of the font'; scr: url('path or url');}`

#### Bold
use the `font-weight` property to create a bold text, this property could have one of the following values:  
1. **normal**: text will appear at a normal weight.
2. **bold**: the text will appear bold

#### italic
use the `font-style` property to create an italic text, this property could have one of the following values:  
1. **normal**: text will appear at a normal style
2. **italic**: text will appear italic
3. **oblique**: text will appear oblique

#### uppercase & lowercase
use the `text-transform` property to change the case of letters(capital or small letters), this property could have one of the following values:  
1. uppercase: text will appear uppercase.
2. lowercase: text will appear lowercase.
3. capitalize: the first letter of each word appear capitalized.

#### underline &strike
use the `text-transform` property with one of the following values:  
1. **none**: removes any decoration
2. **underline**: adds a line underneath the text.
3. **overline**: adds a line over the top of the text.
4. **line-through**: adds a line through words.

#### leading:
it is the vertical space between text lines. you can specify it using the `line-height` property
  * note that Increasing the line-height makes the vertical gap between lines of text larger.and make paragraphs easier to read.
#### letter & word spacing:
* use the `letter-spacing` property to specify the empty space between each letter. the value is only in **em** .
* use the `word-spacing` property to specify the gap between each word. the value is only in **em**.

#### alignment
use the `text-align` property with one of the following values:  
1. **left**: aligns text to the left.
2. **right**: aligns text to the right.
3. **center**: centers the text.
4. **justify**: every line in a paragraph, except the last line, should be set to take up the full width of the containing box.

#### indent text
The `text-indent` property allows you to indent the first line of text within an element. it's value usually specified in pixels or ems.

#### drop shadow
use the `text-shadow` property to create a dorp shadow which is a dark version of the word just behind it and slightly offset.
EX:`p{text-shadow: 2px 2px 7px #111111;}` The first value indicates the offset to the left or right the shadow
should fall, the second value indicates the offset to the top or bottom the shadow should fall, The third value is optional and specifies the amount of blur,the fourth value for the color.

#### styling links:
use the next pseudo classes for styling the links:
1. `:link`: This allows you to set styles for links that have not yet been visited.
2. `:visited`: This allows you to set styles for links that have been clicked on.
EX: `a:link{color: green;}`

#### responding to user
There are three pseudo-classes that allow you to change the appearance of elements when a user is interacting with them:
1. `:hover`: this is applied when a user hovers over an element.
2. `:active:`: This is applied when an element is being activated by a user; for example, when a button is being pressed or a link being clicked.
3. `:focus:`: focus occurs when a browser discovers that you are ready to interact with an element.