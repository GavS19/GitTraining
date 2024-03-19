# Commands #
## Tags - simply add tags like for version controlling
Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git tag mytag
Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git tag --list
mytag

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git hist
*   1860d80 (HEAD -> master, tag: mytag) Resolving conflict
|\
| * 750a41a (very-bad) worse update in newcommands
* | 72c0896 fixed bad updates in master for newcommands
|/
* 9b0ede5 updated newcommands
* 5c98c09 added newcommands
* d249390 removed readme from gitignore
* 79c2163 updated gitignore
* 1b2cfac untracking readme
*   b249cf7 Merge branch 'updates'
|\
| * 879beb4 Updated Home.html
* | 7d97490 Updated the same line on Home.html
* | 83c173a Readme first checkin
|/
* 2f0e65c added commands
* 7a8d2fb updated in branch
* 994afc9 Initial

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git tag -d mytag
Deleted tag 'mytag' (was 1860d80)

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git tag -a V1.0 -m "Release 1.0"

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git hist
*   1860d80 (HEAD -> master, tag: V1.0) Resolving conflict
|\
| * 750a41a (very-bad) worse update in newcommands
* | 72c0896 fixed bad updates in master for newcommands
|/
* 9b0ede5 updated newcommands
* 5c98c09 added newcommands
* d249390 removed readme from gitignore
* 79c2163 updated gitignore
* 1b2cfac untracking readme
*   b249cf7 Merge branch 'updates'
|\
| * 879beb4 Updated Home.html
* | 7d97490 Updated the same line on Home.html
* | 83c173a Readme first checkin
|/
* 2f0e65c added commands
* 7a8d2fb updated in branch
* 994afc9 Initial

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git tag --list
V1.0

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git show
commit 1860d805dda9893d12d483093361b7019ffec606 (HEAD -> master, tag: V1.0)
Merge: 72c0896 750a41a
Author: GavS19 <124889856+GavS19@users.noreply.github.com>
Date:   Mon Mar 18 21:50:44 2024 +0530

    Resolving conflict

## Stash - save work in progress in current file for emergency commit 

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ ls
Home.html  HowTo.md  NewCommands.md  license.txt

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ nano Home.html

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git stash
Saved working directory and index state WIP on master: f97e43b added license

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git stash list
stash@{0}: WIP on master: f97e43b added license

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ nano license.txt

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   license.txt

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git commit -am "Updated release"
warning: in the working copy of 'license.txt', LF will be replaced by CRLF the next time Git touches it
[master 260d165] Updated release
 1 file changed, 1 insertion(+)

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ cat Home.html
This is Home Page
Updates in 'updates' branch
Well this is an HTML.. if you look at it

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
nothing to commit, working tree clean

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git stash pop
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (ac0dbdbd228d33105ebdb440be091e503aa76d1b)

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git stash list

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ cat Home.html
This is Home Page
Updates in 'updates' branch
Well this is an HTML.. if you look at it
added lines.. work in progress

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git commit Home.html -m "removed stash & commited my work"
[master dd49304] removed stash & commited my work
 1 file changed, 1 insertion(+)

## reset
Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ ls
Home.html  HowTo.md  NewCommands.md  license.txt

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ nano Home.html

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ cat Home.html
This is Home Page
Updates in 'updates' branch
Well this is an HTML.. if you look at it
added lines.
work to be added in staging area


Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git add .

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Home.html


Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ nano Home.html

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ cat Home.html
This is Home Page
Updates in 'updates' branch
Well this is an HTML.. if you look at it
added lines.
work to be added in staging area
more work added


Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html


Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git hist
* a4a2f67 (HEAD -> master) checkin new commands
* dd49304 removed stash & commited my work
* 260d165 Updated release
* f97e43b added license
* 87d0406 new commands
*   1860d80 (tag: V1.0) Resolving conflict
|\
| * 750a41a (very-bad) worse update in newcommands
* | 72c0896 fixed bad updates in master for newcommands
|/
* 9b0ede5 updated newcommands
* 5c98c09 added newcommands
* d249390 removed readme from gitignore
* 79c2163 updated gitignore
* 1b2cfac untracking readme
*   b249cf7 Merge branch 'updates'
|\
| * 879beb4 Updated Home.html
* | 7d97490 Updated the same line on Home.html
* | 83c173a Readme first checkin
|/
* 2f0e65c added commands
* 7a8d2fb updated in branch
* 994afc9 Initial

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git reset 1860d80 --soft

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git hist
*   1860d80 (HEAD -> master, tag: V1.0) Resolving conflict
|\
| * 750a41a (very-bad) worse update in newcommands
* | 72c0896 fixed bad updates in master for newcommands
|/
* 9b0ede5 updated newcommands
* 5c98c09 added newcommands
* d249390 removed readme from gitignore
* 79c2163 updated gitignore
* 1b2cfac untracking readme
*   b249cf7 Merge branch 'updates'
|\
| * 879beb4 Updated Home.html
* | 7d97490 Updated the same line on Home.html
* | 83c173a Readme first checkin
|/
* 2f0e65c added commands
* 7a8d2fb updated in branch
* 994afc9 Initial

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Home.html
        modified:   NewCommands.md
        new file:   license.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html


Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$
Display all 5441 possibilities? (y or n)

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git reset a4a2f67 --soft

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html


Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git hist
* a4a2f67 (HEAD -> master) checkin new commands
* dd49304 removed stash & commited my work
* 260d165 Updated release
* f97e43b added license
* 87d0406 new commands
*   1860d80 (tag: V1.0) Resolving conflict
|\
| * 750a41a (very-bad) worse update in newcommands
* | 72c0896 fixed bad updates in master for newcommands
|/
* 9b0ede5 updated newcommands
* 5c98c09 added newcommands
* d249390 removed readme from gitignore
* 79c2163 updated gitignore
* 1b2cfac untracking readme
*   b249cf7 Merge branch 'updates'
|\
| * 879beb4 Updated Home.html
* | 7d97490 Updated the same line on Home.html
* | 83c173a Readme first checkin
|/
* 2f0e65c added commands
* 7a8d2fb updated in branch
* 994afc9 Initial

