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

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git checkout ft/team-page
M       README.md
Switched to branch 'ft/team-page'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/team-page)   
$ cd practice

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ touch team.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ git commit -m "My changes in team page"
[ft/team-page 701b7bd] My changes in team page
 2 files changed, 24 insertions(+), 2 deletions(-)
 create mode 100644 practice/team.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ git push 
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 643 bytes | 107.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.       
To https://github.com/beylar/Gym-Git-Practices.git
   ce955f3..701b7bd  ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.        
Aborting

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ git checkout -f main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git branch ft/contact-page

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)  
$ git checkout -f ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/team-page)
$ git log
commit 701b7bdbf80cb7c3d560c92a9a24f3ab5542d2bc (HEAD -> ft/team-page, origin/ft/team-page)
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 18:01:49 2024 +0200

    My changes in team page

commit ce955f3eab2e2cfa745658eed03a6b21efba480b (origin/main, origin/HEAD, main, ft/contact-page)
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:52:27 2024 +0200

    Diff main ft/service-redesign

commit cac470eaa98deef3fd3f866552112ed4f333d80e
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:47:10 2024 +0200

    My ReadMe

commit 93335a2a2c43029710ce7840bb348170d18722e6
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:42:53 2024 +0200

    Services file

commit ada7644f5c428f28d7156f1103be2e0e43d0434e
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:27:24 2024 +0200

    My services page in main branch

commit f27daaf03a9ac6e82bf19cd05ca09787c4185b35
Merge: b5e0e67 eeb1cc5
Author: Beyla Ruzindana Irakoze <142901020+beylar@users.noreply.github.com> 
Date:   Mon Apr 22 17:23:56 2024 +0200

    Merge pull request #2 from beylar/ft/service-redesign

    Ft/service redesign

commit eeb1cc55c12b3ebd22f5d08c6ab977bc4e3348e2 (origin/ft/service-redesign, ft/service-redesign)
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:22:36 2024 +0200

    M y README

commit e7db401601217321f9ab4497a6de378e3bac19c6
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:16:17 2024 +0200

    My services file changes

commit b5e0e67d9ab438a22ec60f788aa9dbd8052e93c0
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:08:52 2024 +0200

    new changes

commit f8b88075a31fdab40bcb8c1c3a5ab3dbd939cc34
Merge: 14d6e13 99370cf
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 17:02:41 2024 +0200

    Merge branch 'main' of https://github.com/beylar/Gym-Git-Practices      

commit 99370cfccd303e9855601f7861dbcb9a1dee4061
Merge: da4680e 902495a
Author: Mugisha Edine Noella <edinenoella@gmail.com>
Date:   Mon Apr 22 16:47:57 2024 +0200

    Merge pull request #1 from beylar/ft/bundle-2

    My services page added

commit 902495a5d28707859cfc2f7cee25c3e6673c34b3 (origin/ft/bundle-2)        
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 16:38:47 2024 +0200

    My services page added

commit 14d6e1332fb9e3e3f03b3f527433b934c485ada0
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 16:36:06 2024 +0200

    Services page added

commit da4680e4a61a6ac89c48cd46918e96002cf081f2
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 16:28:12 2024 +0200

    My ReadMeFile

commit 51e294b8859afb6b999fcf334338247121b4cadc
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 16:22:29 2024 +0200

    Stashed files

commit ca2ee16f5ae471cdc28cb52a30d2051429620240 (origin/dev, dev)
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 16:14:23 2024 +0200

    Renaming files

commit c263dc452d3c05230f3c7963d1c43907e6a7fe76
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 16:13:30 2024 +0200

    Adding files

commit 1c3d0758d53794cefb509b3c290c039dcec27be7

    Renaming files


    Renaming files

commit c263dc452d3c05230f3c7963d1c43907e6a7fe76
Author: Beyla Irakoze <beylaruz@gmail.com>     
Date:   Mon Apr 22 16:13:30 2024 +0200

    Adding files

