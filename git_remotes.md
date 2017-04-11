---
title: "Remotes"
---

### Synchronization between local and remote master branches.
The goal is to fetch changes on the remote master branch and place local commits at the top of the tip.
```
git co master
git fetch origin
git rebase origin/master
```

### Track local feature branch
If you already have a local feature branch `dev`, you first check it out:
```
git checkout dev
```

Next, you want to push the `dev` branch to the remote:
```
git push -u origin dev
```

[Source](http://stackoverflow.com/a/29847192/2323832)


### Delete feature branch on remote
You want [delete](http://stackoverflow.com/a/2003515/2323832) the feature 
branch `dev` on the remote:
```
git push origin --delete dev
```

Propagate this on other machines using:
```
git fetch --all --prune
```

Then, delete its local counterpart:
```
git branch -d dev
```

### Synchronization between local and remote feature branches.
The goal is to fetch changes from the remote and then push the changes from the local feature branch to the remote feature branch without affecting the remote master branch.
http://stackoverflow.com/q/820178/2323832
```
git co feature_branch
git fetch origin
git config push.default current
git push origin feature_branch
```
