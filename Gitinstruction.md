![Git logo](Git-Logo-1788C.png)
# Git manual
## 1. Git installation check.
Run command `git version` in terminal.
If Git is installed you'll get a message about programm version otherwise you'll get an error message.
## 2. Git installation.
Download the last vesion of Git programm from the website: [Git programm](https://git-scm.com/downloads).
Install Git programm with default settings.
## 3. Git setting up.
The first time you use Git it is necessary to introduce yourself. To do this please run two commands in terminal:
```
git config --global user.name "Your name"
git config --global user.email "Your email" 
```
## 4. Repository Initialization.
Please choose the folder in terminal where repository will be and run command:
```
git init
```
## 5. Alteration saving in repository
### 5.1. Main command for determine of repository condition is:
```
git status
```
This command provides information about changes in the repository and returns advices for the next actions.

### 5.2. Main command to start tracking of the file changes is:
```
git add
```
This command allows Git to identify changes in the file.

### 5.3. Main command to create version of the file is:
```
git commit
```
This command create a check point of the file condition with unique hash code that's provide possibility to return to this conditon of the file.

### 5.4. How to understand the difference between last committed version and current status of the file?
To identify the differencies between two files helps command:
```
git diff
```
This command returns the information about deleted or added lines.
## 6. Avaliable versions review.

The main command to see the list of file commits is:
```
git log
```
This command returns all avaliable file checkpoints with hash-code and developer comments. Also it is possible to use short version of the command to see the title of the check points only: `git log --oneline`.
## 7. Navigation between different versions of the file.
If it is necessary to return to previous version of the file we can find hash-code of reqiured commit using command `git log`.
Using command:
```
git checkout + hash-code
```
we are able to return to any files condition that was commited.

To return to main file we have to use command:
```
git checkout master
```
or 
```
git switch master
```

## 8. Files ignore
 To exlude from tracktion certain files of repository it is necessary to create folder ***.gitignore*** and notes names of these files in this file.

 If it is necessary to exclude group of the similar files (pictures or movies for example) it is necessary to add a sample in the folder ***.gitignore*** for this group of files (last four symbols from file name). For example ***.jpg**.
 ## 9. Branches creation in git.
 The name of the main branch in git is master as default.
To create new branch we have to use command:
```
git branch branch_name
```
List of branches in repository we can see using to:
```
git branch
```
Current branch is highlighted by ("*"): For example ***master**.

To return to main branch  or another one we have to use command:
```
git checkout master or branch_name
```
or 
```
git switch master or branch_name
```
## 10. Branches merging and conflicts resolving.
To merge selected branch with current branch it is necessary to run command:
```
git merge branch_name
```
If the same part of file was modified in merged branches, conflict is occure ==> User actions is required.

VSCode propose ways to resolve the issue. User can follow by one of the proposed way or may correction manualy.

`Important !` As conflict is resolved it is necessary to run commit command to complete merge of two branches.

## 11. Branch removal
If we need to remove one of the branch that have been already merged with main branch we need to use command:
```
git branch -d branch_name
```
Before branch removal it is necessary to be sure that we are on the master branch otherwise we'll got error message.

If we need to remove additional branch without merging with master branch we have to use command:
```
git branch -D branch_name
```
## 12. Work with remote repo

Remote access to repository allows to work with projects many users at the same time. To control the changes made by different developers we use special remote services. The most wide spread service is GitHub.
### 12.1 Registration at GitHub.com

Please follow the link to join GitHub service: [Link to GitHub](https://github.com). Manual for registration you will find on the web-site.
### 12.2 Transfer of local repo to remote version at your account.
Once you have your account at GitHub you are able to share your local repo to other users.

First of all it is necessary to create new repository at GitHub.com.
To transfer you local repo to GitHub it is necessary to run comand:

```
git push
```

As an example:
```
git remote add origin https://github.com/(Your GitHub account Name)/RepositoryName.git
git branch -M main
git push -u origin main
``````

### 12.3 Transfer of new commits of yours remote repo to local work station.

In case your repository was created or modified remotely at your GitHub account you are able to transfer new commits to your local work station.

The main command to transfer remote repo to local work station is:
```
git pull
```
### 12.4 Transfer of other users remote repo to your local work station.

First of all you need to copy url address of remote repo from GitHub.com (please see picture below):

![Link of remote repo](Pull_image.jpg)

And than you need run command:
```
git clone (https://url address)
```
### 12.5 Getting access to repos of other users in GitHub service.

If you are intersted in open source projects avaliable at GitHub service you need to get an access. You have to use "Fork" function to copy the repo to your GitHub account.

Please push the button as shown below:
![Fork button](Fork.png)

### 12.6 Sharing of your ideas to project owner.

Once you have forked repo of other users you can decribe your ideas in new branch and return you ideas to the author.

Please use `Pull request` button in GitHub.