commit 1c3d0758d53794cefb509b3c290c039dcec27be7
Author: Beyla Ruzindana Irakoze <142901020+beylar@users.noreply.github.com>
Date:   Mon Apr 22 16:10:58 2024 +0200

    Initial commit
~
~
~
~
~

    Renaming files

commit c263dc452d3c05230f3c7963d1c43907e6a7fe76
Author: Beyla Irakoze <beylaruz@gmail.com>     
Date:   Mon Apr 22 16:13:30 2024 +0200

    Adding files

commit 1c3d0758d53794cefb509b3c290c039dcec27be7
Author: Beyla Ruzindana Irakoze <142901020+beylar@users.noreply.github.com> 
Date:   Mon Apr 22 16:10:58 2024 +0200

    Initial commit
(END)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/contact-page)
$ git cherry-pick
usage: git cherry-pick [--edit] [-n] [-m <parent-number>] [-s] [-x] [--ff]
                       [-S[<keyid>]] <commit>...
   or: git cherry-pick (--continue | --skip | --abort | --quit)

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    --skip                skip current commit and continue
    --[no-]cleanup <mode> how to strip spaces and #comments from message    
    -n, --no-commit       don't automatically commit
    --commit              opposite of --no-commit
    -e, --[no-]edit       edit the commit message
    -s, --[no-]signoff    add a Signed-off-by trailer
    -m, --[no-]mainline <parent-number>
                          select mainline parent
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --[no-]strategy <strategy>
                          merge strategy
    -X, --[no-]strategy-option <option>
                          option for merge strategy
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit
    -x                    append commit name
    --[no-]ff             allow fast-forward
    --[no-]allow-empty    preserve initially empty commits
    --[no-]allow-empty-message
                          allow commits with empty messages
    --[no-]keep-redundant-commits
                          keep redundant, empty commits

```
```bash
thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/contact-page)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/contact-page)
$ git commit -m "Changes from contact page"
[ft/contact-page 57ce879] Changes from contact page
 1 file changed, 1 insertion(+)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 414 bytes | 69.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.       
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:  
remote:      https://github.com/beylar/Gym-Git-Practices/pull/new/ft/contact-page
remote:
To https://github.com/beylar/Gym-Git-Practices.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/contact-page)
$ git branch ft/faq-page

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/contact-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/faq-page)
$ cd practice
bash: cd: practice: No such file or directory

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/faq-page)
$ touch faq.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/faq-page)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/faq-page)
$ git commit -m "My faq file and changes"
[ft/faq-page 8ec310e] My faq file and changes
 1 file changed, 11 insertions(+)
 create mode 100644 practice/faq.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 526 bytes | 47.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.        
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:      
remote:      https://github.com/beylar/Gym-Git-Practices/pull/new/ft/faq-page
remote:
To https://github.com/beylar/Gym-Git-Practices.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices/practice (main)
$git revert 76a811c6b82cf59857af43a5a0327b788efe6316
[ft/faq-page 33bc7ca] Revert "added the team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/team-page)   
$ git add . 

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/team-page)
$ git commit -m "Team page reverted by hash"
[ft/team-page 9057c8d] Team page reverted by hash 
 2 files changed, 2 insertions(+), 24 deletions(-)
 delete mode 100644 practice/team.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.    
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 366 bytes | 91.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.       
To https://github.com/beylar/Gym-Git-Practices.git
   701b7bd..9057c8d  ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

```

### Exercise 2
```bash
thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git checkout -f ft/faq-page
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/faq-page)
$ git branch ft/home-page-redesign

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/faq-page)
$ git checkout -f main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git commit -m "Changes and Commit"
[main 75aedbe] Changes and Commit
 2 files changed, 229 insertions(+), 1 deletion(-)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git push origin main
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 2.22 KiB | 189.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.       
To https://github.com/beylar/Gym-Git-Practices.git
   d5b61e7..75aedbe  main -> main


thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git commit -m "My readME"
[main 4f562fb] My readME
 1 file changed, 38 insertions(+), 1 deletion(-)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 568 bytes | 142.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.        
