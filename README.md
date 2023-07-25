# git exercise

## bundle 1

### exercise1

```bash
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git init
Initialized empty Git repository in C:/Users/Eligrand/Gym Git Exercise Solutions/.git/
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git add .\README.md
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git commit -m 'Add README file'
[master (root-commit) 082d98f] Add README file
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git remote add origin https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git branch
* master
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git branch -m master main
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git add .\index.html
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git commit -m 'Add html file'
[main 63526d9] Add html file
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git push -u origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 636 bytes | 159.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git checkout dev
Switched to branch 'dev'
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git branch -d test
Deleted branch test (was 63526d9).
PS C:\Users\Eligrand\Gym Git Exercise Solutions>

```

### exercise 2

```bash

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git add .\home.html
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git stash
Saved working directory and index state WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git stash list
stash@{0}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git add .\about.html
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git stash
Saved working directory and index state WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git add .\team.html
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git stash
Saved working directory and index state WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
PS C:\Users\Eligrand\Gym Git Exercise Solutions> git stash list
stash@{0}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
stash@{1}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
ev
stash@{1}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
stash@{2}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
(END)

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
stash@{1}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
stash@{2}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Sol

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{1} (f44cb017da9f1b4c4f28c13d09b91e1bfdbc708c)

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git  add .

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git commit -m 'Add new changes'
[dev ca44eef] Add new changes
 2 files changed, 38 insertions(+), 1 deletion(-)
 create mode 100644 about.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
stash@{1}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev
Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: ca44eef Add new changes
stash@{1}: WIP on dev: c983edc Merge branch 'main' of https://github.com/Nezerwa/Gym-Git-Exercise-Solutions into dev

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{1} (099cc78142aad70d9afafc4cc88d3b19b7eae8aa)

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git reset --hard
HEAD is now at ca44eef Add new changes

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git status
On branch dev
nothing to commit, working tree clean
Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$
```

## Bundle2

## Exercise 1

```bash

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (ft/bundle-2)
$ git add services.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (ft/bundle-2)
$ git commit -m 'Add services page'
[ft/bundle-2 927e888] Add services page
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 448 bytes | 89.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

Eligrand@Eligrand-Pc MINGW64 ~/Gym Git Exercise Solutions (ft/bundle-2)
$
```

# exercise 2

```bash



User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git pull origin main
From https://github.com/Nezerwa/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Already up to date.


User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout -b  ft/service-redesign
Switched to a new branch 'ft/service-redesign'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m 'Add changes on service.html file'
[ft/service-redesign 620931a] Add changes on service.html file
 1 file changed, 8 insertions(+), 7 deletions(-)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin  ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 375 bytes | 375.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add services.html

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m "Add another changes on service.html"
[main 6102520] Add another changes on service.html
 1 file changed, 8 insertions(+), 7 deletions(-)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 388 bytes | 388.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   ffbaf79..6102520  main -> main

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff ft/service-redesign..main
diff --git a/services.html b/services.html
index 84759fe..e250312 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
   </head>
   <body>
     <h1>justing for testing purpose</h1>

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git merge main
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m 'Fix merge conflict'
[ft/service-redesign 4557a60] Fix merge conflict
 2 files changed, 93 insertions(+), 13 deletions(-)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 13, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 1.49 KiB | 1.49 MiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   620931a..4557a60  ft/service-redesign -> ft/service-redesign

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$

```
