AngularJS - The Basics
======================

What is AngularJS?
------------------
Angular JS is a html/JS framework that allows you to have JS functionality in HTML Documents. You can have data and user content without even needing a separate .js file (Although it's a good idea to keep the code clean). Basically Angular lets you make static HTML web-pages more dynamic.

How to use AngularJS?
---------------------
Like any Framework, you need to download the files needed for running it. You can do that by downloading from [Angular](https://angularjs.org/) or cloning from github [here](https://github.com/angular/angular.js)

Once installed, you use Angular in your HTML and JS files. I rely on the API docs heavily [Angular/API](https://docs.angularjs.org/api)

Here are the basics you need to know about, all of which are explained here in the [Angular/Guide](https://docs.angularjs.org/guide)
--------------------------------------------------------------------------------------------------------------------
 * **Controllers**
      Controllers are Javascript constrictor functions that allow Angular to augment Scope. Meaning that Angular uses controllers to define or limit the related Scope object. Controllers should be used to set up the inital state of a Control object or add behavior to a scope object.
 * **Factories**
      Think of service Factories as groups of functions, almost like a class. Factories are set up by service providers which have a property called $get which holds the service factory.
 * **Services**
      Services are single object ran by a factory. You can learn more about Controllers, Factories and Services from the [Angular Docs](https://docs.angularjs.org/api/auto/service/$provide)

 * **Data binding**  
      Data Binding is how Angular syncs the data between views and models, allowing sites to have dynamic content. This is the core of AngularJS
      You can see how in Angular documents, there are "weird" attribute on html tags, like <div ng-body>. This is how we implement data binding.
      The ng-bind directive binds application data to the HTML view. You can learn more from [w3schools](http://www.w3schools.com/angular/angular_intro.asp)
 * **Expressions**  
      In pure HTML, you can't type in 2+2 and expect 4 to be displayed on the page. Well thanks to Angular, expressions like 1+2 or items[index] are now possible! All thats required is using double curly brackets {{2+2}} and your html page will display 4
 * **Directives**  
      "At a high level, directives are markers on a DOM element (such as an attribute, element name, comment or CSS class) that tell AngularJS's HTML compiler ($compile) to attach a specified behavior to that DOM element or even transform the DOM element and its children. There are built in directives such as ng-model and you also have the ability to create you own custom directives as well."
 * **Views and routes (see the example)**  
      "$route is used for deep-linking URLs to controllers and views (HTML partials). It watches $location.url() and tries to map the path to an existing route definition."
 * **Filters** 
      "A filter formats the value of an expression for display to the user. They can be used in view templates, controllers or services and it is easy to define your own filter."
 * **Forms**  
      "Controls (input, select, text-area) are ways for a user to enter data. A Form is a collection of controls for the purpose of grouping related controls together.
      Form and controls provide validation services, so that the user can be notified of invalid input. This provides a better user experience, because the user gets instant feedback on how to correct the error. Keep in mind that while client-side validation plays an important role in providing good user experience, it can easily be circumvented and thus can not be trusted. Server-side validation is still necessary for a secure application."
 * **Initalizing a Angular app**
      Angular initializes automatically upon DOMContentLoaded event or when the angular.js script is evaluated if at that time document.readyState is set to 'complete'. At this point Angular looks for the ng-app directive which designates your application root.  Read more on [Angular Docs](https://docs.angularjs.org/guide/bootstrap)

Tutorials:
----------
   * [Angular/Tutorial](https://docs.angularjs.org/tutorial)
   * [w3schools](http://www.w3schools.com/angular/)
   * [thinkster](https://thinkster.io/a-better-way-to-learn-angularjs/)

My confession:
--------------
   I hope you learned enough to get interested in AngularJS, I'm still wrapping my head around the concepts. I used angularjs.org to verify what I thought I knew as well as copy the information that I didn't. Please visit [Angular](https://angularjs.org/) if you want to learn more. Anything in "" can be found on angularjs.org