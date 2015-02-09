#epicGit()

Using bash functions it is possible to string multiple git commands together into a single epicGit function. It's a bit different from an alias since an alias is just another name for a single command.

When using bash(terminal) you can create a function to chain multiple commands together. Here we'll walk through setting up a simple function that will do four git commands in a single line.

After you have cloned a repository on github.com or after setting up the origin remote for a repository you have initialized on your local machine automating the push process is a breeze.

All you need to do is go into terminal and define this function

```
epicGit(){
	git add .
	git commit -m "$1"
	git push origin master
	git status
}
```

The "$1" will allow you to call the function epicGit with a string argument that will be the commit message.

You can use this by typing

```
epicGit "I'm pushing this to github using an awesome function I wrote"
```

If everything goes according to plan you should see a few lines of change notifications, a few lines of writing the changes, and a nice "nothing to commit, working directory clean" message.

You can also make changes to the function like including the -A flag in the git add command in order to also delete the files you have removed from the project.

Or you could use another git pull command before the push command to make sure nothing in the github.com repository has changed since your last pull. Very useful if you're working one project on multiple computers or working with other people on the same project to insure your new code won't conflict with the code that is already published.

##Other Bash Uses
Using bash you are also able automate a lot of other things. For instance if you were ever sick cd using the cd command to move around the file system you could make a command to automatically move you to the project you want. You could create a function that moves you into a directory so you don't have to remember exactly where everything is.

If you write a function that first uses "cd ~" you can get the function to take you anywhere in the file system from any starting location.

##Last Notes
Another thing to keep in mind when setting up bash functions is that unless you save your functions to the .bashrc file your functions will not be available to use after shutting down your terminal window or other bash interface. So open that up in your preferred text editor and have fun creating.
