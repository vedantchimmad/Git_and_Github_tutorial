# Working Directory, Staging Area and Local Repository

---
* `git init`:This command will provide empty repository for our working directory, so that version control is applicable for our workspace.
>[!NOTE]
> 1) If our working directory contains any files, then these files won't be added to the local repository bydefault, we have to add explicitly. 
> 2) If our working directory already contains local repository(.git), still if we call git init command, then there is no impact.

### Configuring users into git
* `git config --global user.email "vedantchimmad@gmail.com"` : To add global user mail
* `git config --global user.name "vedantchimmad"`: To add global username
* `git config --list`: To list out all the configration available 
>[!NOTE]
> 
>global means these configurations are applicable for all repositories created by git. If we are not using global then it is applicable only for current repository.
### Adding to staging Area and then commit:
* `git status`: to check the status of files in Working Directory
* `git add <filenames>`: TO move files into staging area
* `git rm --cached <filenames>`: To un stage into Working directory
* `git commit -m "Message name"`: To commit the changes into local repository 
* `git log`: To check the fast commit in branch repository 
* `git restore <file>...`: To discard changes in Working directory
* `git commit -a -m "commit msz"`: Combine add and commit in single command
* `git ls-files`: This command will listout all files which are tracked by git.

