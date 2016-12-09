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

### Synchronization between local and remote feature branches.
The goal is to fetch changes from the remote and then push the changes from the local feature branch to the remote feature branch without affecting the remote master branch.
http://stackoverflow.com/q/820178/2323832
```
git co feature_branch
git fetch origin
git config push.default current
git push origin feature_branch
```
