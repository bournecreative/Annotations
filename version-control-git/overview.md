# Overview

## Visualizing the Git Workflow

Once we initialize a folder with the "_**init git**_" command, git begins watching the files in our local directory or "**working directory**". The working directory is the actual directory on your local machine you are working out of. Files that reside in your working directory are not yet tracked by Git.

The following illustration will help us visualize the less physical areas files are pushed through during the Git workflow.

![git workflow](../.gitbook/assets/screen-shot-2019-03-28-at-10.06.33-pm.png)

Changes made within the working directory as not yet "tracked" until they are added to the "staging area or staging index". 

```text
git add . // will move files to staging index
```

Changes are now ready to be committed. 

```text
git commit 

or 

git commit -m "commit message"
```

Once changes are committed, we can view them in the commit history using

```text
git log // See Viewing Commits section for more info on this.
```

