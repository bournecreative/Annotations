# Committing and more

We covered the purpose of committing and how to execute commits in the [Overview of Git Workflow section](../overview.md)

```text
git commit
// ensure you have configured you bash terminal to open in a code editor or
// this command will open Vimm. Enter message and description for commit

or 

git commit -m "commit message" // use the -m flag or message flag. This method does not 
                               // allow you to provide a description for the commit,
                               // only the message
```

### Are Commits forever?

We have seen that once we add and commit changes, the changes are added to the repository history and associated with the commit/SHA created and associated with that message. How might we back out of a commit if changes are committed that were not needed.

