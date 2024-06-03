# Git Aliases

---
Alias means nickname or short name or other alternative name to the command,In Git we can create our own commands by using aliasing concept.

### Creating alias Name
We can create alias name by using git config command.
```commandline
Syntax: 
   git config --global alias.aliasname "original command without git"
```
Ex:git config --global alias.one "log --oneline" 
>[!NOTE]
> 
> After creating alias name, we can use either alias name or original name.