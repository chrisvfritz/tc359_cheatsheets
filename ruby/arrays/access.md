# Array Access

There are a few different ways to access an item in an array in Ruby. This is not an exhaustive list - just some examples of the most common methods. In all of the examples below, I'll be demonstrating with this hypothetical array:

``` ruby
array = ['one', 'two', 'three']
```

## By index

Access with the position of the item in the array, starting with 0 (don't ask why 0 instead of 1) - it makes sense if you think in bits like a computer, but certainly not for humans.

``` ruby
array[0]
=> "one"
```

``` ruby
array[1]
=> "two"
```

``` ruby
array[2]
=> "three"
```

## By relative position

``` ruby
array.first
=> "one"
```

``` ruby
array.last
=> "three"
```

``` ruby
array.first(2)
=> ["one", "two"]
```

## By value

`select` will find *all* items that match the criteria.

``` ruby
array.select do |item|
  item != 'two'
end
=> ["one", "three"]
```

`find` only returns the *first* item that matches the criteria.

``` ruby
array.find do |item|
  item != 'two'
end
=> "one"
```

## Randomly

`sample` just grabs a random item.

``` ruby
10.times do
  puts a.sample
end
```

Output:

```
three
two
three
three
one
three
two
two
one
one
```