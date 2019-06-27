# Backing out of Commits

## Really...we can do this?

Yes, and there are a series of tools at our disposal for different scenarios.

### Alter the most recent commit

In the event we forgot to include a change or made a typo in the commit message

`git commit --amend`

#### How it works

You can run this command if your working directory is clean and there are no uncommitted changes.

* Edit the files or add files if you missed changes
* Save the files
* Stage the files
* Run `git commit --amend`

### Reversing the changes of a commit

In the event we want to revert the changes of commit. In other words, we are literally reversing the changes made by a particular commit.

`git revert <SHA of the commit we are targeting to revert>`

#### How it works

* Use git log to identify the commit you want to revert
* `git revert SHA of commit`

{% hint style="info" %}
Note that this command creates a new commit in the commit history
{% endhint %}

### Git Reset 

{% hint style="danger" %}
Danger! Use with caution since you are literally removing commits from the repository.
{% endhint %}

In this scenario, we are removing commits from the git commit history. Because of this, we must use this command with caution.

### In the event a commit is removed but thats really not what we wanted

This scenario should be avoided at all costs. In the event a mistake is made, `git reflog` can be used to retrieve a history that is deleted ~ for about 30 days.

{% embed url="https://git-scm.com/docs/git-reflog" %}

### 

