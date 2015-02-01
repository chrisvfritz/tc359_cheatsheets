# Ruby methods

Methods are a way of storing code that you might want to run later. Here's a simple example of a method **def**inition:

``` ruby
def current_month
  Time.now.strftime('%B')
end
```

Then if we ever want to get the current month, we can run that code by calling `current_month`:

``` ruby
current_month
=> "February"
```
