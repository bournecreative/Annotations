# Remote

## Remote Repository

A remote repository is the same Git repository on our local, but is exists somewhere remote ;\). Once a remote repository has been configured to your local repository, the following command will identify where your remote exists. 

```text
git remote -v
```

But it appears I am getting ahead of myself.  Setting up a remote repository is pretty straightforward but i want to high light one of the steps.

```text
git remote add origin [url location]
```

**This command is used when setting up a local repository to push to an existing repository**

{% hint style="info" %}
When we break the command apart we see that we are "**adding**", the "**remote**'" "**location**". **Origin** is the short name that we will reference to refer to our remote location. We could substitute any other word for origin but its standard naming convention to refer to the main repository.
{% endhint %}

