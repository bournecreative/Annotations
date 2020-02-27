# Removing Working Directory Changes

In the event changes have been made and you have decided that these changes are not to be moved forward with, we need to discard the changes. At this point we understand we are in the "**Working Directory**" and will not `add` and `commit` these changes to the current branch.

![We are in the working directory.](../.gitbook/assets/screen-shot-2019-03-28-at-10.06.33-pm.png)

Discard local changes permanently  to a file

```
// discard local changes to a targeted tracked file

git checkout -- <file name>

// discard local changes to all tracked files

git checkout .

```

Discard local changes permanently  to any tracked files.

```
git reset --hard
```

Remove all untracked files/directories in addition to untracked files.

```text
git clean -f -d
```



