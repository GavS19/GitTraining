Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
nothing to commit, working tree clean

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ ls
Home.html  HowTo.md

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git checkout -b updates
Switched to a new branch 'updates'

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (updates)
$ git status
On branch updates
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (updates)
$ git switch master
Switched to branch 'master'
M       Home.html

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (master)
$ git switch updates
Switched to branch 'updates'
M       Home.html

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (updates)
$ git status
On branch updates
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Home.html

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (updates)
$ git add .

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (updates)
$ git commit -m "updated in branch"
[updates 7a8d2fb] updated in branch
 1 file changed, 2 insertions(+)

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (updates)
$ git diff updates master
diff --git a/Home.html b/Home.html
index 599ee1a..e69de29 100644
--- a/Home.html
+++ b/Home.html
@@ -1,2 +0,0 @@
-This is Home Page
-Updates in 'updates' branch
\ No newline at end of file

Admin@DESKTOP-092184C MINGW64 /f/DOMAIN_LEARNING/SigmaWebDev/GitBranching (updates)
$ git switch master
Switched to branch 'master'
