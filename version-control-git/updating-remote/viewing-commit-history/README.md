# Viewing Commit History

## Filtering Collaborator commits

```
git shortlog
```

We cam quickly see collaborators and a commit summary

Flags can be amended to the command to provide more clarity. 

`-s` shows the number of commits.  `-n` sorts the commit history numerically by commit count rather then by author name

```text
git shortlog -s -n
```

You can also target commits by a specific author

```text
git log --author=authorName //use quotes for multiple words
```

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}



