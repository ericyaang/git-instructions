# Instructions

## Settings for SSH
```
ssh-keygen -t rsa -b 4096 -C "email@test.com"
```
Set a name and password for the key files.

Look at your files:
```
ls
```
There will be 2 files:
- yourkeyame: your private key (don't share)
- yourkeyname.pub: you public key

Making sure that the git knows that key
Ensure the ssh-agent is running

```
eval "$(ssh-agent -s)"
``` 
## Initiate a repository
```
git init
```
## Clone the repository with HTTPS

```
git clone https://github.com/user-name/repo-name.git

```

## Go to the repo folder directory
```
cd repo-name
```

## See all changes in the repository
```
 ls -la
```

## Before you commit

This command will show you all the changes that have not been committed yet.
```
git status
```
If the file is untracked, this means that you need to add the file to git before anything else.
```
git add file
```

or use . to track all files.
```
git add .
```
## Now commit you file!
```
git commit -m "what and why" -m "some description"
```

## Push commited files to a remote repository

`origin` is the location of the repository.
`master` is the branch that we want to push.
```
git push origin master
```

## Create .gitignore
```
touch .gitignore
```

## Remove files
```
git rm file.txt
```
Remove only from repository
```
git rm --cached file.txt
```
C:\Users\Eric\my-git\git-instructions
## Revert deleted files
C:\Users\Eric\my-git\git-instructions
```
git reset --hard HEAD
```