## GitHub setup
In Github, create a repository. 
then copy the URL available in the readme/help page displayed

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git remote -v

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git remote add origin https://github.com/GavS19/GitTraining.git

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git remote -v
origin  https://github.com/GavS19/GitTraining.git (fetch)
origin  https://github.com/GavS19/GitTraining.git (push)

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git push -u origin master --tags
Enumerating objects: 61, done.
Counting objects: 100% (61/61), done.
Delta compression using up to 4 threads
Compressing objects: 100% (55/55), done.
Writing objects: 100% (61/61), 7.36 KiB | 396.00 KiB/s, done.
Total 61 (delta 21), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (21/21), done.
To https://github.com/GavS19/GitTraining.git
 * [new branch]      master -> master
 * [new tag]         V1.0 -> V1.0
branch 'master' set up to track 'origin/master'.


## Git default  branch rename ##
Due to recent developments, the default branch names is being changed from 'master' to 'main'
for the new repo's which could create conflict if local git uses existing naming convention - master and Github uses main
### Workarounds
1. Github - Update default repo name under Profile>>Settings>>Repository. Set to main 
2. Git - update existing branch name to main
    git branch -m main
3. Git - Initiate with new name
    git init -b main local-demo
4. Git - Configure default branch
    git config --global init.defaultBranch main


## Authentication
### HTTPS 
* Need to input username & password everytime pushing files from local to remote repo

### SSH
* Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev
$ ls
GitBranching/  SigmaWebDev/  TestGitOps/

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev
$ ls .ssh
ls: cannot access '.ssh': No such file or directory

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev
$ mkdir .ssh

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev
$ cd .ssh

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/.ssh
$ .ssh-keygen -t rsa -C "gsaitwal19@gmail.com"
bash: .ssh-keygen: command not found

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/.ssh
$ cd \
>

Admin@DESKTOP-092184C MINGW64 ~
$ ssh -V
OpenSSH_9.4p1, OpenSSL 3.1.2 1 Aug 2023

Admin@DESKTOP-092184C MINGW64 ~
$ echo $PATH
/c/Users/Admin/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:/c/Users/Admin/bin:/c/Python312/Scripts:/c/Python312:/c/Program Files/Microsoft MPI/Bin:/c/Program Files (x86)/Common Files/Oracle/Java/javapath:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/130/Tools/Binn:/c/Program Files (x86)/Microsoft SQL Server/140/Tools/Binn:/c/Program Files/Microsoft SQL Server/140/Tools/Binn:/c/Program Files/Microsoft SQL Server/140/DTS/Binn:/c/Program Files (x86)/Microsoft SQL Server/140/DTS/Binn:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/110/Tools/Binn:/c/Program Files (x86)/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/DTS/Binn:/c/Program Files (x86)/Microsoft SQL Server/150/DTS/Binn:/c/Program Files/Azure Data Studio/bin:/cmd:/c/Program Files/nodejs:/c/ProgramData/chocolatey/bin:/c/Program Files/dotnet:/c/Users/Admin/AppData/Local/Programs/Python/Python37-32/Scripts:/c/Users/Admin/AppData/Local/Programs/Python/Python37-32:/c/Users/Admin/AppData/Local/Microsoft/WindowsApps:/e/PyCharm Community Edition 2018.3.2/bin:/c/Program Files/Java/jre1.8.0_281/bin:/c/Program Files/Azure Data Studio/bin:/c/Users/Admin/AppData/Local/Programs/Microsoft VS Code/bin:/c/Users/Admin/AppData/Local/GitHubDesktop/bin:/c/Users/Admin/AppData/Roaming/npm:/usr/bin/vendor_perl:/usr/bin/core_perl

Admin@DESKTOP-092184C MINGW64 ~
$ cd /f/DOMAIN_LEARNING/SigmaWebDev/.ssh

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/.ssh
$ ssh-keygen -t rsa -C "gsaitwal19@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Admin/.ssh/id_rsa):
Created directory '/c/Users/Admin/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/Admin/.ssh/id_rsa
Your public key has been saved in /c/Users/Admin/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:Rt8OXymLfn117om/tQIDEQ4qWrBn+iyooB5CdYTbvFY gsaitwal19@gmail.com
The key's randomart image is:
+---[RSA 3072]----+
| .  .. . ..      |
|  o.. . o.       |
| . *+o  ...      |
|  B.oo E o .   . |
| +    o S + o o  |
|o o  o .   B +  o|
|+o o.     . *. .+|
|= o      .  ..o *|
|+.        .. .oBo|
+----[SHA256]-----+

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/.ssh
$ ls -al
total 0
drwxr-xr-x 1 Admin 197121 0 Mar 19 21:55 ./
drwxr-xr-x 1 Admin 197121 0 Mar 19 21:55 ../
