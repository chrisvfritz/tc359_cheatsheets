Many simple animations that may have onced required jQuery can now be achieved through css animations with CSS3. Let's take a look at some simple examples:

So let's start with a div we can target:
``` html
<!DOCTYPE html>
<html>
<head>
    <style type="text/css">
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```

We'll give it a height, width, and color so we can see the effects:

``` css
<style type="text/css">
	body > div
		{
      width: 400px;
			height: 200px;
      background: gray;
      transition:all 0.3s ease; /* Transition will be for the effect. Tranistion all properties at a speed of 0.3 seconds with the default ease value for timing. */
		}
</style>
```

Now for some animations! Here's a fade in to a different color on hover:

``` html
<!DOCTYPE html>
<html>
<head>
    <style type="text/css">
    </style>
</head>
<body>
    <div class = "fade"></div>
</body>
</html>
```

``` css
<style type="text/css">
	body > div {
    width: 400px;
		height: 200px;
    background: gray;
    transition:all 0.3s ease; /* Transition will be for the effect. Tranistion all properties at a speed of 0.3 seconds with the default ease value for timing. */
	}

	.fade {
    opacity:0.5;
	}

	.fade:hover {
    opacity:1;
	}
</style>
```

Notice we gave the div a class of "fade". The class will have intially an opcaity of 0.5. On hover, the opacity will tranistion to 1 with the transition parameters we set for the div.

Okay so now how about a transform:

``` html
<!DOCTYPE html>
<html>
<head>
    <style type="text/css">
    </style>
</head>
<body>
    <div class = "shrink"></div>
</body>
</html>
```

``` css
<style type="text/css">
	body > div{
    width: 400px;
		height: 200px;
    background: gray;
    transition:all 0.3s ease; /* Transition will be for the effect. Tranistion all properties at a speed of 0.3 seconds with the default ease value for timing. */
	}

	.shrink:hover{
    -webkit-transform: scale(0.8);
    -ms-transform: scale(0.8);
    transform: scale(0.8);
	}
</style>
```

Transform allows you to rotate, scale, move, and skew elements among other things. We change our divs class to "shrink" and then on hover, have the div transform at our transition speed for the div. In this case, we are scaling the div down to 80%, shrinking it!

With many animations, it's important to add cross browser compatibility by not only calling the property, but also the browser specific property. In this case -ms-transform for IE and -webkit-transform for chrome, safari, and opera. This is also -moz for firefox if needed.

Here's a great cheatsheet for animation ideas that will take you further into animations, including things like translate and keyframes: http://www.justinaguilar.com/animations/
Download the css file to see all the examples.