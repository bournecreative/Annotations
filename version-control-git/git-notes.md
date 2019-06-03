# Starting a Git Repository

### Clone a repository

```
git clone [repository-address.git]
cd new_folder
touch README.md
git add README.md
git commit -m "initial commit"
git push -u origin master

```

### Create via existing folder 

```
cd existing_folder
git init
git remote add origin [repository-address.git]
git add .
git commit -m "initial commit"
git push -u origin master
```

### Create via existing repository

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

### Pull an active Pull Request down as a branch onto your local

Modify your git config

```text
[alias]
prstash = "!if() { git fetch upstream
refs/pull-requests/$1/from:pull-requests/2: } ; f"
```

Now from bash

```text
git prstash # nameOfBranch
```

The \# is the pull request number and what follows is the branch name. This information can be sourced from the actual pull request url

Once you are complete reviewing you can also delete all branches created with git pr

```text
git pr-clean
```

