Getting Started With React.JS
======

What is React?
------

React is a Javascript libary that makes it easier to maintain a consistant UI in contexts where the data being represented is constantly changing. It allows you to write in an XML like syntax called <a href="http://facebook.github.io/react/docs/jsx-in-depth.html">JSX</a>, making it simple to build and edit code.  

Setting up
------

There are a few tools you'll need to write in React. If you want to skip the setup and get right to working in React, you can use the <a href="http://jsfiddle.net/reactjs/69z2wepo/">React.JS fiddle</a>.

In order to write in React with JSX, you'll need two download the React files, which can be found at <a href="http://facebook.github.io/react/index.html">facebook.github.io/react</a>. If you download the starter pack, there will be a few optional addons, and a folder full of helpful code examples.

Go through the <a href="http://facebook.github.io/react/docs/getting-started.html">Getting Started</a> setup to get your development environment up and running. You'll need the command-line tools to test React with JSX offline.

Writing in React
------

React is an object oriented javascript syntax. When writing in React, you will pretty much always create an object or class, and then render an instance of that object. It is important to use this pattern if you want to take full advantage of the framework.

Creating a class in react is a lot like writing in HTML, but much more flexible and powerful. A simple React class can be made with the following format:

	var NameOfClass = React.createClass({
		render:function(){
			return (
				<tag>
					content
				</tag>
			)
		}
	});

The first letter of the name in a React class is **always** capitalized. The tags are written very much like HTML and can be nested and indented just like you would with regular HTML.

After you create a class, you can render it like this:

	React.render(<NameOfClass />, document.getElementById("content"));

This is the very most basic format for writing in React. This isn't really very exciting though, so we'll do an example with minimal interactivity and introduce object properties into the mix.

Our example will be a simple counter that allows you to add or subtract 1 from the displayed value. Here's the code:

	var Counter = React.createClass({
        getInitialState: function(){
            return {count: this.props.initialCount};
        },
        addToCount: function (number) {
            this.setState({ count: this.state.count + number })
        },
		render:function(){
			return (
                <div>
                    <h2>{this.state.count}</h2>
                    <CounterButton text="LESS" action={this.addToCount.bind(this, -1)} />
                    <CounterButton text="MORE" action={this.addToCount.bind(this, 1)} />
                </div>
			)
		}
	});

	var CounterButton = React.createClass({
		render:function(){
			return (
				<button onClick={this.props.action}>{this.props.text}</button>
			)
		}
	});
    
	React.renderComponent(<Counter initialCount={2} />, document.body);

To break down the code above, when we use <code>var Counter = React.createClass()</code> we are creating a new **object**. Then we add the **methods** <code>getInitialState</code> and <code>addToCount</code> and <code>render</code> to that object. In <code><CounterButton text="LESS" action={this.addToCount.bind(this, -1)} /></code> we are declaring the value of the property **text**, which we create later when we call <code>{this.props.text}</code>. And we are also calling the function <code>addToCount</code>, when the <code>CounterButton</code>s are clicked.. In JSX, the HTML-like syntax that gets returned by each React object, if we ever need to include javascript in our code, we use curly braces <code>{ }</code> to do so.

Then there is the "state" object. React works by comparing the state of the UI to the state of the UI previously, calculating the difference, and adding in the changes. The state object allows us to automatically update the view when data changes, and it's why React is so powerful. In our <code>getInitialState</code> function, the line <code>return {count: this.props.initialCount};</code> gets the initial count for the counter, which we set to 2 when we call <code><Counter initialCount={2} /></code>. We then use our <code>addToCount</code> method to change the count, and call on the method any time we push one of our two buttons.

This gives a short overview of how React can be used. Like most things, the bulk of the learning will be done in the <a href="">documentation</a>, through other resources, and from trial and error.

Resources
------
<a href="https://www.youtube.com/watch?v=rFvZydtmsxM">React.js Components Part I</a>

<a href="https://www.youtube.com/watch?v=XxVg_s8xAms">Introduction to React.JS</a> (first 25 minutes)

<a href="http://facebook.github.io/react/docs/getting-started.html">Facebook documentation</a>

<a href="http://jsfiddle.net/reactjs/69z2wepo/">React.JS fiddle</a>




