# Method parentheses

Method parentheses are optional in Ruby (except when necessary for clarification). The example in the methods README could also have been written like this:

``` ruby
def current_month()
  Time.now.strftime('%B')
end
```

Then if we ever want to get the current month, we can run that code by calling `current_month`:

``` ruby
current_month()
=> "February"
```

The same is true when a method takes one or more parameters. Both of the following are acceptable:

``` ruby
def say_hello(name)
  "Hello #{name}!"
end
```

``` ruby
def say_hello name
  "Hello #{name}!"
end
```

Even when *calling* a method with parameters, the parentheses are optional:

``` ruby
say_hello('Chris')
=> "Hello Chris!"
```

``` ruby
say_hello 'Chris'
=> "Hello Chris!"
```

The only time when you must have parentheses, are with nested methods that take parameters. Though Ruby is often smart enough to figure out what you're trying to do anyway, not including parentheses in these cases can sometimes cause unexpected results. And even when they don't, they can still be difficult for *people* to read. Here's an example of how to do it right:

``` ruby
say_hello say_hello('Chris')
=> "Hello Hello Chris!!"
```
