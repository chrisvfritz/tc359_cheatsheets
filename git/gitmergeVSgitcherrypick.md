# Git Merge vs. Git Cherry-Pick 
- Using git merge you can add branched commits back to the master branch.
- Using git cherry-pick you can apply the changes from one or more existing commits and recording a new commit for each one

## When to use Merge or Cherry-Pick
- Use Git Merge on a regular basis when merging a branch back to another to add the new commits to the other branch.
- Use Git Cherry-Pick when you have to use code that exists in a remote branch which is really out of date. This way you can add each commit individually since the branch was created.

## Documentation
Git Merge: http://git-scm.com/docs/git-merge
Git Cherry-Pick: http://git-scm.com/docs/git-cherry-pick

## Examples
Git Merge: http://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
Git Cherry-Pick: http://wiki.koha-community.org/wiki/Using_Git_Cherry_Pick