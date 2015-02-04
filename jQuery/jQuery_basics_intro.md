{\rtf1\ansi\ansicpg1252\cocoartf1344\cocoasubrtf720
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\froman\fcharset0 Times-Roman;}
{\colortbl;\red255\green255\blue255;}
\margl1440\margr1440\vieww13760\viewh11960\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural

\f0\fs26 \cf0 What is jQuery?\
============
\fs24 \
jQuery is a Javascript library that is meant to present complicated Javascript code in an easier and more efficient manner\
\

\fs26 Why should I bother with jQuery?\
=========================
\fs24 \
jQuery can accomplish a lot of things. It simplifies Javascript to the point where many lines of Javascript can be turned into a single line of jQuery. It is used very widely throughout the web development industry, and can accomplish almost any task via a number of plugins. \
\

\fs26 Getting Started
\fs24 \
============\
The first thing you need to do is decide how we are going to get jQuery onto your webpage. There are two methods typically used to accomplish this\'85\
\
a. Downloading jQuery:\
\'97\'97\'97\'97\'97\'97\'97\'97\'97\'97-\
Downloading jQuery directly from jQuery.com means you will need to keep it in the same directory as the pages you wish to use it on. This gives you more control but can be a bit of a hassle to keep updated. The code for this would be something like:\
\
\pard\pardeftab720

\f1 \cf0 \expnd0\expndtw0\kerning0
<head>\
<script src="jquery-1.11.2.min.js"></script>\
</head> 
\f0 \kerning1\expnd0\expndtw0 \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural
\cf0 \
b. Using a CDN:\
\'97\'97\'97\'97\'97\'97\'97\
Both Google and Microsoft provide jQuery CDNs (Content Delivery Network). These allow you to use the jQuery library through one of these sources using code such as the following:\
\
\pard\pardeftab720

\f1 \cf0 \expnd0\expndtw0\kerning0
<head>\
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>\
</head> \
\
\pard\pardeftab720

\f0\fs26 \cf0 \kerning1\expnd0\expndtw0 jQuery syntax 
\fs24 \
===========\
In general a jQuery element will look something like this:\
$(
\i HTMLelement
\i0 ).
\i action
\i0 ()\
*The $ symbol says that we are defining jQuery\
*(
\i HTMLelement) 
\i0 is the element of your page we are going to affect\
*
\i action()
\i0  is where we define the jQuery function we would like to perform on the HTML element\
\
A working example of this would be:\
$(\'93h1\'94).hide()\
This would hide all <h1> elements on the webpage\
\

\fs26 Beginning your jQuery\
=================
\fs24 \
In order to prevent your jQuery from running before your page loads you always want to place your jQuery within a document ready event. This would look something like this:\
\pard\pardeftab720

\f1 \cf0 \expnd0\expndtw0\kerning0
\
$(document).ready(function()\{\
\'a0\'a0 
\i \expnd0\expndtw0\kerning0
// jQuery methods go here...
\i0 \expnd0\expndtw0\kerning0
\
\});
\f0 \kerning1\expnd0\expndtw0  \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural
\cf0 \
Tip: \'93\expnd0\expndtw0\kerning0
$(document).ready(function()\{\'93\kerning1\expnd0\expndtw0  can be shortened to just \'93\expnd0\expndtw0\kerning0
$(function()\{\'93\
\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural

\fs26 \cf0 \expnd0\expndtw0\kerning0
Give it a try! \

\fs24 \expnd0\expndtw0\kerning0
==========\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural

\fs26 \cf0 \expnd0\expndtw0\kerning0
Lets try some jQuery out using a well known example.
\fs24 \expnd0\expndtw0\kerning0
 \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural
\cf0 \expnd0\expndtw0\kerning0
\
1. Create an HTML page and link jQuery to it using one of the methods above. \
2. Create a <button>Click Me</button> on your HTML page along with some <p> entries. \
3. Now add the following jQuery in the <head> or by linking another file:\
\
\pard\pardeftab720

\f1 \cf0 \expnd0\expndtw0\kerning0
$(document).ready(function()\{\
\'a0\'a0\'a0 $("button").click(function()\{\
\'a0\'a0\'a0 \'a0\'a0\'a0 $("p").hide();\
\'a0\'a0\'a0 \});\
\}); \
\
4. 
\f0 \expnd0\expndtw0\kerning0
View your page, when you click the button your paragraphs should disappear!\
\
\pard\pardeftab720

\fs26 \cf0 Where to go from here
\fs24 \
===================\
jQuery is a powerful tool that has lots to offer. There are a number of awesome online resources to further expand your jQuery knowledge such as w3schools.com or code academy.com\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural
\cf0 \expnd0\expndtw0\kerning0
\
}