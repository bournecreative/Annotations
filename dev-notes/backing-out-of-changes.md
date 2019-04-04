# Backing Out of Changes

## Git Stash

Sometimes you are working in the wrong branch and realize it right when you need to commit your changes. We can use git stash to record the current state of the working directory and go back to a clean working directory.

```
git stash
```

We can then create a new branch and apply the changes

```
// See the array of stashs 
git stash list
// Apply the specified stash - most recent stash is at [0]
git stash apply[0]
// Remove all stash entries
git stash clear 
```

{% embed url="https://git-scm.com/docs/git-stash" %}



