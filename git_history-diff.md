---
title: "History/Diff"
---

### Commit history
Get the commit history for a single branch
```
git log branchA..
```
Get the commit history for a single file
```
git log -- [/path/to/file]
```

### Branch comparison
#### Compare commits between two branches.
The following code will answer the question, which commits have been made on `branchB` that are not yet part of `branchA`.
```
git log --oneline branchA..branchB
```

#### Compare contents between two branches.
The following code will answer the question, which changes have been made on `branchB` compared to `branchA`.
```
git diff branchA..branchB
```

### See which files were part of a particular commit
```
git diff-tree --no-commit-id --name-status -r <commit-id>
```

### Diff between files from different commits
```
# Set-up git as your merge tool
git config --global merge.tool vimdiff
git config --global diff.tool vimdiff
git config --global merge.conflictstyle diff3
git config --global mergetool.prompt false

# Run a vimdiff on two files from different commits
git difftool <sha-id>:/path/to/file <sha-id>:/path/to/file
```

### Display a file from an old commit with the text editor of your choice
```
# Note the dash at the end of the command, which is required
git show <sha-id> | <text-editor> -
```
