# Merge Conflicts

## What causes a merge conflict

A merge conflict will happen when the exact same line\(s\) are changed in separate branches. 

### When a merge conflict occurs

You are notified that merge conflicts exist in the respective file\(s\). Open the file\(s\) and resolve the merge conflicts. You will manually need to decide which changes from each branch will kept.

Once the merge conflict is resolved. Save the file. Add the file\(s\) to the staging index and commit it just as usual. Remember, this merge will prompt you to supply a commit message but its common to just use the provided merge commit message.

### Indicators

When you are looking at the file with the merge conflicts you will see various indicators. This is what they mean.

**Head** refers to the current active branch

`<<<<<<< HEAD`  Everything below this, \(until the next indicator\) identifies what is on the current branch

`||||||| merged common ancestors` Everything below this line \(until the next indicator\) identifies what the original lines were

`=======` is the end of the original lines. Everything that follows \(until the next indicator\) is whats on the branch that's being merged.

`>>>>>>>>>> branchName` is the ending indicator of whats on the branch that's being merged in







