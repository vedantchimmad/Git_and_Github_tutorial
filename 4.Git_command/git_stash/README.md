# Git stash

---
Store (something) safely in a hidden or secret place
### What is git stash:
The git stash command takes our uncommitted changes (both staged and unstaged), saves in some temporary location
* After completing our urgent work, we can bring these stashed changes to our current working directory
* `git stash`: used to store current changes into temp location
* `git stash list`: to show the list of stash
* `git show stash@{0}`:to check the contents of stash
* `git stash pop stash@{0}`:It will bring stashed changes from temporary location to working directory.
* `git stash clear`: to delete all the stash 
* `
>[!NOTE]
>
> 1. Stashing concept is applicable only for tracked files but not for newly created files.
> 2. To perform stashing, atleast one commit must be completed

### Partial Stash
Assume we have multiple files, but we want stash only for some files. It is possible and this concept is called partial stash.
* `git stash -p: used to do partial stash
