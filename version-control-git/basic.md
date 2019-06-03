---
description: Everyday commands
---

# Viewing Commits

### Reviewing past changes

List commits. Press "_**k**_" key _****_to exit. Use the "_**up**_" and "_**down**_" arrows to scroll the output.

* "_**d**_" key will scroll down half a page
* "_**u**_" key will scroll up half a page

```text
git log
```

* commit SHA
* Author
* Date
* Commit message

#### We can alter the information displayed by git log in a more terse presentation using

```text
git log --oneline
```

* first 7 characters of commit SHA
* Commit message

#### We can show more details regarding the changes, 

```text
git log --stat
```

* git log content 
* list files modified
* list the number of lines that were added or removed
* summary of files changed

#### We can drill down even more and list the actual changes that occurred using the --patch flag

```text
git log -p
```

The patch output highlights deleted information in "red" and added information in "green"

{% hint style="info" %}
git tracks line changes even with whitespace. This is usually not relevant especially when you are searching for actual changes. We can display the changes while ignoring 'white space' 
{% endhint %}

Adding the white space flag will ensure whitespace is not included in the displayed changes.

```text
git log -p -w 
```

### Searching for a Specific Commit

Rather then list out all the commit history, we can list specific commit history by providing the SHA of the commit. 

{% hint style="info" %}
The commit history listed starts with the commit listed rather then starting from the most recent commit. 
{% endhint %}

```text
git log -p fdf5493
```

Listing only the information for a specific commit - nothing else

```text
git show fdf5493
```

Remember that we can add multiple flags and use combinations of these commands to get what we need. A cool combo to quickly find the commit you are looking for my description is

```text
git log --oneline

//identify the commit you would like to see more of

git show commitSHA --stat //for a summary
// or
git show commitSHA -p // for actual changes  
```

