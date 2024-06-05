# Remote Repositories

---
### The Advantages of Common Remote Repositories: 
1. On the developer's machine, we are not required to install GIT server. GIT Server is available on common remote repository. 
2. Developer should aware only url of the common remote repository and he is not required to aware all hostnames and port numbers of all remaining developer's machines

>[!NOTE]
>
> 1. The max allowed file size in Github public repository: 100MB 
> 2. The max allowed repo size in Github public repository: 2GB

* `git remote add <alias_name> remote_repository_url`:We can use git remote command to configure remote repository to our local repository with alias name
* `git remote`:It just provides the alias names of remote repositories
* `git remote -v`:It provides remote repository urls also
* `git push <remote_name> <branch_name>`:to send our changes from local repository to remote repository.
* `git clone <remote_repo_url>`: used to clone the remote repo into local repo
* `git fetch origin <branchName>`:check whether any updates available at remote repository or not.
* `git pull <remote> <branch>`:merge updates from remote repository into local repository.
* 