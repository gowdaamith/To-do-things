# GitHub Commands 

Setup and Config
```bash
git config --global user.name "your name"
```
```bash
git config --global user.email "your@example.com"
```
To see the Confiured list of the user use : 
```bash
git config --list
```
_________________________________________________________________________________________________________________

Create / Clone Repo 

_____________________________________________________________________________________________________________
Add and Commit 

Add a specific file
```bash
git add filename.txt
```
Add all changes
```bash
git add .
```
Commit the changes
```bash
git commit -m " message "
```
_______________________________________________________________________________________________________________
Branching 

List the branches
```bash
git branch
```
Create a branch
```bash
git branch new-branch
```
Switch the Branch 
```bash
git checkout  new-branch
```
Create and Switch 
```bash
git checkout -b new-one
```

               or 
Switch the branch
```bash
git switch branch-name
```
Create and switch teh branch 
```bash
git switch -c new-branch
```
_________________________________________________________________________________________________________________
Check Status and History 

Gives the current state of the repo
```bash
git status
```
Commit History 
```bash
git log
```
Compact history 
```bash
git log --oneline --graph
```
______________________________________________________________________________________________________________
Merging of Branch 

First Switch to the main branch
```bash
git switch main
```
Then merge the branch
```bash
git merge feature-branch
```
_______________________________________________________________________________________________________________
Remote 
To check where your local repo is connect to use 
```bash
git remote -v
```
To connect your local repo to the remote repo 
```bash
git remote add origin  <URL>
```
To push use
```bash
git push origin main
```
To pull use 
```bash
git pull origin main
```
To Set the Upstream once  ,after this you can just use git pull and git pulll: 
```bash
git push -u origin main
```
To push the local changes 
```bash
git push
```
To pull and  Merge the Chages from remote repo
```bash
git pull
```
To Only fetch the changes and not to merge
```bash
git fetch
```
 
______________________________________________________________________________________________________________f
Stash

To make the working directory Clean so other imp work can be done now 
```bash
git stash
```
To Bring back the stash :

Applie  and delete:
```bash
git stash pop
```
Applie and keep : 
```bash
git stash apply
```
View stash 
```
git stash list
```
Push a Stash with a message 
```bash
git stash push -m " any message"
```
Drop the stash
```bash
git stash drop StashID
```
Clear all the stash 
```bash
git stash clear
```
____________________________________________________________________________________________________________
Undo / Fix the Mistakes

Discard the file changes
```bash
git restore file.txt
```
Unstage file
```bash
git restore --staged file.txt
```
Undo commit and keep changes
```bash
git reset --soft HEAD~1
```
Undo commit and delete changes
```bash
git reset --hard HEAD~1
```
____________________________________________________________________________________________________________
Difference 

To know the differece between the Working dir and staging area [Use before git add]
```bash
git diff
```
To know the difference between the staging area and the last commit 
```bash
git diff --staged
```
To see the detail fo the last commit use 
```bash
git show
```
or To me more specific
```bash
git show <commit-id>
```
____________________________________________________________________________________________________________
To create a Tag on the current commit
```bash
git tag v1.0
```
To list all the tags in the repo
```bash
git tag
```
To tags are local by default to push the tags use :
```bash
git push origin v1.0
```
Or push all tags
```
git push origin --tags
```

