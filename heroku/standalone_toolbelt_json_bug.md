This advice applies if you're using the standalone version of the Heroku toolbelt: that is, if you're running neither Windows, nor Mac OS, nor Debian or other derivatives.

Heroku Toolbelt depends plenty on JSON, which you can provide with `gem install json`. Beware of using `bundle clean` and *especially* `bundle clean --force`, however, because that will obliterate the JSON gem and ruin your day. Here's what I'm talking about:

```
[18:44 1771 ~/tc359/p5] % heroku apps:info
=== name
Error submitting error.
!    Heroku client internal error.
!    Search for help at: https://help.heroku.com
!    Or report a bug at: https://github.com/heroku/heroku/issues/new

   Error:       undefined method `map' for "[]":String (NoMethodError)
   Command:     heroku apps:info
   Version:     heroku-toolbelt/3.25.0 (x86_64-linux) ruby/2.0.0

   More information in /home/ec2-user/.heroku/error.log

```

In short, *anything* you try to do with the client will fail, until you do this again: `gem install json`. That will fix the problem.

In short, don't use `bundle clean --force`.
