# Method Parameters

A method parameter is just a value that gets passed to a variable used in a method.

``` ruby
def say_hello(name)
  "Hello #{name}!"
end
```

When you call this method, you'll pass in the value the variable should have.

``` ruby
say_hello('Chris')
=> "Hello Chris!"
```

## Multiple parameters

When there are multiple parameters, they'll be separated by a comma.

``` ruby
# This is like the method above, except we abbreviate the middle name
# to its first letter, turning it into an initial.
def say_hello(first_name, middle_name, last_name)
  "Hello #{first_name} #{middle_name[0]} #{last_name}!"
end
```

## Optional parameters

You can make a parameter optional by giving it a default value.

``` ruby
def say_hello(name, title=nil)
  "Hello #{ title + ' ' if title }#{name}!"
end
```

Now we can still just pass in a single parameter for the name, with the same results.

``` ruby
say_hello 'Sarah'
=> "Hello Sarah!"
```

Or if the person we're addressing has a special title we should use, we can pass that in as well.

``` ruby
say_hello 'Sarah', 'Dr.'
=> "Hello Dr. Sarah!"
```

## Advanced parameters

If you want to know more, here's some stuff that's a little fancy.

### Splat parameters

In cases where you might want to accept *any* number of parameters, you can use a "splat" by placing an asterix (`*`) in front of the variable that will now contain an array of anything passed in. For example, the below methods will say hello to any number of people.

``` ruby
# Joins a list of strings in the style of the oxford comma
def oxford_join(names)
  return names[0] if names.size == 1

  names[-1] = "and #{names.last}" if names.size > 1

  if names.size == 2
    names = names.join(' ')
  elsif names.size > 2
    names = names.join(', ')
  end

  names
end

# Says hello to any number of people
def say_hello(*names)
  "Hello #{ oxford_join names }!"
end
```

``` ruby
say_hello 'Sarah'
=> "Hello Sarah!"
```

``` ruby
say_hello 'Sarah', 'Michael'
=> "Hello Sarah and Michael!"
```

``` ruby
say_hello 'Sarah', 'Michael', 'Charles'
=> "Hello Sarah, Michael, and Charles!"
```

Fancy!

### Hash parameters

Hash paremeters can be useful when we have multiple optional parameters, like in the following example.

``` ruby
def translate_hello(language)
  case language.downcase
  when 'french',  'fr' then 'Bonjour'
  when 'german',  'de' then 'Guten Tag'
  when 'dutch',   'nl' then 'Goeiedag'
  when 'spanish', 'es' then 'Hola'
  else                      'Hello'
  end
end

def say_hello(name, options={})
  hello = translate_hello options[:language].to_s
  title = options[:title] ? options[:title].to_s + ' ' : ''
  "#{hello} #{title}#{name}!"
end
```

Now we can call `say_hello` with only a name or with any combination of optional parameters we're using.

``` ruby
say_hello 'Sarah'
=> "Hello Sarah!"
```

``` ruby
say_hello 'Sarah', title: 'Ms.'
=> "Hello Ms. Sarah!"
```

``` ruby
say_hello 'Sarah', language: 'fr'
=> "Bonjour Sarah!"
```

``` ruby
say_hello 'Sarah', title: 'Dr.', language: 'de'
=> "Guten Tag Dr. Sarah!"
```
