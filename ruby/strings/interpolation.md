# String interpolation

"Interpolation" is just executing code and dumping the results in the middle of a string. In Ruby, **interpolation can only be done within a string surrounded by double quotes** (single quotes create a "literal" string).

To run code inside of a double-quoted string, just type `#{`YOUR-CODE-HERE`}` somewhere in the string. Here are some examples:

``` ruby
"2 + 2 = #{2 + 2}"
=> "2 + 2 = 4"
```

``` ruby
name = 'Chris'
"My name is #{name}! What's yours?"
=> "My name is Chris! What's yours?"
```

``` ruby
current_time  = Time.now
current_day   = Time.now.strftime('%-d')
current_month = Time.now.strftime('%B')
current_year  = Time.now.strftime('%Y')
"This is day #{current_day} of #{current_month}, in the year #{current_year}!"
=> "This is day 1 of February, in the year 2015!"
```