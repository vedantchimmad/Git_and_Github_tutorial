# Git reflog

---
We can use git reflog command to display all git operations what ever we performed on local repository
* `git reflog`:It will show all git operations performed on local repository related to that particular branch with commit id.
* `git reset --hard <commit-id>`: we can recover running this command 
>[!NOTE]
>
>*  reflog will maintain 90 days git operations history bydefault
>* We can use reflog command to go to specific state of the repository.
>* By mistake if we did any unwanted destruction operation( like git reset --hard), still we can recover by using git reflog command.