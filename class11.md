# advanced web development  
at this webpage I will tell you about what I have learnt today about **css**, and **websites**.
## CSS
### Images
**Controlling Image sizes**
use `width` and `height` properties to specify the dimensions of an image using css.(Specifying image sizes helps pages to load more smoothly). EX:
```
img.large {
width: 500px;
height: 500px;}
```
**Aligning Images**
use the **float** property to align images to left or right.
EX: `img.align-left { float: left;}`
**Centering Images**
to center an image, you should sprcify it `display` property with the value `block` to make the image a blocklevel.
then use the `margin` property of the image and set the left and right margins values to `auto`. or On the containing element, use the text-align property with a value of center. EX:
```
img.align-center {
display: block;
margin: 0px auto;}
```
**Background image**
to set a background to any html element use the `background-image` property. EX:
`p { background-image: url("path");}`
  * a background image will repeat to fill the entire box.

**repeating image**
you can controll the repetition of a background image using `background-repeat` property with one of the following values:
1. repeat: (the default) The background image is repeated both horizontally and vertically.
2. repeat-x: The image is repeated only horizontally
3. repeat-y: The image is repeated only vertically.
4. no-repeat: the background won't repreat and will take a place at the top left corner of the box.  

**controlling image poition when scrolling**
use the `background-attachment` property with one of the following values:
1. fixed: when the user scrolls the background image stays.
2. scroll: when the user scrolls the background image moves.

**background position**
When the image's `background-repeat` is set to `no-repeat` , you can use the `background-position` property to specify where in the box the background image should be placed. by specifying ywo values to it ,the first indicate the x-axis, the second indicate the y-axis:
  * the first value could be `left` or `center` or `right` or a number in pixels or percent.
  * the second value could be `top` or `center` or `bottom` or a number in pixels or percent.  

## practical information
### search engine optimization (SEO)
rules to follow inorder for the website to be shown near the top results in a search engine website (like google).
  * On-page techniques: include the keywords that people are likely to enter into a search engine if they wanted to find a topic that your site cover it in in the text and HTML code of the site.
    * where to put keywords:
    1. in the title tag
    2. in the URL (related to the website files name)
    3. headings
    4. text: any text in the `<body>`, and try to repeat the keyword 2~3 times
    5. text between `<a>` tags that links between the website pages and sections
    6. `alt` text of images: the search engines uses the content of `alt` attribute of the image to understand the content of the image.
    7. page describtion in the `<meta>` which is in the `<head>`
  * Off-page techniques: you rank will increase with the number of the **content related websites** that links to your site. consedering the words in the link(between the `<a>` tags)

### analytics
to collect informations about the users who visited your website like: how they found it, what they were looking at and at what point they left the website, and the visitors number. you can use **Google Analutics** free service for that.
this service will give you a ***tracking code*** that you will put on each page of the website just before the `</head>` tag.
### Domain Names and Hosting
In order to put your site on the web you will need a *domain name* and *web hosting*.
**domain name**: it is the website web adress. you get it by a web sites that allow you to register domain names. usually you will have to pay an annual fee to keep that domain name.
**web hosting**: you need to upload your site into a web server which is a special computers that are constatnly connected to the internet. there are a lot of companies that host websites on their servers.
  * To transfer your code and files from your computer to your hosting company, you use a File Transfer Protocol(FTP) programs

## html
### video and audio
use `<video>` and `<audio>` elements to embed video and audio into web pages.
  * note that this elements come with their own APIs for controlling playback, seeking, etc.
  * use the `controls` attribute enables the default set of playback controls.
  * you can remove the `controls` attribute and make your own controls using html,css,and JavaScript.
```
<video controls>
  <source src="path with extention like .mp4" type="video/mp4">
  <source src="path with extention like .webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>  \\fall back
</video>
```
