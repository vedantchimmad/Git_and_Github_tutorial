# git checkout

---
We can use checkout command to discard unstanged changes in the tracked files of working directory.

* `git checkout -- <filename>`:It will discard any unstaged changes made in file1.txt.After executing this command, staged copy content and working directory content is same.
* `git checkout`: To discard changes in all tracked files of working directory.
* ``

>[!NOTE]
>
> * git checkout is applicable only for the files which are already tracked by git. It is not applicable for new files.
> * git checkout command can be used in branching also.
