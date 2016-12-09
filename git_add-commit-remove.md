---
title: "Add/Commit/Remove"
---

### git-add
#### add all untracked files to the staging area
```
echo -e "a\n*\nq\n" | git add -i
```
http://stackoverflow.com/a/7446711/2323832

#### remove all staged files from the staging area
```
git reset HEAD
```

#### add only modified files to the staging area
```
git add `git status | grep modified | sed 's/\(.*modified:\s*\)//'`
```
http://stackoverflow.com/a/22437750/2323832


#### remove a particular file from the staging area
```
git reset HEAD <filename>
```

### git-rm
#### Add all deleted files to the staging area
```
git rm `git status | grep deleted | awk '{print $3}'`
```
http://tylerfrankenstein.com/code/how-git-rm-all-deleted-files-shown-git-status


### Undo a commit that has not been pushed to the remote, yet
```
git reset --soft HEAD^
```
http://stackoverflow.com/a/2941598/2323832


