# Git-Pluralsight

# What is git?
 - Version control system 
   - Software designed to record changes made to files overtime
   - Ability to revert back to older versions
   - Compare changes through different versions

# Three stages of a file
 - Committed; File is stored in the local database within a project
 - Modified;  File content has changed, changed from committed; Changed but not committed yet (Work in progress)
 - Staged;    Changes are ready to be committed; 

![image](https://user-images.githubusercontent.com/45315180/113683456-84c21380-96c4-11eb-9e60-6bc23311c903.png)


## Process 
 1. Committed file if modifed turns to be Modified
 2. Modified file when done with changes is marked for committing and changed to Staged
 3. Staged files are then committed
### Files only tracked by git are in this process; File in the last commit snapshot

# Three Main parts of git
 - .git directory (repository); Origin of data, Pulled down from the remote server; stores metadata and object database.
 - Working Directory; Single copy, checkout of one version of the project; pulled from .git directory to here
 - Staging Area (Index); Build up changes that he wants to commit; takes snapshot of project with those changes in place
## Process
 1. Pulled files from remote repo are in .git directory
 2. Files are then sent to the working directory
 3. A snapshot could be taken to the Staging directory to apply more modifications
 4. Staging is then commited back to the .git directory
 
 ![image](https://user-images.githubusercontent.com/45315180/113676217-766ff980-96bc-11eb-920d-1e35599d6d30.png)

# Process for simple repo
## 1. Init a repo
```
git init
```
 - A .git directory is created and is hidden.

## 2. Create a README file
```
echo "# FileName" >> README.md
```

## 3. Add file to staging
```
git add . // Add all
git add <fileName>
```
## 4. Commit
```
git commit -m "first commit"
```

## 5. Link local with remote repo
```
git remote add origin "remoteURL"
```

## 6. Push repo to remote
```
git push -u origin master
```

# Lets check the status of our repo
```
git status
```

## Shorter status
```
git status -s
```
 _________________________________
 | Staged | Modified | File Name |
 |   M    |          |     F1    |
 |        |     M    |     F2    |
 |   ?    |     ?    |           |
 --------------------------------- 
 - M : Modified
 - A : New File added to staging
 - ??: New file untracked by git

# Git Diff 
 - Changes staged that are ready to be committed

![image](https://user-images.githubusercontent.com/45315180/113685543-a7edc280-96c6-11eb-88fb-c7c33947c635.png)

 ```
 git diff --staged
 ```
   - Shows files that are compared from different snapshot versions
   - File Metadata; hash of files compared (SHA-1); Number identifier (100644: Normal file)
   - Change markers for files
   - Chunk header; changes happend `@@ -12, 2 +12, 3 @@` (- for file A and + for file B); -12 2: File A has 2 changes starting from line 12
   - Chunk changes; the line itselfes
 ## If two files are similar and are not the same name, git thinks we copied and renamed the files
 Avoid this:
 ```
 git diff --staged --no-renames
 ```
 
 - Changes made but not yet staged
 ```
 git diff
 ```
 
 # View commit history
  -  Reverse chronological order; Latest is first
 ```
 git log
 ```
 
 ## Limit number of logs
 ```
 git log -1
 ```
 
  ## Single line format
 ```
 git log --oneline
 ```
 
 ## Detailed log
 ```
 git log --stat
 ```
 
 ## More Detailed log
 ```
 git log --patch
 ```
 
 # Guidlines for commit messages
 https://chris.beams.io/posts/git-commit/
 
 # Remove file from tracking and project
 ```
 git rm <fileName>
 ```
 
 # Remove file from tracking ONLY
 ```
 git rm <fileName> --cached
 ```
 
 # Rename file
 ```
 git mv <filename> <newFileName>
 ```
 
 # Stash commits
 ```
 git stash
 git stash list
 git stash show
 git stash pop // Remove from stash
 ```
 
 # Branches
  - Visualization Tool: https://git-school.github.io/visualizing-git/
  ## Creating a new branch
  ```
  git branch <branchName>
  ```
  ## Creating a new branch and checkout to it
  ```
  git checkout -b <branchName>
  ```
  
  ## Checkout to another branch
  ```
  git checkout <branchName>
  ```
  
  ## Merge branches
  ```
  git merge <branch1> // Merge current branch with <branch1>
  ```
  
# Change History with rest
 - Move specifc commit(s) from repo to staging
 ```
 git reset --soft
 ```
 - Move changes to workdir
 ```
 git reset --mixed
 ```
 - Move changes to trash
 ```
 git reset --hard
 ```
# Pull from remote repo
```
git clone <repoLink>
```

# Pull latest metadata info from original repo
```
git fetch <repoLink>
```
