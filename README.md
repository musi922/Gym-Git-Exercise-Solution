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


```