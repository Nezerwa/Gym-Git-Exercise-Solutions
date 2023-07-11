# git exercise

## bundle 1

### exercise 
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