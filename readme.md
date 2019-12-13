#### Navigation:
#### [Part 1 Preparations](#part-1-preparations-1)
##### 1. [get git](#1-here-you-can-find-and-download-git)
##### 2. [setup git](#2-setup-git-change-your-global-configs)
##### 3. [generate ssh](#3-generate-ssh-key)
##### 3. [gitignore](#4-gitignore)
#### [Part 2 Basics & bash commands](#part-2-basics--bash-commands-1)
##### 1. [folders](#1-folders-1)
##### 2. [basics](#2-git-basics)
##### 3. [merging](#3-merging-branches)
##### 3. [inspect a repo.](#4-inspect-your-repository)

***

### Part 1 Preparations 

##### 1. [here you can find and download Git](http://git-scm.com/download/) 

***

##### 2. Setup git: change your global configs 
###### user name:
`git config --global user.name "Vladyslav Filippov"`
###### email:
`git config --global user.email ******@****.com` 

###### set a core editor 												
`git config --global core.editor "'C:/Program Files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"` 

###### check config:
`git config --list`  
***
##### 3. Generate ssh-key 
###### without RSA
`ssh-keygen -t ed25519 -C "email@example.com"`
###### with RSA:
`ssh-keygen -t rsa -b 4096 -C "email@example.com"`
***
##### 4. Gitignore 
###### create the file
`touch .gitignore`

###### add '.gitignore' to .gitignore file 
###### no .a files
`.a`
###### but do track lib.a, even though you're ignoring .a files above
`!lib.a`
###### ignore all files in the build/ directory
`build/`
###### ignore all .pdf files in the doc/ directory
`doc/**/*.pdf`
***
### Part 2 Basics & bash commands 

##### 1. Folders 
###### Create a folder
`mkdir git_handbook`

###### Go to this folder
`cd git_handbook`
***
##### 2. Git basics 
###### Initialize a git repository
`git init`

###### set a remote repository where to push 
`git remote add origin https://github.com/xVladyslav/git_handbook.git`

###### push your local repo. into remote repo.
`git push -u origin master`

###### create readme file 
`touch readme.md`

###### stage your changes
`git add . `

###### make a commit
`git commit -m "initial commit"`
***
##### Branching
###### create new 'develop' branch
`git branch develop`

###### go to this branch
`git checkout develop`
***
###### creating an index.html file in 'developer' branch
`touch index.html`

###### commiting into 'develop' branch
`git add . `

`git commit -m "develop branch changed"`

`git push --set-upstream origin develop`

***

##### 3. Merging branches
`git merge *what to [+additional]*`
##### Example:
###### go to 'develop' branch 
`git checkout develop`
###### merging branches into 'develop'
`git merge images styles`

`git add . `

`git commit -m "merging images and styles in develop"`

`git push`

***

##### 4. Inspect your repository
`git log`

`git reflog`

***
##### 5. Amend
###### use 
`git commit --amend` 
###### to change your latest log message.

###### use 
`git commit --amend`
###### to make modifications to the most recent commit. 

***

#### Part 4 Rebasing
##### 1. rebase 

###### for rebasing use
`git rebase develop`

###### for interactive rebasing use
`git rebase develop -i`
###### to continue rebasing
`git rebase --continue`
###### to abort rebasing
`git rebase --abort`

***
#### Part 5 Conflicts solving
###### abort merge
`git merge --abort`

###### resolve by selecting version
`git checkout --Xours --Xtheirs`

##### resolve manually:
###### show changes between commits, commit and working tree, etc
`git diff`

###### undo merge
`git revert 09fe472`

***

#### Part 6 Undoing changes
###### working directory
`git checkout -- file.txt`

`git checkout . `

`git clean -xdf`

###### staging area (Index)
`git reset -- file.txt`

`git reset --hard`

`git reset --soft`

`git reset --mixed`

![Image of Yaktocat](https://github.com/xVladyslav/git_handbook/blob/master/img/Picture1.png)

###### local branch
`git reset HEAD^^ (HEAD~2)`

`git commit --amend -m “commit message”` 

###### Remote repository
`git revert <sha1>`

	
