# Tracking Changes

When working with remote repositories you must be mindful of the repository status. Ensure you make use of `git status` and `git log --oneline --graph --decorate --all`

![In this example, we see that the remote repository has an additional commit the local does not](../../../.gitbook/assets/screen-shot-2019-06-19-at-11.49.23-pm%20%281%29.png)

The image above is a visual of the mental model you need to be mindful of. Depending on how you are working with your remote repository, `git pull origin master` and `git push origin master` are commands you will use often.

{% hint style="info" %}
Remember **origin** is the shortname that refers to the location of the repository. The location being the url that refers to the physical location your code is housed.
{% endhint %}

### Pulling Changes with `git pull`

In the event illustrated above, a `git pull origin master` would be needed to sync the remote with the local repository.

{% hint style="info" %}
git pull is really 2 commands - it fetches \(or pulls in the changes from target branch\) and merges them into current branch 
{% endhint %}



