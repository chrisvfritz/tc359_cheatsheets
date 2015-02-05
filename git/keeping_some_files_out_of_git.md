# Keeping some files out of Git

There are some files, like log files or OS X's automatically generated `.DS_Store` files, that we just don't ever want in our Git repositories. Fortunately, there's a simple way to blacklist certain files and folders from ever being committed into your repository!

## The `.gitignore` file

If there's a `.gitignore` file in the root of your project, Git will read it to keep track of the kinds of files it should ignore. Makes sense, right? So let's say for example, that you never want to keep track of any file called `.DS_Store`. Just add this line to `.gitignore`:

```
.DS_Store
```

And what if you never want the `tmp` or `logs` directories - or anything in them - in your Git repo? Just add these lines:

```
tmp
logs
```

## Removing files already in your Git repo

Unfortunately, any files that you've already committed to your Git repo will still be there. For an example, to get rid of any `.DS_Store` files already committed to your repo, you can run a command like this from the root of your project:

``` bash
find . -name '.DS_Store' -print0 | xargs -0 git rm -f --ignore-unmatch
```

That finds all the files called `.DS_Store` and removes them from your repo (while keeping them on your computer).
