---
title: "Branches"
---

### Merge specific file from one branch into another branch
Suppose that you have a development `dev` branch where you have made multiple commits since your last `checkout`. Now, you just want to merge a single file `file1.txt` into your `master` branch.
```
git checkout master
git checkout dev file1.txt
```
