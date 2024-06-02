# git diff Command

---
This command will help to find differences between the content of a particular file or all files

* `git diff <filename>`: difference in File Content between Working Directory and staging Area
* `git diff HEAD <filename>`:It shows the differences between working copy and last commit copy.
* `git diff --staged HEAD <filename>`: It shows the differences between staged copy and last commit copy.
* `git diff <comitID> <filename>`:To see the difference in File Content between specific Commit and Working Directory Copy
* `git diff --staged <comitID> <filename>`:To see the difference in file content between specific commit and staging area copy
* `git diff <commitID1> <commitID2> <filename>`:To see the difference in File Content between 2 specified Commits
* `git diff HEAD HEAD^ <filename>`:To see the difference in File Content between Last Commit and Last butone Commit
* `git diff <commitID1> <commitID2>`:To see the differences in all Files Content between 2 specified Commits
* `git diff master <branchname>`:To see the differences in Content between 2 Branches
* `git diff <localbranch> <remotebranch>`:To see the differences in Content between Local and Remote Repositories
* 
>[!NOTE]
>
> * `---` means missing lines in staged copy
> * `+++` means new lines added in working directory version