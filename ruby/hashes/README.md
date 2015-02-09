# Hashes

Hashes are an arbitrary collection of key-value pairs. If that doesn't make any sense to you, don't worry. It's simpler than you think. Let's take a look at a simple example.

Whether you realize it or not, you kind of have a hash in your head this very moment. There are some phrases for which there is usually only one response. This is what your hash for small talk might look like:

``` ruby
SMALL_TALK = {
  'go green'              => 'go white',
  'sup'                   => 'nothin much',
  'how bout them tigers'  => 'umm... yeah, how about them?',
  'they say it will rain' => 'i hope it does not'
}
```

Then when your brain is looking for an appropriate response to one of these statements - sometimes before you even register what's been said, it runs the conversation through a method like this:

``` ruby
def appropriate_response_to(phrase)
  SMALL_TALK[phrase]
end
```

And that's how you know that when someone says "go green" you just say "go white" - it's just habit.

``` ruby
appropriate_response_to 'go green'
=> "go white"
```

If a key (one of the phrases on the left of the hash definition) doesn't match what you feed into it, then `appropriate_response_to` returns `nil` and you know you have to actually use the rest of your brain to figure out what to say.
