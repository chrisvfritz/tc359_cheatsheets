# String substitution

"Substitution" is just finding something in a string and replacing it with something else. Just like the Find & Replace you see in many text editors. Most of the time, string substitution is done with one of two methods:

## `sub`

`sub` substitutes the first instance it finds of the first string with the second string.

``` ruby
'This is a test.'.sub('is', 'is NOT')
=> "This NOT is a test."
```

In cases where there are multiple instances of the search string, only the first will be replaced.

``` ruby
'This is a test. And that is a giraffe.'.sub('is', 'is NOT')
=> "This NOT is a test. And that is a giraffe."
```

## `gsub`

`gsub` does exactly what `sub` does, except it acts *globally*, replacing *all* instances of the search string with the replacement string.

``` ruby
'This is a test. And that is a giraffe.'.sub('is', 'is NOT')
=> "This NOT is a test. And that is NOT a giraffe."
```
