# Method returns

Every method in Ruby returns a value, even if that value is `nil` (Ruby's way of saying "nothing"). There are two ways to return a value: explicitly and implicitly.

## Explicit returns

Sometimes you want to stop a method in its tracks because you already have what you want to return. In these cases, like below, you can call return and pass in a value.

``` ruby
def current_month(format=:number)
  current_time = Time.now
  case format.downcase.to_sym
  when :number then return current_time.strftime('%-m').to_i
  when :word   then return current_time.strftime('%B')
  else              raise  TypeError, 'Only acceptable formats are :number and :word.'
  end
end
```

The above method will return the following:

``` ruby
current_month
=> 2
```

``` ruby
current_month(:number)
=> 2
```

``` ruby
current_month(:word)
=> "February"
```

Notice that for an invalid format, we don't get a `=>`, indicating a returned value. Instead, `raise` stops the program completely so that the programmer knows they're not using the method correctly. The method *would have* eventually returned a value, except it was not allowed to finish running.

``` ruby
current_month(:invalid_format)
TypeError: Only acceptable formats are :number and :word.
```

## Implicit returns

Probably most returns in Ruby are implicit. If no return is explicitly called, then a return is assumed for the last line of the method.

``` ruby
def current_month
  Time.now.strftime('%B')
end
```

``` ruby
current_month
=> "February"
```

As we can see by the `=>`, `"February"` is returned by `current_month`. The method is behaving exactly the same as if an explicit return were called like this:

``` ruby
def current_month
  return Time.now.strftime('%B')
end
```

Unnecessarily explicit returns are usually considered a "code smell" in Ruby, meaning it's kind of ugly and makes programmers squirm.

### Empty methods

This is even true in the case of an empty method.

``` ruby
def empty_method
end
```

``` ruby
empty_method
=> nil
```

The method is behaving exactly as it would with an explicit return, with nothing passed into it.

``` ruby
def empty_method
  return
end
```
