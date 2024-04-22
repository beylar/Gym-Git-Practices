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
