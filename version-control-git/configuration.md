---
description: Getting up and running with Git
---

# Getting Started

## Configuration of Terminal color

Update your bash profile. Look for the _**.bash\_profile**_ file_**.**_ Copy the following into it.

```text
# colors!
red="\[\033[38;5;203m\]"
green="\[\033[38;05;38m\]"
blue="\[\033[0;34m\]"
reset="\[\033[0m\]"

```

Update your git config file

```text
# sets up Git with your name
git config --global user.name "<Your-Full-Name>"

# sets up Git with your email
git config --global user.email "<your-email-address>"

# makes sure that Git output is colored
git config --global color.ui auto

# displays the original state in a conflict
git config --global merge.conflictstyle diff3

git config --list
```

Configure Git to work with your code editor

```text
git config --global core.editor "code --wait"
```