To https://github.com/beylar/Gym-Git-Practices.git
   75aedbe..4f562fb  main -> main

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (main)
$ git checkout -f "ft/home-page-redesign"
Switched to branch 'ft/home-page-redesign'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/home-page-redesign|REBASE 1/2)
$ git rebase --continue
Successfully rebased and updated refs/heads/ft/home-page-redesign.

hegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/home-page-redesign)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/home-page-redesign)
$ git commit -m "Rebased"
On branch ft/home-page-redesign
nothing to commit, working tree clean

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/home-page-redesign)
$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 532 bytes | 66.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.        
To https://github.com/beylar/Gym-Git-Practices.git
   d5b61e7..91df030  ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

   ```

## Bundle 4
### Exercise 1
``` bash
   thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Gym-Git-Practices (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PS C:\Users\thegym\Desktop\Practice-Git> git clone https://github.com/beylar/Gym-new-repo.git
Cloning into 'Gym-new-repo'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop
$ cd Practice-Git/

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git
$ cd Gym-new-repo/

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (main)   
$ touch home.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (main)   
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (main)   
$ git commit -m "My home page in git copy repo"
[main d9889b1] My home page in git copy repo
 1 file changed, 11 insertions(+)
 create mode 100644 home.html

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (main)   
$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 445 bytes | 111.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/beylar/Gym-new-repo.git
   2794505..d9889b1  main -> main
```

### Exercise 2
```bash
 thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (main)   
$ git checkout -f ft/footer
Switched to branch 'ft/footer'
Your branch is up to date with 'origin/ft/footer'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/footer)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/footer)
$ git commit -m "My footer file"
[ft/footer f5593ac] My footer file
 1 file changed, 1 insertion(+), 1 deletion(-)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/footer)
$ git push --set-upstream origin footer
error: src refspec footer does not match any
error: failed to push some refs to 'https://github.com/beylar/Gym-new-repo.git'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/footer)
$ git push --set-upstream origin ft/footer
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 354 bytes | 177.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.        
To https://github.com/beylar/Gym-new-repo.git
   d9889b1..f5593ac  ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/footer)
$ git checkout -f main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (main)   
$ git branch ft/sqashing

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (main)   
$ git checkout -f ft/sqashing
Switched to branch 'ft/sqashing'

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/sqashing)
$ git merge --squash ft/footer
Auto-merging home.html
Squashed commit of the following:

commit f5593acfedbce3dbb4fc27323e9c39e7c05673b7
Author: Beyla Irakoze <beylaruz@gmail.com>
Date:   Mon Apr 22 21:22:06 2024 +0200

    My footer file

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/sqashing)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/sqashing)
$ git commit -m "Footer changes Squashing"
[ft/sqashing ec67381] Footer changes Squashing
 1 file changed, 2 insertions(+), 1 deletion(-)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/Practice-Git/Gym-new-repo (ft/sqashing)
$ git push --set-upstream origin ft/sqashing
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 948 bytes | 105.00 KiB/s, done.
Total 9 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.        
To https://github.com/beylar/Gym-new-repo.git
   d9889b1..ec67381  ft/sqashing -> ft/sqashing
branch 'ft/sqashing' set up to track 'origin/ft/sqashing'.
```

## Bundle 5
### Exercise 2
```bash
 C:\Users\thegym\Desktop> git clone https://github.com/beylar/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (14/14), done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 93
Receiving objects: 100% (107/107), 1.95 MiB | 2.51 MiB/s, done.
Resolving deltas: 100% (5/5), done.

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/git-cafe-exercise (main)
$ git add .

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/git-cafe-exercise (main)
$ git commit -m "My text Welcome"
[main 8a882df] My text Welcome
 1 file changed, 1 insertion(+), 1 deletion(-)

thegym@DESKTOP-3L2FSN6 MINGW64 ~/Desktop/git-cafe-exercise (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.    
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done. 
Writing objects: 100% (3/3), 323 bytes | 161.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.       
To https://github.com/beylar/git-cafe-exercise.git
   d1d3f9c..8a882df  main -> main
```

## Bundle 6
### Exercise 1
