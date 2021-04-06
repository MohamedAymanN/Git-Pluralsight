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
