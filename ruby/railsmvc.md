#MVC Primer

Model-View-Controller is a software pattern for user interfaces that splits the software into 3 components based on function, called the view, the model, and the controller.

- The model is the central component which manages the data of the application. Typically it includes a database, and business logic associated with the app.
- The view is the component which handles displaying data to the user. It requests data from the controller when it needs to, and then displays it whatever form is necessary.
- The controller handles user input and sends instructions to the view. Once it collects and validates input, it sends the data to the model to be handled, and sends new instructions to the view

It is important that the view and the model never interact directly. The controller gets data from the model, and then tells the view how to change. The controller controls the overall application. 

#Rails and MVC

Rails by default supports an MVC architecture. Specifically, it creates an MVC architecture that works as follows
- A model is a class that wraps a SQL database and provides functions for accessing the tables inside it without the need for SQL queries
- A view is an html page
- A controller is a set of methods that are run when the associated view is active.

![alt text](https://camo.githubusercontent.com/569fe8a8431ec8532a7ff5e4debc12bf9d86f962/687474703a2f2f7261696c737475746f7269616c2e6f72672f696d616765732f666967757265732f6d76635f64657461696c65642d66756c6c2e706e67 "MVC example")
