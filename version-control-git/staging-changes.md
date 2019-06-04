# Git add and more

## Staging Changes

As illustrated in the Overview of Git Workflow, we need to move pages from our "_**working directory"**_ into the "_**staging index"**_ so git can _**"track"**_ the files.

```
git add [target file]

// you can alos add multiple files in one go
git add [target file] [target file] [target file] [target file]

// will target all pages where changes have occured
git add . 
```

### Ignoring files on purpose

What if we purposely wanted to ignore and not include specific files in our repository?

#### .gitignore file to the rescue

Adding a .gitignore file to the root of our working directory will allow us to ignore specific file types or directories.

```text
//within our .gitignore file we can simply list the directory to disinclude

node_modules

```

We can also use a method known as Globbing to match patterns to identify specific file types or directories you wish to not include.

* blank lines can be used for spacing
* `#` - marks line as a comment
* `*` - matches 0 or more characters
* `?` - matches 1 character
* `[abc]` - matches a, b, \_or\_ c
* `**` - matches nested directories - `a/**/z` matches
  * a/z
  * a/b/z
  * a/b/c/z

The following is an example to illustrate how we could ignore all jpgs within the imgs folder

```text
imgs/*.jpg
```

### Un-Staging Changes

In the event we adding a file to the staging index as unintended consequence, we can undo this mistake using the `git rm` command

```text
git rm --cached <file>
```



