# Git

## Reduce local disk size

To delete all the local references of the remote branch

`git remote prune origin`

Packs are used to reduce the load on disk spaces, mirror systems, etc.

`git repack`

This command will help you to reduce extra objects that are already present in the pack files. This will help you to reduce the size of the pack file itself.

`git prune-packed`

Git has a feature called reflog that helps to track Git refs in the local repo. Git has an internal garbage collection mechanism to remove old refs in Git. But there is also a manual mechanism to remove old refs.

`git reflog expire --expire=1.month.ago`

Garbage collection. This command will help Git to remove unwanted data in the current repo (but it's quite slow).

`git gc --aggressive`

Combining all command

`git remote prune origin && git repack && git prune-packed && git reflog expire --expire=1.month.ago && git gc --aggressive`