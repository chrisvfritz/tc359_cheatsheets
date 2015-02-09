#Object Oriented CSS

Object Oriented CSS (OOCSS) is writing reusable CSS that is scalable. It is used for adding style to plain HTML websites.
Object Oriented CSS main function is to make sure that the CSS behaves the same way no matter where it is place.
It encourages code to be reused and to make more efficient stylesheets that are easier to maintain. 
OOCSS is faster to code because it removes the need to repeat code. 
It is easier for other developers to add to and modify.
OOCSS is based on two main principles the separation of structure from skin and separating container from content.

Separating structure from skin means to remove the positioning styles from the presentational styles and skin.
Separating container from content means to remove the dependency of the containers. This allows objects to be
placed in other containers and still look the same.

Separating structure from skin means to remove objects like position, float, margin, etc from objects like background, color, border, etc
Separating container allows the code to be independent and the not dependent on where it is on the page.

##Non Object Oriented CSS Example

###HTML

```
<aside>
    <h1>Latest News</h1>
    <ul>
        <li>
            <h3><a href="”#”">Lorem Ipsum Dolor</a></h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </li>
        <li>
            <h3><a href="”#”">Lorem Ipsum Dolor</a></h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </li>
        <li>
            <h3><a href="”#”">Lorem Ipsum Dolor</a></h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </li>
    </ul>
</aside>
```
###CSS

```
aside {
  float: right;
  width: 15em;
  padding: 2em;
}
 
aside h1 {
  margin: 0;
  font-size: 1.25em;
  border-bottom: 1px dashed #ccc;
}
 
aside ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
 
aside ul li {
  margin: 1em 0;
  padding-bottom: .5em;
  border-bottom: 1px dashed #ccc;
}
 
aside h3 {
  margin: 0;
  font-size: 1em;
}
 
aside h3 a {
  color: #000;
  text-decoration: none;
}
 
aside h3 a:hover {
  color: #1c86a1;
}
 
aside p {
  margin: .5em 0;
  font-size: .938em;
  line-height: 1.188em;
}
```

##Now with Object Oriented CSS

###HTML

```
<aside class="cont-right">
    <h1 class="section-heading no-margin separated">Latest News</h1>
    <ul class="item-list no-margin">
        <li class="item-list--item separated">
            <h3 class="area-heading no-margin"><a href="”#”">Lorem Ipsum Dolor</a></h3>
            <p class="item-content">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </li>
        <li class="item-list--item separated">
            <h3 class="area-heading no-margin"><a href="”#”">Lorem Ipsum Dolor</a></h3>
            <p class="item-content">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </li>
        <li class="item-list--item separated">
            <h3 class="area-heading no-margin"><a href="”#”">Lorem Ipsum Dolor</a></h3>
            <p class="item-content">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </li>
    </ul>
</aside>
```
###CSS

```
.cont-right {
  float: right;
  width: 15em;
  padding: 2em;
}
 
.section-heading {
  font-size: 1.25em;
}
 
.separated {
  border-bottom: 1px dashed #ccc;
}
 
.no-margin {
  margin: 0;
}
 
.item-list {
  padding: 0;
  list-style: none;
}
 
.item-list--item {
  margin: 1em 0;
  padding-bottom: .5em;
}
 
.area-heading {
  font-size: 1em;
}
 
.area-heading a {
  color: #000;
  text-decoration: none;
}
 
.area-heading a:hover {
  color: #1c86a1;
}
 
.item-content {
  margin: .5em 0;
  font-size: .938em;
  line-height: 1.188em;
}
```
It makes the HTML appear to be more complex, but it is now easier to track and change the styles. I found this online resource to be very helpful check it out [here.](http://appendto.com/2014/04/oocss/)


