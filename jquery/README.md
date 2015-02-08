What is jQuery?
===============
jQuery is a Javascript library that is meant to present complicated Javascript code in an easier and more efficient manner

Why should I bother with jQuery?
================================
jQuery can accomplish a lot of things. It simplifies Javascript to the point where many lines of Javascript can be turned into a single line of jQuery. It is used very widely throughout the web development industry, and can accomplish almost any task via a number of plugins.

Getting Started
===============
The first thing you need to do is decide how we are going to get jQuery onto your webpage. There are two methods typically used to accomplish this

a. Downloading jQuery:  
Downloading jQuery directly from jQuery.com means you will need to keep it in the same directory as the pages you wish to use it on. This gives you more control but can be a bit of a hassle to keep updated. The code for this would be something like:

script src="jquery-1.11.2.min.js"

b. Using a CDN:  
Both Google and Microsoft provide jQuery CDNs (Content Delivery Network). These allow you to use the jQuery library through one of these sources using code such as the following:

script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"

jQuery syntax 
=============
In general a jQuery element will look something like this:

$(HTMLelement).action()

* The $ symbol says that we are defining jQuery  
* (HTMLelement)is the element of your page we are going to affect  
* action()is where we define the jQuery function we would like to perform on the HTML element  

A working example of this would be:  
$('h1').hide()  
This would hide all h1 elements on the webpage

Beginning your jQuery
=====================
In order to prevent your jQuery from running before your page loads you always want to place your jQuery within a document ready event. This would look something like this:

$(document).ready(function(){  
  jQuery methods go here...  
});  

Tip: $(document).ready(function() can be shortened to just $(function()

Give it a try!
==============
Lets try some jQuery out using a well known example.

1. Create an HTML page and link jQuery to it using one of the methods above. 
2. Create a Click Me button on your HTML page along with some "p" entries. 
3. Now add the following jQuery in the <head> or by linking another file:

$(document).ready(function(){  
  $("button").click(function(){  
    $("p").hide();  
  });  
});   

View your page, when you click the button your paragraphs should disappear!

Where to go from here
=====================
jQuery is a powerful tool that has lots to offer. There are a number of awesome online resources to further expand your jQuery knowledge such as w3schools.com or code academy.com
