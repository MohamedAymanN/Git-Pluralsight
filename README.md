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

![image](https://user-images.githubusercontent.com/45315180/113683456-84c21380-96c4-11eb-9e60-6bc23311c903.png]


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
