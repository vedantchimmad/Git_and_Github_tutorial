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
>[!NOTE]
>
> we can use -n and --oneline options together also.
>* git log -n 2 --oneline
