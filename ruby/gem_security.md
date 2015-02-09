#Gem Security
#####by Mike Holloway

##Where are gems installed from?
RubyGems come from open source communities, typically RubyGems.org, a package manger that comes with Ruby. Other repositories exist online, but RubyGems is far and away the most used.
##How do members of the Ruby community make sure they're installing a gem from an "official" source?
To quote the RubyGems.org FAQs, when it comes to trusting gems, "ultimately, you can't." The page recommends only using gems that are known to be good and even performing your own security audits.

On January 30, 2013, RubyGems.org itself was compromised using malicious code execution by a gem. Such a gem could run code to infiltrate users' computers.

While there is a way to sign gems to know from who they've come, very few people utilize this feature. Some bloggers have suggested that users be forced to sign their gems before uploading in order to know the source of malicious gems. As RubyGems.org notes, it is currently neither easy for developers to do so nor is it transparent for users. It has also been suggested that gem users be notified of unsigned/insecure gems. Several people noted that people trust gems simply "because they usually work."

Security steps can be taken, including installing gems with "trust policies" that limits gems only to signed and verified gems. RubyGems also depends on users to report potential new security vulnerabilities by contacting creators and letting them know about issues in their work.
##What does it take to submit an "official" gem that others can easily install?
While anybody can create private gems to use for themselves, you might want to publish it for the world to use. This means signing up for a RubyGems.org account by registering a username and password. These will be used to push the gem:

>$ gem push squid-utils-0.1.0.gem
>Enter your RubyGems.org credentials.
>Don't have an account yet? Create one at https://rubygems.org/sign_up
>   Email:   gem_author@example
>Password:
>Signed in.
>Pushing gem to RubyGems.org...
>Successfully registered gem: squid-utils (0.1.0)

And that's pretty much it. You can see why it's hard to know which gems are really safe to use out there.

###Sources
http://guides.rubygems.org/faqs/
http://en.wikipedia.org/wiki/Ruby_on_Rails
http://guides.rubygems.org/publishing/
http://cristianobetta.com/blog/2013/02/02/ruby-gems-are-not-safe-to-use/
https://gemfury.com/blog/2013/rubygems-vulnerability
https://www.honeybadger.io/blog/2013/06/25/stop-using-rubygemsorg-in-production