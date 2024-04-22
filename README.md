# Gym-Git-Practices

## Bundle 1

 ### Exercise 1
 ```bash
 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ mkdir practice

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git init
Reinitialized existing Git repository in C:/Users/thegym/Desktop/Gym-Git-Practices/.git/

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ touch index.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ cd practice

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ mv index.html new.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git commit -m "Renaming files"
[main ca2ee16] Renaming files
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename practice/{index.html => new.html} (100%)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 320 bytes | 160.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/beylar/Gym-Git-Practices.git
   c263dc4..ca2ee16  main -> main

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git branch dev

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git checkout dev
Switched to branch 'dev'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (dev)   
$ git branch test

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (dev)   
$ git branch -d test
Deleted branch test (was ca2ee16).

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (dev)   
$ git merge dev
Already up to date.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (dev)   
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```

### Exercise 2
```bash
thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ touch home.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)
$ git stash
Saved working directory and index state WIP on main: ca2ee16 Renaming files

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)
$ touch about.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)
$ git stash
No local changes to save

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)
$ git stash
Saved working directory and index state WIP on main: ca2ee16 Renaming files

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ touch team.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git stash
Saved working directory and index state WIP on main: ca2ee16 Renaming files

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git stash list
stash@{0}: WIP on main: ca2ee16 Renaming files
stash@{1}: WIP on main: ca2ee16 Renaming files
stash@{2}: WIP on main: ca2ee16 Renaming files

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git stash pop 1
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped refs/stash@{1} (935b2737d764cbeefeb761ff6f2616c7eb9b7c31)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git stash pop 0
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped refs/stash@{0} (8c60bd8e8998cdf4f46ff764032a163b227b463d)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git stash list
stash@{0}: WIP on main: ca2ee16 Renaming files

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (a32ff765aa1ad0ed7e7591d5627a0827a614d32e)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git commit -m "Stashed files"
[main 51e294b] Stashed files
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 practice/about.html
 create mode 100644 practice/team.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 338 bytes | 112.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/beylar/Gym-Git-Practices.git
   ca2ee16..51e294b  main -> main

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git reset --hard
HEAD is now at 51e294b Stashed files
```
## Bundle 2

### Exercise 1
```bash
thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git branch ft/bundle-2

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git checkout ft/bundle-2 
Switched to branch 'ft/bundle-2'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/bundle-2)    
$ touch services.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/bundle-2)    
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/bundle-2)    
$ git commit -m "My services page added"
[ft/bundle-2 902495a] My services page added
 1 file changed, 11 insertions(+)
 create mode 100644 practice/services.html

 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/bundle-2)    
$ git push origin -u ft/bundle-2 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 527 bytes | 175.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.        
To https://github.com/beylar/Gym-Git-Practices.git
   da4680e..902495a  ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

```

### Exercise 2
```bash
thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git pull
remote: Enumerating objects: 2, done.
remote: Counting objects: 100% (2/2), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 1.74 KiB | 296.00 KiB/s, done.
From https://github.com/edine-noella/Git-practice-project1
   3276ce4..2e4beb0  main       -> origin/main
Updating 3276ce4..2e4beb0
Fast-forward
 about.html    | 11 +++++++++++
 home.html     | 11 +++++++++++
 services.html | 12 ++++++++++++
 3 files changed, 34 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git branch ft/service-redesign

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git checkout ft/service-redesign 
M       README.md
D       practice/team.html
Switched to branch 'ft/service-redesign'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/service-redesign)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/service-redesign)
$ git commit -m "My services file changes"
[ft/service-redesign e7db401] My services file changes
 2 files changed, 40 insertions(+)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 904 bytes | 301.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.       
To https://github.com/beylar/Gym-Git-Practices.git
   b5e0e67..e7db401  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git pull
Updating b5e0e67..f27daaf
Fast-forward
 README.md              | 58 ++++++++++++++++++++++++++++++++++++++++++++++++++
 practice/services.html | 11 ++++++++++
 practice/team.html     |  0
 3 files changed, 69 insertions(+)

 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git commit -m "Services file"
[main 93335a2] Services file
 1 file changed, 1 insertion(+)
 
 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 408 bytes | 204.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.       
To https://github.com/beylar/Gym-Git-Practices.git
   ada7644..93335a2  main -> main

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git checkout -f ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/service-redesign)
$ git diff main ft/service-redesign
diff --git a/README.md b/README.md
index d1b1d2c..3d84f6b 100644
--- a/README.md
+++ b/README.md
@@ -261,33 +261,5 @@ remote: Resolving deltas: 100% (2/2), completed with 2 
local objects.
 To https://github.com/beylar/Gym-Git-Practices.git
    b5e0e67..e7db401  ft/service-redesign -> ft/service-redesign
 branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'. 
-
-thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
-$ git pull
-Updating b5e0e67..f27daaf
-Fast-forward
- README.md              | 58 ++++++++++++++++++++++++++++++++++++++++++++++++++
- practice/services.html | 11 ++++++++++
- practice/team.html     |  0
- 3 files changed, 69 insertions(+)
-
- thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
-$ git add .
-
-thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
-$ git commit -m "Services file"
-[main 93335a2] Services file
- 1 file changed, 1 insertion(+)

- thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
-$ git push origin main
-Enumerating objects: 7, done.
-Counting objects: 100% (7/7), done.
-Delta compression using up to 4 threads
-Compressing objects: 100% (4/4), done.
-Writing objects: 100% (4/4), 408 bytes | 204.00 KiB/s, done.
-Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
-remote: Resolving deltas: 100% (2/2), completed with 2 local objects.      
 
-To https://github.com/beylar/Gym-Git-Practices.git
-   ada7644..93335a2  main -> main

\ No newline at end of file
diff --git a/practice/services.html b/practice/services.html
index 6dd7f53..7544a4e 100644
--- a/practice/services.html
+++ b/practice/services.html
@@ -6,7 +6,6 @@
     <title>My services are the following</title>
 </head>
 <body>
-    <p>Please follow for more info: what is it?</p>
-    <div class="new"></div>
+    <p>Please follow for more info</p>
 </body>
 </html>
\ No newline at end of file
(END)
```

## Bundle 3
 ### Exercise 1

 ```bash
 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git branch ft/team-page

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ touch team.html

