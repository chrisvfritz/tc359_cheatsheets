# Hash Access

Accessing a hash in Ruby is simple. Let's say we have the following hash:

``` ruby
small_talk = {
  'go green'              => 'go white',
  'sup'                   => 'nothin much',
  'how bout them tigers'  => 'umm... yeah, how about them?',
  'they say it will rain' => 'i hope it does not'
}
```

The items on the left are keys, all pointing to a respective value. To access a value in that hash, we have to call its key in square brackets (`[]`). Some examples:

``` ruby
small_talk['go green']
=> "go white"

small_talk['sup']
=> "nothing much"
```
