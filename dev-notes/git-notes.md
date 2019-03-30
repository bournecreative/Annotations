# Git Notes

## Ways to create a repo

Create a new repository:

```
git clone [repository-address.git]
cd new_folder
touch README.md
git add README.md
git commit -m "initial commit"
git push -u origin master

```

Create via existing folder:

```
cd existing_folder
git init
git remote add origin [repository-address.git]
git add .
git commit -m "initial commit"
git push -u origin master
```

Create via existing repository

```text
cd existing_repo
git remote rename origin old-origin
git remote add origin [repository-address.git]
git push -u origin --all
git push -u origin --tags
```

{% hint style="warning" %}
Remember to ensure your git config reflects the email address associated with your GitHub account otherwise contributions will not be reflected in profile contributions graph.

[https://help.github.com/en/articles/why-are-my-contributions-not-showing-up-on-my-profile](https://help.github.com/en/articles/why-are-my-contributions-not-showing-up-on-my-profile)
{% endhint %}

Ensure your config is up to dated with the correct info

```text
git config --global user.name "user name"
```

```text
git config --global user.email "user email address
```

### Stages of Changes

![Git workflow cycle](../.gitbook/assets/screen-shot-2019-03-28-at-10.06.33-pm.png)

#### Local \| Working Directory

Files that have not been added or staged. These are known as untracked files.

#### Local \| Staging Area

Files that have been added for a commit.

#### Local \| Repository

Files that have been staged and committed.

#### Remote

Files that have been added, committed and pushed to your remote repository

### Listing Tracked Files

List the tracked files within a repository

```text
git ls-files
```

### Backing out of Untracked Changes

In the event you have made changes that have not been added or committed and you no longer wish to keep such changes

```text
git checkout -- .
```

```text
git checkout -- path/filetorevert
```

### Working with Forks

When a repository is forked that you plan to submit pull requests to you must ensure you update the upstream url.

You should have forked the repo in question, cloned it your machine. 

```text
git remote add upstream [original_repository_url]
```

```text
git remote -v
```

You should conform that the **origin** urls for _fetch_ and _push_ are pointing to your remote repositories while _fetch_ and _push_ of **upstream** are pointing to the original repository git address

### Deleting Branches

delete a local branch - you must not be in the branch

```text
git branch -D [branch_name]
```

delete a remote branch

```text
git push origin --delete [branch_name]
```

