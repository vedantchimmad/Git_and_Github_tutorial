# Git Log Command

---
If we want to see history of all commits in local repository, then we have to use git log command.

* `git log`: To see all the git commit 
* `git log <filename>`:To see log information for particular file

## Options are available for git log command
* `git log --help`: To see all the available option for git log
* `git log --oneline`: to see all the commit in line with 7digit id and commit msz
* `git log -n <number>`: To limit the git log in descending
* `git log --grep="pattern"`: It shows all commits which has given pattern in the commit message.
* `git log --since=<date>`:Show commits more recent than a specific date
* `git log --until=<date>`:Show commits older than a specific date.
* `git log --author=<pattern>`:Show commits based on Author
* `git log --decorate --oneline`:This option will print some extra information like branch information,head information, tags information etc
* `git log --oneline --graph`: used to see the commits in graph
>[!NOTE]
>
> we can use -n and --oneline options together also.
>* git log -n 2 --oneline

| Fast-forward                                                                                                                                           | Three-way Merge                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| After creating child branch, if updates are available only in the child branch but not in the parent branch, then GIT will perform Fast-Forward Merge. | After creating child branch, if updates are available in both Parent and child branches, then GIT will perform Three-way Merge. |
| It does not require any additional commit                                                                                                              | It requires a new commit which is also known as Merge commit.                                                                   |
| There is no chance of conflicts because new commits are available only in child branch but not in parent branch                                        | There may be a chance of conflicts because new commits are available in both parent and child branches.                         |
| Fast-forward merge is fully handled by GIT.                                                                                                            | If there is a conflict, we may required to handle manually.                                                                     |

### Merge Conflicts
In the case of 3-way merge, if the same file updated by both Parent and child branches then may be a chance of merge conflict.
* If there is a conflict then GIT stops the merge process and provides conflict message.
* We have to resolve the conflict manually by editing the file.

### Delete a Branch
The main objective of deleting branch is to keep our repository clean.
* Deletion of the branch is optional.
* `git branch -d <branch_name>`:used to delete feature branch

### Merging By using Rebase
Rebase is alternative way to merge changes of two branches togther
#### Process of rebasing: It is a two step process.
**Step-1:** We have to rebase feature branch on top of master branch.
1. Checkout feature branch 
   * `git checkout feature` 
2. Rebase feature branch on top of master branch 
   * `git rebase master`

**Step-2:** We have to merge feature branch into the master branch(fast-forwar merge will be happend)
1. checkout master branch 
   * `git checkout master` 
2. Merge feature branch into master branch 
   * `git merge feature`

### Advantages of rebasing: 
1. Rebase keeps history linear.
2. Clear work flow (Linear) will there. Hence easy to understand for the developers. 
3. Internally git performs Fast-forward merge and hence there is no chance of conflicts. 
4. No extra commit like merge commit.
### Disadvantages of rebasing: 
1. It rewrites history. We cannot see history of commits what we did in feature branches 
2. We does not aware which changes are coming from which branch.

| Merge                                                                 | Rebase                                                      |
|-----------------------------------------------------------------------|-------------------------------------------------------------|
| It is a single step process `git checkout master` `git merge feature` | It is a two-step process                                    |
| Merge preserves history of all commits                                | Rebase clears history of feature branch                     |
| The commits can have more than one parent and history is non-linear   | Every commit has only one parent and history is linear.     |
| In merge, there may be a chance of conflicts.                         | In Rebase, there is no chance of conflicts.                 |
| We can aware which changes are coming from which branch.              | We can not aware which changes are coming from which branch |
| We can use merge on public repositories                               | It is not recommended to use rebase on public repositories. |