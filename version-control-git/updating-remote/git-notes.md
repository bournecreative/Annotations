---
description: >-
  This information is typically displayed when you create a repository without
  auto generating a README.md
---

# Creating a Remote

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

