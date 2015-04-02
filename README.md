# flipclock
a flipclock like widget for displaying images

Definitely a work in progress ;)

Q: How to use it?

A:

You're going to need some img tags with images in them, and a place to inject the clock...

For example:

  Include the includes:
```html
	<link rel="stylesheet" type="text/css" href="styles.css">
	<script src="jquery.js"></script>
	<script src="flipclock.class.js"></script>
```
  Set stuff up:
```html
    <img id="cat" src="cat.jpg"/>
    <img id="cat2" src="cat2.jpg"/>
    <img id="cat3" src="cat3.jpg"/>

    <div id="clocks">
```
  Create the clock and inject it
```javascript
    //the ids of the image tags
    var images = ["cat", "cat2", "cat3"];
    flipClockName = "flipClock0";     //any old name will do
    var fc = new flipClock(images) ;  //flipclock object
    fc.fillDiv();                     //generates divs
    fc.div.id = flipClockName;        //name the div
    $("#clocks").append(fc.div);      //inject the clock
    fc.setUpInitial();                //set up the flipping action
```

And that's it
