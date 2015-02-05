# Symbols

These are symbols:

``` ruby
:an_example_symbol
:'This is a symbol too!'
```

They look kind of like a variable name or string, except they have a colon in front.

Symbols are a somewhat unusual feature in Ruby. They can be difficult for many people to understand at first, but here's what you really need to now: **if you have a string that you'll never need to change, it should be a symbol.**

The really short explanation is that if it doesn't need to be a string, then it's much more efficient for the computer to work with a symbol instead.

## Practical uses

### To represent a limited number of parameter values

In the following example, the `format` variable can only either be a number or word, so we use the symbols `:number` and `:word` to represent those options.

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

### To organize values in a hash

Symbols are very often used to access items in a hash, because they're readable by a human looking at the code, but the computer never has to *manipulate* them (so they never have to be *thought of* as strings.

In the example below, the values that we're pointing to are *not* appropriate as symbols however, because I can very easily think of cases when I might want to manipulate these strings to generate a username or display initials.

``` ruby
me = {
  :first_name => 'Chris'
  :last_name  => 'Fritz'
}
```

``` ruby
me[:first_name]
=> 'Chris'
```

``` ruby
me[:last_name]
=> 'Fritz'
```
