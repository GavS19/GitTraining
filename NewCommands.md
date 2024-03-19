## Commands ##
**Tags - simply add tags like for version controlling**
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
