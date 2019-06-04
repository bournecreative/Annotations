# Overview of Git Workflow

## Visualizing the Git Workflow

Once we initialize a folder with the "_**init git**_" command, git begins watching the files in our local directory or "**working directory**". The working directory is the actual directory on your local machine you are working out of. Files that reside in your working directory are not yet "_**tracked**_" by Git.

The following illustration will help us visualize the less physical spaces our files will be pushed through during the Git workflow.

![git workflow](../.gitbook/assets/screen-shot-2019-03-28-at-10.06.33-pm.png)

Changes made within the working directory as not yet "tracked" until they are added to the "staging area or staging index". Say we created 3 files within our working directory and ran `git status.` 

Git would would highlight those files in red, indicated the files are "_**untracked**_" and provide some dialog regarding your options.

```text
git add [file name.ext] // you can target specific files and move to Staging Area

git add . // will target all files and move to Staging Area
```

Running git status again will highlight your new files in green, indicating these files are being "_**tracked**_" now and have been "_**staged**_". Committing these changes will group these newly added files, updates, or deletions with this current commit within the commit history.

```text
git commit
// ensure you have configured you bash terminal to open in a code editor or
// this command will open Vimm. Enter message and description for commit

or 

git commit -m "commit message" // use the -m flag or message flag. This method does not 
                               // allow you to provide a description for the commit,
                               // only the message
```

Once changes are committed, we can view them in the commit history using

```text
git log // See Viewing Commits section for more info on this.
```

#### Writing clear commit messages

Its important you improve the patterns and detail of your commit messages. Doing so will improve readability and make your commits more useful.

{% hint style="info" %}
Commits should apply to a single focus. Commit often and do not pollute commits with unrelated changes. 
{% endhint %}

{% hint style="info" %}
**The goal is that each commit has a single focus.**

\*Keep each commit short \(less then 60 characters\)

To ensure your commits are helpful, try using this phase:

This commit will...&lt;commit message&gt;

Also helpful is to write your commit messages with clarity
{% endhint %}

### Seeing changes that have not yet been committed

Changes that have not yet been committed are "_**untracked"**_. If we are working on a project and want to see _**what changes have been made but not yet committed**_, this command will be especially helpful.

```text
git diff // will highlight the difference in changes not yet tracked
```

### Remote

Based on the illustration at the top of the page, we have moved our files from the "**Staging Index"** all the way to the "**Repository**". Pushing to the remote requires that we make use of GitLab, GitHub or Bitbucket so we can push our local changes to a remote location were we can share our code publicly or with specific teams.

