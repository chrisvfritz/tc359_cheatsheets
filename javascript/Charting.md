# Charting Libraries - when and why

## D3.js
D3 is an extremley powerful charting library.  It doesn't come prepackaged with default charts that you flesh out allowing for extensive creativity. Rather, it provides you with the tools necessary to make the connection between data and graphic display  A very advantageous choice anytime a developer needs to show data in a flashy and creative way.  Not usually a good choice when working with very large amounts of data.  D3 works by manipulating DOM elements which tends to be very slow when working with a lot of entries. Would recommend for doing something like comparing the stats of two athletes within a superbowl vs comparing the stats of every athlete to ever play the superbowl. 

D3 also tends to not work very well with Internet Explorer.

## Chart.js
One of the most popular charting libraries today, chart.js is extremley easy to use. It uses HTML 5 canvas making the learning curve practically non-existant.  Chart.js comes with 6 basic charts that will satisfy pretty much any basic charting need.  Usually works pretty well in responsive web layouts but doesn't always like to play nice with twitter bootstrap.  Framework is also very easy to edit making it super-customizable.  I can pretty much recommend using chart.js in any situation except one where you need a lot of creativity in your display.

Chart.js works well with old browsers like IE 7 and 8 helping to eliminate the headache of cross browser support for web devs.

## Highchart.js
Also a very popular charting library, highchart.js comes pre-loaded with cool animations and a lot of flash.  Similiar to chart.js it comes loaded with several pre-made graphs. Highchart is very compatibile with older browsers, it even works well with the dreaded IE6.  A really good choice if you have a good idea that your user base may not be the most technologically advanced.

Highchart is very easy to integrate into any framework.  One of the easiest charting libraries to drop into twitter bootstrap.  

## Google Charts
One of the easiest charting libraries to use.  A very quick and painless process for getting a chart built and displaying.  Also does a great job with cross platform support like working well with Android/iOS devices.  It also works decent with older IE versions.  Would recommend anytime a developer needs something done quickly and wants it to display well on mobile without too much extra work.

## Flot.js
One of my absoloute favorite charting libraries.  Very easy to use and has excellent documentation.  Also I tend to have the best success using flot with bootstrap as it always tends to scale very well with the mobile layouts. I recommend using it on web apps that will be used equally on both desktops and mobile platforms.  However, flot is not very extensible.  It's a little more difficult to customize it as compared to a library like chart.js.  

Flot also works well with older browsers like IE6.

## Chartkick
I actually have no experience with chart kick but i thought i'd include it here since this is a ruby class.  Chartkick is awesome because it is a ruby gem and is also very easy and quick.  Chartkick will also integrate with both Highchart and Google Charts.  Chartkick will also work without ruby since it is also a javascript library i.e. chartkick.js.
