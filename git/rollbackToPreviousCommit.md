Once upon a time, when the semester was winding down and a certain project was coming to completion I ran in to this problem. 
There I was just pushing along and getting some real work done on my project when BOOM! whole directory was trashed.
A few hours later and I was back to working on a valid working commit.

##### DISCLAIMER: Do not attempt unless you know what you're doing or everyone is aware as bad things CAN happen.

If you wish to roll back to a certain commit the following is how you might wish to complete it

1. Run ```git log```
  
  This will get you a nice commit history so if you know of a working commit, you can go back to that
  For example this is what it may look like 
  
  `commit b8a9090203713c6aed315ecca6bc8cd47f3c503a`
  
  `Merge: 4265f3b 0887b9b`
  
  `Author: `
  
  `Date:   Mon Feb 2 15:55:27 2015 -0500`
  
  `Merge branch 'master' of https://github.com/chrisvfritz/tc359_cheatsheets`
  
Then do something along the lines of the [following](http://stackoverflow.com/questions/4114095/revert-to-a-previous-git-commit) 
which is a fantastic link, I could give you a set in stone method, but every situation is different. Happy rolling back! Be careful!



  

