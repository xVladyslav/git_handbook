#### Navigation:
#### [Part 1 Preparations](#part1)
##### 1. [get git](#getgit)
##### 2. [setup git](#setup)
##### 3. [generate ssh](#ssh)
##### 3. [gitignore](#gitignore)
#### [Part 2 Basics & bash commands](#part2)
##### 1. [folders](#folders)
##### 2. [basics](#basics)
##### 3. [merging](#merging)
##### 3. [inspect a repo.](#logs)

***

### Part 1 Preparations {#part1}

##### 1. [here you can find and download Git](http://git-scm.com/download/) {#getgit}

***

##### 2. Setup git: change your global configs {#setup}
###### user name:
`git config --global user.name "Vladyslav Filippov"`
###### email:
`git config --global user.email ******@****.com` 

###### set a core editor 												
`git config --global core.editor "'C:/Program Files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"` 

###### check config:
`git config --list`  
***
##### 3. Generate ssh-key {#ssh}
###### without RSA
`ssh-keygen -t ed25519 -C "email@example.com"`
###### with RSA:
`ssh-keygen -t rsa -b 4096 -C "email@example.com"`
***
##### 4. Gitignore {#gitignore}
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
### Part 2 Basics & bash commands {#part2}

##### 1. Folders {#folders}
###### Create a folder
`mkdir git_handbook`

###### Go to this folder
`cd git_handbook`
***
##### 2. Git basics {#basics}
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

###### create new 'develop' branch
`git branch develop`

###### go to this branch
`git checkout develop`

###### creating an index.html file in 'developer' branch
`touch index.html`

###### commiting into 'develop' branch
`git add . `

`git commit -m "develop branch changed"`

`git push --set-upstream origin develop`

***

##### 3. Merging branches {#merging}
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

##### 4. inspect your repository {#logs}
`git log`

`git reflog`

***
