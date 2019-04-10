# Updating

### Fetch vs pull

The git fetch command downloads commits, files and refs from a remote repository into your local repo but does not merge them into your repository. 

```text
git fetch
```

{% hint style="info" %}
Git isolates fetched content as a form of existing local content that has no effect on your local development work. Fetched content must be explicitly checked out.
{% endhint %}

### git pull = git fetch + git merge

Brings the local branch up-to-date with its remote version

#### Workflow Scenario

You are working on a task and learn there are upstream changes that impact your work. You attempt a git pull but cannot execute because there are conflict. 

```text
git pull
...fails because of conflict

git stash // save your work
git pull
git stash pop /git stash apply
```



