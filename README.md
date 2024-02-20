# **Codegorrilla Git 101**

A project to help out my fellow dev friends with popular/special Git commands when they're in real need...

## Commands used:

### Initializing a local git repo

## 1. Configure Git settings in your local machine
```html 
git config global user.name <your name>
git config global user.email <your email>
```

## 2. Initialize Git in any of your local repo
```html
git init 
```

## 3. At first only master branch is created, so add/stage all files inside the local folder with the following command first

### to add a single file 
```html 
git add <file-name>
```

### to add all files
```html 
git add .
```

### to unstage all file
```html 
git reset
```

### OR unstage any single file
```html 
git reset <file_name> OR git restore --staged <file_name>
```

## 4. Commit all the staged file in the master branch
```html 
git commit -m "your message" <any single file name> or keep blank for commtting all staged file at once
```

## 5. Now to check the status of the working tree,
```html 
git status 
```

## 6. Once you see the tree is clean, nothing left for commit, set the remote Origin URL
```html
git remote add origin <remote_url>
```
### to change the remote repo URL into SSH URL do type this command
```html
git remote set-url <remote_name> <ssh_remote_url>
```
### to change the remote repo URL
```html
git remote set-url origin <new_remote_url>
```

## 7. to push the master from local to the remote repo(origin)
```html
git push-u origin master or git push -u origin <branch_name>
```
### from second time, only use
```html
git push
```

## 8. to create and checkout to a branch use
```html
git checkout -b <branch_name>
```
## 9. the check all the available branch in both local and origin
```html
git branch -a
```
OR to check the local branches only
```html
git branch
```
### know more about branches, click on the left


## 10. to merge a branch from master, first checkout to the specific branch, then
```html
git merge master or vice versa
```





# Branches

## to create a branch
```html
git branch <branch_name>
```
## create a new branch based on some existing branch
```html
git branch <new_branch> <base_branch>
```
## a new branch from a specific commit
```html
git branch <new_branch> <commit_hash_value>
```

## you can also base your new branch on a specific tag you already have in your repository
```html
git branch <new_branch> v1.2
```
## to create a new local branch from a remote branch
```html
git branch --track <new_branch> origin/<base_branch>
```

alternatively, if the name of the new branch is same as ther remote base branch

```html
git checkout --track origin/<base_branch>
```
## to delete a branch
```html
git branch -d <local_branch_name>
```
in case if you've any pending commits or merge for the branch, then git won't let you delete the branch, hence in that case use to enforce the deletion

```html
git branch -D <local_branch_name>
```
**_do use this command with caution_**

to delete a branch from the remote repo

```html
git push origin --delete <remote_branch_name>
```
## after deletion/creation of any remote branch, how to update the branches in local

```html
git fetch --prune
git pull --prune
```
or to update the set of remote branches in local everytime we run git pull or git fetch use

```html
git config remote.origin.prune true
```
# Additional commands

## to list out all existing git configs use
```html
git config --global --list
```

## to remove all existing git configs use
```html
git config --global --unset-all
```
or use to individually remove configs
```html
git config --global --unset user.name
git config --global --unset user.email
```

## Special commands

### you can use separate Git user name and email for separate project folders in your local environment, use by going inside any specific folder
```html
git config user.name <your user name>
```

and type
```
git config user.email <your email>
```
### in case in local during a merge, the info in the HEAD file is at a mismatch between two branches/ in case when terminal showing can not merge due to unrelated histories,use
#### for example, we're using main branch from both local and remote repo
```html
git pull origin main --allow-unrelated-histories
git merge origin origin/main
```

