# Git reset

---
Changes already added to staging area, but if we don't want to commit, then to remove such type of changes from staging area, then we should go for git reset.
* It is opposite to git add command.
* `git reset <filename>`:The file won't be removed from staging area, but reset to previous state

>[!NOTE]
> * `git reset <filename>`: To ignore changes in staging area 
> * `git checkout -- <filename>` To ignore changes in working directory

### To undo Commits at Repository Level
```commandline
Syntax: 
  git reset <mode> <commitid>
```
* Moves the HEAD to the specified commit, and all remaining recent commits will be removed.
* mode will decide whether these changes are going t0 remove from staging area and working directory or not. 

## The allowed values for the mode are: 
* --mixed 
* --soft 
* --hard 
* --keep 
* --merge

### 1. --mixed Mode:
* To discard commits in the local repository and to discard changes in staging area we should use reset with --mixed option.
* It is the default mode.
* It won't touch working directory.
* After undo commit changes will be there in working directory,To discard changes in working directory `git checkout -- filename`
>[!NOTE]
> 
> To discard commit-3: 
> * git reset --mixed <commitID> 
> * git reset --mixed HEAD~1 
> * git reset HEAD~1

### 2. --soft Option:
It is exactly same as --mixed option, but changes are available in working directory as well as in staging area.
* The commits will be discarded only in local repository, but changes will be there in working directory and staging area
* `reset --soft HEAD~1`:To discard the latest commit
#### Use Cases: 
1) If some files are missing in the last commit, then add those files and commit again. 
2) We forgot to add defect number in commit message.

### --hard option:
It is exactly same as --mixed except that Changes will be removed from everywhere (local repository,staging area,working directory)
* It is more dangerous command and it is destructive command
* `git reset --hard HEAD~2`: It removes recent 2 commites permanently 
>[!NOTE]
> * If the commits are confirmed to local repository and to discard those commits we can use reset command. 
> * But if the commits are confirmed to remote repository then not recommended to use reset command and we have to use revert command.