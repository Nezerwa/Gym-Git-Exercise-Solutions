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

## Bundle 3

## Exercise 2

```bash

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout -b 'ft/team-page'
Switched to a new branch 'ft/team-page'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add team.html

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m 'Add new changes'
[ft/team-page 2c45e90] Add new changes
 1 file changed, 25 insertions(+)
 create mode 100644 team.html

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 461 bytes | 461.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout -b 'ft/contact-page'
Switched to a new branch 'ft/contact-page'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit 2c45e90d47c66c15f2ceeee43cb75967304fa583 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Nezerwa <eligrand2000@gmail.com>
Date:   Wed Jul 26 10:51:13 2023 +0200

    Add new changes

commit 0d52b0fdec56ef318226ef17da313c2303d470c1 (origin/ft/service-redesign, ft/service-redesign)
Author: Nezerwa <eligrand2000@gmail.com>

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'


User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick 2c45e90d47c66c15f2ceeee43cb75967304fa583
[ft/contact-page 92f2cc8] Add new changes
 Date: Wed Jul 26 10:51:13 2023 +0200
 1 file changed, 25 insertions(+)
 create mode 100644 team.html


User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m 'add changes from team branch'
[ft/contact-page 307360c] add changes from team branch
 1 file changed, 3 insertions(+)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 693 bytes | 693.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add faq.html

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m 'add new changes'
[ft/faq-page f7a07a3] add new changes
 1 file changed, 14 insertions(+)
 create mode 100644 faq.html

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit 2c45e90d47c66c15f2ceeee43cb75967304fa583 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Nezerwa <eligrand2000@gmail.com>
Date:   Wed Jul 26 10:51:13 2023 +0200

    Add new changes

commit 0d52b0fdec56ef318226ef17da313c2303d470c1 (origin/ft/service-redesign, ft/service-redesign)
Author: Nezerwa <eligrand2000@gmail.com>

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git commit -m "commit changes"
On branch ft/faq-page
You are currently reverting commit 2c45e90.
  (all conflicts fixed: run "git revert --continue")
  (use "git revert --skip" to skip this patch)
  (use "git revert --abort" to cancel the revert operation)


User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m 'add changes'
[ft/team-page 212a524] add changes
 1 file changed, 25 deletions(-)
 delete mode 100644 team.html

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert 2c45e90d47c66c15f2ceeee43cb75967304fa583
CONFLICT (modify/delete): team.html deleted in parent of 2c45e90 (Add new changes) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 2c45e90... Add new changes
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git revert --continue
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

You are currently reverting commit 2c45e90.
  (all conflicts fixed: run "git revert --continue")
  (use "git revert --skip" to skip this patch)
  (use "git revert --abort" to cancel the revert operation)

nothing to commit, working tree clean

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git commit -m 'add changes'
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

You are currently reverting commit 2c45e90.
  (all conflicts fixed: run "git revert --continue")
  (use "git revert --skip" to skip this patch)
  (use "git revert --abort" to cancel the revert operation)

nothing to commit, working tree clean

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git revert 2c45e90d47c66c15f2ceeee43cb75967304fa583
CONFLICT (modify/delete): team.html deleted in parent of 2c45e90 (Add new changes) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 2c45e90... Add new changes
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page|REVERTING)
$ git commit -m 'revert'
[ft/faq-page d4dc952] revert
 1 file changed, 3 deletions(-)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 279 bytes | 279.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   f7a07a3..d4dc952  ft/faq-page -> ft/faq-page

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$

```

```bash

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add index.html

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'Add some changes to test'
[main 7f0c2ed] Add some changes to test
 1 file changed, 12 insertions(+), 7 deletions(-)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.


User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git commit -m 'add new changes'
[ft/home-page-redesign 714a5b7] add new changes
 1 file changed, 1 insertion(+)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 23, done.
Counting objects: 100% (23/23), done.
Delta compression using up to 12 threads
Compressing objects: 100% (20/20), done.
Writing objects: 100% (20/20), 4.45 KiB | 1.48 MiB/s, done.
Total 20 (delta 9), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (9/9), done.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$
```

## Bundle 4

## exercise 1

```bash

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)


User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git remote add git-copy https://github.com/Nezerwa/git-copy.git

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git add .

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git commit -m 'add changes'
[ft/home-page-redesign 45dfa63] add changes
 1 file changed, 1 insertion(+)

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git push --all
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 483 bytes | 483.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   9c1bee0..45dfa63  ft/home-page-redesign -> ft/home-page-redesign
   2c45e90..212a524  ft/team-page -> ft/team-page
   6102520..7f0c2ed  main -> main
 ! [rejected]        ft/faq-page -> ft/faq-page (non-fast-forward)
error: failed to push some refs to 'https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because a pushed branch tip is behind its remote
hint: counterpart. Check out this branch and integrate the remote changes
hint: (e.g. 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.


User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git push git-copy main
Enumerating objects: 37, done.
Counting objects: 100% (37/37), done.
Delta compression using up to 12 threads
Compressing objects: 100% (27/27), done.
Writing objects: 100% (37/37), 6.19 KiB | 6.19 MiB/s, done.
Total 37 (delta 12), reused 30 (delta 8), pack-reused 0
remote: Resolving deltas: 100% (12/12), done.
To https://github.com/Nezerwa/git-copy.git
 * [new branch]      main -> main

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

User@DESKTOP-441QGV2 MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$
```
