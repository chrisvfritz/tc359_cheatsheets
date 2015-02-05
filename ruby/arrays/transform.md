# Transforming Arrays

Sometimes

## Transform each item individually

`map` is your go-to method here.

``` ruby
[1, 2, 3].map do |number|
  number + 1
end
=> [2, 3, 4]
```

``` ruby
['Abe Alderson', 'Brandy Bauer', 'Charles Chittendon the Fourth'].map do |name|
  name.downcase.gsub(' ', '-')
end
=> ['abe-alderson', 'brandy-bauer', 'charles-chittendon-the-fourth']
```

## Combine all items through a transformation

`inject` is your go-to method here. In the vast majority of cases, this is just used to sum up a list of numbers.

``` ruby
[1, 2, 3].inject do |first_number, second_number|
  first_number + second_number
end
=> 6
```
