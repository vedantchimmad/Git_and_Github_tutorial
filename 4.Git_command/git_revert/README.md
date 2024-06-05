# Git revert

---
git revert command won't delete commit history. It reverts the required commit by creating a new commit
* `git revert <commitid>`: revert the changes with new commit id
* `git revert -n`:revert the changes with no any comment 
* `git revert --continue`:if in case there is conflict fixed the conflict and run this command to continue the revert 
* `git revert --skip`: skip this revert patch
* `git revert --abort`:Cancel the revert operation in case of any conflict 