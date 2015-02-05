For this example of parallax scrolling, css is used because it allows a browser to use hardware acceleration which means consistent frame rates and smoother scrolling.

The basic idea is that there will be multiple layers that scroll at different "speeds" because they appear to be at different depths.

This styling example shows how it can be done:

``` css
.parallax {
  perspective: 1px;
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;
}
.parallax__layer {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
.parallax__layer--base {
  transform: translateZ(0);
}
.parallax__layer--back {
  transform: translateZ(-1px);
}
```

when used with html like the following:

``` html
<div class="parallax">
<div class="parallax__layer parallax__layer--back">
...
</div>
<div class="parallax__layer parallax__layer--base">
...
</div>
</div>
```


basically, the parallax class height and perspective properties will lock the perspective to the center and setting overflow-y to auto will allow the page to scroll regularly.

as you can see, translating the back layer by -1 in the z direction and keeping the base layer at zero, will make the back layer scroll slower than the base layer.

more information can be found on this website: http://keithclark.co.uk/articles/pure-css-parallax-websites/
