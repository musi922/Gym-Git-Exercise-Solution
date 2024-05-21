# Gym-Git-Exercise-Solution
## Challenge 1
```bash
Rich-kid@Richard MINGW64 ~/Desktop/thegymgit
$ echo "# Gym-Git-Exercise-Solution" >> README.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit
$ git init
Initialized empty Git repository in C:/Users/irako/Desktop/thegymgit/.git/

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (master)
$ git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (master)
$ git commit -m "first commit"
[master (root-commit) 60559a8] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (master)
$ git branch -M main

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git remote add origin https://github.com/musi922/Gym-Git-Exercise-Solution.git

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 240 bytes | 80.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solution.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ touch test{1..4}.md
git add test1.md && git commit -m "chore: Create initial file"
git add test2.md && git commit -m "chore: Create another file"
git add test3.md && git commit -m "chore: Create third and fourth files"
[main 060eee8] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
[main a95421d] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
[main ad9c340] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git log
commit ad9c340280916ebc400b8b7a7777187e7e847f79 (HEAD -> main)
Author: Richard <richardmusime6@gmail.com>
Date:   Tue May 21 14:39:28 2024 +0200

    chore: Create third and fourth files

commit a95421de3103f901ffb8c445df4d58bc7d1b2e23
Author: Richard <richardmusime6@gmail.com>
Date:   Tue May 21 14:39:28 2024 +0200

    chore: Create another file

commit 060eee87c257aff2b381fa3f32658e10e42bdc08
Author: Richard <richardmusime6@gmail.com>
Date:   Tue May 21 14:39:27 2024 +0200

    chore: Create initial file

commit 60559a80a34b3792c35efece34b4d1a60304cea1 (origin/main)
Author: Richard <richardmusime6@gmail.com>
Date:   Tue May 21 14:38:53 2024 +0200

    first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add test4.md



```
### challenge 2 and 3

```bash
Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git commit --amend -m "chore: Create third, fourth, and missing fifth files"
[main 49327f2] chore: Create third, fourth, and missing fifth files
 Date: Tue May 21 14:39:28 2024 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$
Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase -i HEAD~3
Successfully rebased and updated refs/heads/main.

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase -i HEAD~3
[detached HEAD a73272b] chore: Create second file
 Date: Tue May 21 14:39:28 2024 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$
```

### challenge 4

```bash

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git log --oneline
66f2b08 (HEAD -> main, origin/main) chore: Create initial file with second file
a73272b chore: Create second file
060eee8 chore: Create initial file
60559a8 first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git reset HEAD^ --soft

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add path/to/third/file
fatal: pathspec 'path/to/third/file' did not match any files

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add test3.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git commit -m "Create Third File"
[main 521e2bd] Create Third File
 3 files changed, 125 insertions(+)
 create mode 100644 test3.md
 create mode 100644 test4.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add test4.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git commit -m "Create fourth file"
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.

nothing to commit, working tree clean


Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git push origin main --force
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.46 KiB | 499.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solution.git
 + 66f2b08...521e2bd main -> main (forced update)

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
```

### challenge 5
```bash

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git log --oneline
66f2b08 (HEAD -> main, origin/main) chore: Create initial file with second file
a73272b chore: Create second file
060eee8 chore: Create initial file
60559a8 first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git reset HEAD^ --soft

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add path/to/third/file
fatal: pathspec 'path/to/third/file' did not match any files

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add test3.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git commit -m "Create Third File"
[main 521e2bd] Create Third File
 3 files changed, 125 insertions(+)
 create mode 100644 test3.md
 create mode 100644 test4.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add test4.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git commit -m "Create fourth file"
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.

nothing to commit, working tree clean

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

nothing to commit, working tree clean

pick a73272b chore: Create second file
# This is a combination of 2 commits.
Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git push origin main --force
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.46 KiB | 499.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solution.git
 + 66f2b08...521e2bd main -> main (forced update)

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase -i HEAD~2
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git stash
Saved working directory and index state WIP on main: 521e2bd Create Third File

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase -i HEAD~2
[detached HEAD d88083c] chore: Create second file and third
 Date: Tue May 21 14:39:28 2024 +0200
 4 files changed, 125 insertions(+)
 create mode 100644 test2.md
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase --continue
fatal: no rebase in progress

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git push origin main --force
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.49 KiB | 381.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solution.git
 + 521e2bd...d88083c main -> main (forced update)

```
### challenge 6
```bash

```
### challenge 6
```bash
$ touch unwanted.txt

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git add unwanted.txt

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git commit -m "Unwanted commit"
[main fd5c0d5] Unwanted commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 unwanted.txt

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase -i HEAD~2
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git stash
Saved working directory and index state WIP on main: fd5c0d5 Unwanted commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase --continue
fatal: no rebase in progress

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git push origin main --force
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 852 bytes | 426.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/musi922/Gym-Git-Exercise-Solution.git
   d88083c..39f6eef  main -> main

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git push origin main --force


```
### challenge 7

