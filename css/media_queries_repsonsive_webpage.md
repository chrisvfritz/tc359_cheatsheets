# Using Media Queries to Make a Responsive Webpage

Media queries are a great thing to use when you want your webpage to become responsive and also work on different fixed screens. 

When done correctly your webpage should work on any screen type without you actually having to check on the individual screens.

### Overview

```
@media (max-width: 500px) {
	
}
```
1. @media is to call the media query

2. max-width is used when you want to change something in the webpage to look differently when the maximum width of the page is what you specify it to be.

3. min-width works in a similar way that max-width does except for you are telling the webpage to change something when the minimum width of the page is what you specify it to be.

4. The pixels you set is up to you but there are some things you should keep in mind as far as the size of phone screens, tablets, laptops, computer screens, and much more. Therefore you want multiple media queries set to change at different widths in order to look good no matter how large or small the width of the screen is.

5. The {} are for you to put CSS into. This is what you want to change once the webpage's width has increased or decreased to what you have set it to be.

### Applying a Media Query

Lets change this code so that when you are on a tablet your contact image on your webpage is a little larger and easier to see.

```
#contact_image {
	width: 250px;
}
```
Take that CSS and apply a media query to it.

```
@media (max-width: 900px) {
	#contact_image {
		width: 350px;
	}
}
```

Now when your webpage is below 900px the width of your contact image will increase from 250px to 350px.

### Wrapping Up

Media queries can be used in many different situations. This is obviously one of the most common ways to use one. They are very powerful and make converting a website into a responsive one quite easy at times, while sometimes making your job quite frustrating. If you are creating a webpage that you know is going to be responsive, it is good to keep that in mind when you are creating it. Hopefully it will make you write better code. There are also a lot of situations that you can use percentages for instead of fixed widths. This will save you a lot of time as well. And remember that a website being responsive is basically mandatory these days, especially if you want to look professional and target a larger audience.

