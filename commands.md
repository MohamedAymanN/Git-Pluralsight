# Config username
```git
git config --global user.name "" 
```
# Config email
```
git config --global user.email "" 
```
# List all configs
```
git config -l
```

# List a specific config
```
git config <configName>
```

# Initialize git repo
```
git init
```

# Add a file to staging
```
git add . // Adds all
git add <fileName>
```

# Commit
```
git commit -m "first commit"
```

# Link local with remote repo
```
git remote add origin "remoteURL"
```
# Push repo to remote
```
git push -u origin master
```

# Status of repo
```
git status
```
## Shorter status
```
git status -s
```
 _________________________________  
 | Staged | Modified | File Name |  
 |   M    |          |     F1    |  
 |        |     M    |     F2    |  
 |   ?    |     ?     |           |  
 ---------------------------------  
 - M : Modified
 - A : New File added to staging
 - ??: New file untracked by git
 
# Git Diff 
 ```
 git diff --staged
 ```
  ## If two files are similar and are not the same name, git thinks we copied and renamed the files
 Avoid this:
 ```
 git diff --staged --no-renames
 ```
 ## Changes made but not yet staged
 ```
 git diff
 ```
 
 # View commit history
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
