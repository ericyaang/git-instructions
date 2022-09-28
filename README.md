<!-- vscode-markdown-toc -->
* 1. [Settings for SSH](#SettingsforSSH)
* 2. [Initiate a repository](#Initiatearepository)
* 3. [Clone the repository with HTTPS](#ClonetherepositorywithHTTPS)
* 4. [Go to the repo folder directory](#Gototherepofolderdirectory)
* 5. [See all changes in the repository](#Seeallchangesintherepository)
* 6. [Before you commit](#Beforeyoucommit)
* 7. [Now commit you file!](#Nowcommityoufile)
* 8. [Push commited files to a remote repository](#Pushcommitedfilestoaremoterepository)
* 9. [Create .gitignore](#Create.gitignore)
* 10. [Remove files](#Removefiles)
* 11. [Revert deleted files](#Revertdeletedfiles)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc --># Instructions

##  1. <a name='SettingsforSSH'></a>Settings for SSH
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
##  2. <a name='Initiatearepository'></a>Initiate a repository
```
git init
```

Create an empty repository on github.

And then connect
```
git remote add origin https://github.com/ericyaang/git-instructions.git
```
Check the connection
```
git remote add origin https://github.com/ericyaang/git-instructions.git
```
Push!
```
git push origin master
```


##  3. <a name='ClonetherepositorywithHTTPS'></a>Clone the repository with HTTPS

```
git clone https://github.com/user-name/repo-name.git

```

##  4. <a name='Gototherepofolderdirectory'></a>Go to the repo folder directory
```
cd repo-name
```

##  5. <a name='Seeallchangesintherepository'></a>See all changes in the repository
```
 ls -la
```

##  6. <a name='Beforeyoucommit'></a>Before you commit

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
##  7. <a name='Nowcommityoufile'></a>Now commit you file!
```
git commit -m "what and why" -m "some description"
```

##  8. <a name='Pushcommitedfilestoaremoterepository'></a>Push commited files to a remote repository

`origin` is the location of the repository.
`master` is the branch that we want to push.
```
git push origin master
```

Lazy push:
```
git push -u origin master
```
then just type use: `git push`

##  9. <a name='Create.gitignore'></a>Create .gitignore
```
touch .gitignore
```

##  10. <a name='Removefiles'></a>Remove files
```
git rm file.txt
```
Remove only from repository
```
git rm --cached file.txt
```

##  11. <a name='Revertdeletedfiles'></a>Revert deleted files
```
git reset --hard HEAD
```
