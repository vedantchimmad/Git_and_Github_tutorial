# Git Tagging

---
* Tag is nothing but a label or mark to a particular commit in our repository.
* Tag is static and permanent reference to a particular commit
* In general Tags can be used for release verions.

#### There are two types of tags 
1) Light Weight/Simple Tags 
2) Annotated Tags [Tags with Information]

### Light Weight Tag
* `git tag <tag_name>`:used to create light-weight tags
* `git tab --list`:used to list the tags
* `git tag -d <tagname>`:used to delete the tag
#### Limitation of LightWeight Tags:
LightWeight Tag is simply text reference to the specified commit. It won't maintain any information like tagger name, date of creation, message etc.

### Annotated Tags
Annotated Tag is exactly same as Light weight tag except that it maintains information like tagger name, date of creation, description etc.
* `git tag -a <tagname>`:Used to create annotated tag,It will ask tag message
* `git tag -a <tagname> -m <tag_message>`: creating annotated tag including tag message 
* `git tag -a <tagname> <commitid> -m <tagmessage>`:Add annotated tag based on previous commit
* `git tag -a <tagname> -f <newcommitid> -m <tagmessage>`:Update the existing annotated tag
* `git diff <tag1> <tag2>`:used to compare two tags 
* `git push origin <tagname>`:used to push the single tag to the remote repo
* `git push origin <branchname> --tags`: used push all tags to the remote repo
>[!NOTE]
> 
> * For the same commit we can define multiple tags also based on our requirement
> * Not possible to use same tag name for multiple commit
> * Bydefault push command wont push tags to the remote repository.

| Light Weight Tag                                       | Annotated Tag                                                    |
|--------------------------------------------------------|------------------------------------------------------------------|
| 1) git tag <tagname>                                   | 1) git tag -a <tagname> -m <tagmessage>                          |
| 2) It is just text label and not implemented as object | 2) It is implemented as object                                   |
| 3) It is stored in .git/refs/tags folder               | 3) It is stored in both .git/refs/tags and .git/objects folders. |
| 4) No extra information stored.                        | 4) It stores tag message, tagger name, date of creation etc.     |