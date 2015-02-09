# Array Iteration

"Iteration" just means going through each item in an array and doing something with each item. Here are the most common ways of doing this in Ruby.

## `each`

This takes each item of the array, gives it a name (`number` in the below example), and then does something with number for each item in the array. The below example happens to print out each item.

``` ruby
['one', 'two', 'three'].each do |number|
  puts number
end
```

Output:

```
one
two
three
```

## `each_with_index`

`each_with_index` does the same as `each`, except adds another variable to keep track of which place in the array we're at, starting with 0.

``` ruby
['one', 'two', 'three'].each_with_index do |number, index|
  puts "#{index + 1}: #{number}"
end
```

Output:

```
1: one
2: two
3: three
```
