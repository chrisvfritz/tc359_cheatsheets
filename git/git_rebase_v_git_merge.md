# Git Rebase vs. Git Merge

`git rebase` and `git merge` both accomplish the same act, but do so in different ways.  Both of the commands integrate the changes from one branch into another branch.

## What is `git merge`?

When using the `git merge` command, a merge commit is made to link the repo you are in with the one that you are merging into.

`git merge` can be invoked as follows:

``` bash
git checkout feature
git merge master
```

We are checking out the feature branch and merging INTO the master branch.

## What is `git rebase`?

`git rebase` does not create a merge commit.  Instead, it moves all of the commits of the branch that you are in onto the end of the commits of the branch that you are merging into.  The commits that are moved are actually re-written so that they can be put on the end of the branch being merged into.

`git rebase` can be invoked as follows:

``` bash
git checkout feature
git rebase master
```

We are checking out the feature branch and MOVING it to the tip of the master branch's log of commits.

Rebasing makes the project history much more clean because there are no merge commits in the changelog for the project.

Merging shows more project history so that developers can more easily see when merges took place and features were added.

An interactive rebase, which can be created by using the `-i` option, allows the developer doing the rebase to modify the re-written commits by giving them commit messages or reordering the commits.

The golden rule of `git rebase` is to never use it on public branches.  If you do, other developers will be working on a different version of the branch that you rebased.  Then you will need to merge the different versions of the branch together to get everything back to normal.