# change-commit-autor
# step by step 
### firts use
```bash
  git log
```
- select the token or id of the commit
```bash
git checkout <commit-hash>
```
- use head to use nano terminal, the n must be an number of a version like 2 or 5
```bash
git rebase -i HEAD~n
```
- you will see the nano terminal so up it you will see the last commits or the commit where you are standing it will see like:
```bash
  pick 22f6c5a explaining the theory of componets in nest
  pick ff7cb5f explaining teory of fundamental elements in nestjs
```

- you need to change the word pick to edit like this:
```bash
  pick 22f6c5a explaining the theory of componets in nest
  edit ff7cb5f explaining teory of fundamental elements in nestjs
```
- after that you need to save it using the command ctrol + o to save changes, then enter to confirm the changes and then ctrol + x to exit remember that if you want to write in the terminal you user ctrol + c

### second use
- now you are in the bash terminal again so you will pul this command to change the credentials of that commit
```bash
git commit --amend --author="new name <newemail@example.com>"
```
- you will see the nano terminal again so verificate if the changes in the commit are correct and confirm with ctrol + o to save changes, then enter to confirm the changes and then ctrol + x to exit 

- now you will confirm the changes so use this command
```bash
git rebase --continue
 ```

### third use
- use this command to see the rebase status if it is not ok use ***git rebase --abort*** and try it again
  ```bash
  git status
  ```

- see if the credentials was changed using the command
```bash
git log
```

- lastly confirm the changes in the remote repository with
```bash
git push --force
```
