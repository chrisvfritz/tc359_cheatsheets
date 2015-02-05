# Ruby blocks

Blocks are an essential component in Ruby. They're used to pass code to a method. There are two ways of representing blocks in Ruby.

## `do` .. `end`

This is probably the most common method of representing a block.

``` ruby
3.times do
  puts 'hello'
end
```

Output:

```
hello
hello
hello
```

In some cases, like for the `each` method, we'll want to pass a variable to the block. We can name variables within pipes (`|`) right after the `do`.

``` ruby
['hello', 'goodbye'].each do |salutation|
  puts salutation.capitalize
end
```

Output:

```
Hello
Goodbye
```

## `{` .. `}`

When you only have a single, short command to run, curly braces are often used in place of `do` and `end`, making the code a bit shorter so it can fit on one line. This is a stylistic choice.

``` ruby
3.times { puts 'hello' }
```

Output:

```
hello
hello
hello
```

``` ruby
['hello', 'goodbye'].each { |salutation| puts salutation.capitalize }
```

Output:

```
Hello
Goodbye
```
