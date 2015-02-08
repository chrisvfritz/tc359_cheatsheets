After starting with the basic HTML markup seen below, there are a few simple guidelines you can follow to create cleaner markup.

``` html
<!DOCTYPE html>
<html>
  <head>
    <title></title>
  </head>
  <body>
  </body>
</html>
```

When a tag is located within another tag: tab.

Additionally, if there is a group of tags located inside of another tag, stack the opening and ending tags on top of one another, and fill in the content as seen below:

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>Title</title>
  </head>
  <body>
    <div>
      <h1>This is a Heading</h1>
      <p><img alt="picture" src="images/image.png"/></p>
      <p>This is a paragraph.</p>
    </div>
  </body>
</html>
```
