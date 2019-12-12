part 1 --------------------------------

1) http://git-scm.com/download/win

2) `git config --global user.name "Vladyslav Filippov"`
   git config --global user.email ******@****.com 
   
   Set a core editor 												
   git config --global core.editor "'C:/Program Files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin" 
   
   check config
   git config --list  

3) 

4) ssh-keygen -t ed25519 -C "email@example.com"
   
   or with RSA
   ssh-keygen -t rsa -b 4096 -C "email@example.com"

5) $ touch .gitignore

//// # no .a files
*.a
# but do track lib.a, even though you're ignoring .a files above
!lib.a
# ignore all files in the build/ directory
build/
# ignore all .pdf files in the doc/ directory
doc/**/*.pdf
///

part 2 -------------------------------------


1) $ mkdir git_handbook

$ cd git_handbook

$ git init

2) $ git remote add origin https://github.com/xVladyslav/git_handbook.git

   $ git push -u origin master
	
	input your username and password




$ git push -u origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 233 bytes | 233.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/xVladyslav/git_handbook.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.



3) $ touch readme.md

4) $ git add .

   $ git commit -m "initial commit"
[master (root-commit) 944db19] initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 readme.md

5) $ git branch develop

$ git checkout develop
Switched to branch 'develop'

6) 
$ touch index.html

$ git add .

$ git commit -m "develop branch changed"
[develop 2a25384] develop branch changed
 1 file changed, 2 insertions(+), 1 deletion(-)

$ git push --set-upstream origin develop


13) 

$ git checkout develop
Switched to branch 'develop'
Your branch is up to date with 'origin/develop'.

Vladyslav_Filippov@EPUAKHAW008A MINGW64 ~/Projects/git_practise1 (develop)
$ git merge styles images
Fast-forwarding to: styles
Trying simple merge with images
Simple merge did not work, trying automatic merge.
Auto-merging index.html
ERROR: content conflict in index.html
fatal: merge program failed
Automatic merge failed; fix conflicts and then commit the result.

Vladyslav_Filippov@EPUAKHAW008A MINGW64 ~/Projects/git_practise1 (develop|MERGING)
$ git add .
warning: LF will be replaced by CRLF in index.html.
The file will have its original line endings in your working directory

Vladyslav_Filippov@EPUAKHAW008A MINGW64 ~/Projects/git_practise1 (develop|MERGING)
$ git add .

Vladyslav_Filippov@EPUAKHAW008A MINGW64 ~/Projects/git_practise1 (develop|MERGING)
$ git commit -m "merging images and styles in develop"
[develop 0160a72] merging images and styles in develop

Vladyslav_Filippov@EPUAKHAW008A MINGW64 ~/Projects/git_practise1 (develop)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 490 bytes | 490.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote:
remote: To create a merge request for develop, visit:
remote:   https://git.epam.com/vladyslav_filippov/git_practise1/merge_requests/new?merge_request%5Bsource_branch%5D=develop
remote:
To https://git.epam.com/vladyslav_filippov/git_practise1.git
   f8dbef1..0160a72  develop -> develop



part 3 ----------------------------
## inspect your repository
$ git log

$ git reflog
