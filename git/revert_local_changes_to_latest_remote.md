# Reverting local changes to latest remote (e.g. GitHub) -- Paul Stanos

## The 'git reset' command

The reset command is used when you want to reset the "HEAD" of your local repository to another position. By resetting the HEAD back to the same commit as the remote (e.g. GitHub), you effectively have a "clean slate".

## The '--hard' command option

By specifying '--hard' on your git reset command you tell Git that you want to discard any changes you made since the commit you are reverting to.
If you do not specify this option, the default will keep your changed files, which is not what you want to happen.

Note: untracked files (e.g. new files that are not currently tracked by Git) will not be discarded even when using --hard. You can manually delete them in Git Bash using 'git rm <file_name>' or by deleting them in Windows Explorer, Mac OSX Finder, or similar file management system on your OS. 

## Putting it all together

```
git reset --hard origin/<branch_name>
```

Running this command will reset your currently checked out branch to the remote repository's latest commit on the branch specified by <branch_name>.