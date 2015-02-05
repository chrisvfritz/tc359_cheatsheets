# Array Creation

There are a *lot* of ways to create arrays in Ruby. Here are some that I commonly use.

## Empty

``` ruby
my_array = Array.new
=> []
```

``` ruby
my_array = []
=> []
```

## Anything

The most obvious and probably common way to create an array in Ruby is by listing everything out between brackets, separated by commmas.

``` ruby
weekdays = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday']
=> ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]
```

These don't have to all be of the same type. You could mix a bunch of random stuff into the same array.

```
random_stuff = [4, 'pocket lint', Time.now]
=> [4, "pocket lint", 2015-02-01 12:18:50 -0500]
```

And you don't even have to list everything on the same line, if things would more more readable split into multiple lines.

``` ruby
my_favorite_things = [
  Raindrop.new( surface: Flower.new(type: 'rose') ),
  Whisker.new( owner: Cat.new(age: 1) ),
  Kettle.new( material: 'copper', condition: 'bright' ),
  Mitten.new( material: 'wool', temperature: 'warm' )
]
=> [#<Raindrop:0x007fe3f59d26d8>, #<Whisker:0x007fe3f2950370>, #<Kettle:0x007fe3f531a020>, #<Mitten:0x007fe3f5a13bd8>]
```

## Words

There are many times when you just want a list words and there's a nice helper in Ruby where you can type the words within a `%w()` and it'll split everything up by the spaces.

``` ruby
weekdays = %w(Monday Tuesday Wednesday Thursday Friday)
=> ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]
```

This way, you don't have to type out all those annoying quotes and commas.

## Ranges

`1..10` creates a "range" in Ruby and `to_a` converts that range to an array. Very compact!

``` ruby
numbers_from_one_to_ten = (1..10).to_a
=> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

You can do this not only for numbers, but also for strings.

``` ruby
alphabet = ('a'..'z').to_a
=> ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
```