```bash
Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git rebase -i --root
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply 39f6eef... Adding Readme file
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply 39f6eef... Adding Readme file

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main|REBASE 3/8)

```
### challenge 8
```bash
Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git checkout -b ft/branch
Switched to a new branch 'ft/branch'

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (ft/branch)
$ echo "This is test 5" > test5.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (ft/branch)
$ git add test5.md
warning: in the working copy of 'test5.md', LF will be replaced by CRLF the next time Git touches it

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (ft/branch)
$ git commit -m "Implemented test 5"
[ft/branch 465b7c2] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (ft/branch)
$ git log --oneline
465b7c2 (HEAD -> ft/branch) Implemented test 5
5ca4839 (main) Adding Readme
c36313e adding Readme file
9d9dd61 adding Readme file
33464e3 Adding Readme file
39f6eef (origin/main) Adding Readme file
d88083c chore: Create second file and third
060eee8 chore: Create initial file
60559a8 first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (ft/branch)
$ abcdef1 Implemented test 5
bash: abcdef1: command not found

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (ft/branch)
$ git checkout main
M       README.md
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git cherry-pick 465b7c2
[main 4eb8ff1] Implemented test 5
 Date: Tue May 21 16:05:55 2024 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
```

### challenge 9

```bash

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git log --graph --oneline
* f96c347 (HEAD -> main, origin/main) Adding the Cherry pick Readme feature
* 4eb8ff1 Implemented test 5
* 5ca4839 Adding Readme
* c36313e adding Readme file
* 9d9dd61 adding Readme file
* 33464e3 Adding Readme file
* 39f6eef Adding Readme file
* d88083c chore: Create second file and third
* 060eee8 chore: Create initial file
* 60559a8 first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git log --graph --oneline --decorate
* f96c347 (HEAD -> main, origin/main) Adding the Cherry pick Readme feature
* 4eb8ff1 Implemented test 5
* 5ca4839 Adding Readme
* c36313e adding Readme file
* 9d9dd61 adding Readme file
* 33464e3 Adding Readme file
* 39f6eef Adding Readme file
* d88083c chore: Create second file and third
* 060eee8 chore: Create initial file
* 60559a8 first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git log --graph --oneline --decorate --all
* f96c347 (HEAD -> main, origin/main) Adding the Cherry pick Readme feature
* 4eb8ff1 Implemented test 5
| * 465b7c2 (ft/branch) Implemented test 5
|/
* 5ca4839 Adding Readme
* c36313e adding Readme file
* 9d9dd61 adding Readme file
* 33464e3 Adding Readme file
| *   f00bef6 (refs/stash) WIP on main: fd5c0d5 Unwanted commit
| |\
| | * e854120 index on main: fd5c0d5 Unwanted commit
| |/
| * fd5c0d5 Unwanted commit
|/
* 39f6eef Adding Readme file
* d88083c chore: Create second file and third
* 060eee8 chore: Create initial file
* 60559a8 first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git log --graph --decorate --all --pretty=oneline --abbrev-commit
* f96c347 (HEAD -> main, origin/main) Adding the Cherry pick Readme feature
* 4eb8ff1 Implemented test 5
| * 465b7c2 (ft/branch) Implemented test 5
|/
* 5ca4839 Adding Readme
* c36313e adding Readme file
* 9d9dd61 adding Readme file
* 33464e3 Adding Readme file
| *   f00bef6 (refs/stash) WIP on main: fd5c0d5 Unwanted commit
| |\
| | * e854120 index on main: fd5c0d5 Unwanted commit
| |/
| * fd5c0d5 Unwanted commit
|/
* 39f6eef Adding Readme file
* d88083c chore: Create second file and third
* 060eee8 chore: Create initial file
* 60559a8 first commit

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$
```
### challenge
```bash

Rich-kid@Richard MINGW64 ~/Desktop/thegymgit (main)
$ git reflog
f96c347 (HEAD -> main, origin/main) HEAD@{0}: commit: Adding the Cherry pick Readme feature
4eb8ff1 HEAD@{1}: cherry-pick: Implemented test 5
5ca4839 HEAD@{2}: checkout: moving from ft/branch to main
465b7c2 (ft/branch) HEAD@{3}: commit: Implemented test 5
5ca4839 HEAD@{4}: checkout: moving from main to ft/branch
5ca4839 HEAD@{5}: rebase (abort): returning to refs/heads/main
060eee8 HEAD@{6}: rebase: fast-forward
60559a8 HEAD@{7}: rebase: fast-forward
b7aa057 HEAD@{8}: rebase (start): checkout b7aa0579b931e9ad734851b85af1c91d20a1d8c5
5ca4839 HEAD@{9}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{10}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{11}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{12}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{13}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{14}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{15}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{16}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{17}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{18}: rebase (abort): returning to refs/heads/main
5ca4839 HEAD@{19}: commit: Adding Readme
c36313e HEAD@{20}: commit: adding Readme file
:
```


