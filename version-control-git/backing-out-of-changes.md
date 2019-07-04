# Saving for Later - Git Stash

Sometimes you are working in the wrong branch and only realize this after the fact. How can you save your work and transfer your work to the correct branch? Git Stash to the rescue. _**Git Stash**_ can record the current state of the working directory and go back to a clean working directory.

```
git stash
```

We can then create a new branch and apply the changes

```
// See the array of stashs 
git stash list

// Apply the specified stash - most recent stash is at [0]
// If no specific stash is specified, position 0 is used
git stash apply

// example of inserting specific array index
git stash apply stash@{2} 

// Remove all stash entries
git stash clear 

// pop is the same as apply but immediately drops from the stash stack
git stash pop

```

{% hint style="info" %}
Git stash does not save untracked files
{% endhint %}

Will stash everything - ignored files and untracked files

```text
git stash --all
```

Will stash everything except ignored files \(_git 2.16.2_\)

```text
git stash --include-untracked
```

{% embed url="https://git-scm.com/docs/git-stash" %}

{% embed url="https://git-scm.com/book/en/v1/Git-Tools-Stashing" %}

