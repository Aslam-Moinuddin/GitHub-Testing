# GitHub-Testing
Aslam Moin
and team
PS C:\Users\aslam\Desktop\Github-Testing> git clone https://github.com/Aslam-Moinuddin/GitHub-Testing.git .
Cloning into '.'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\aslam\Desktop\Github-Testing> git add .
PS C:\Users\aslam\Desktop\Github-Testing> git commit -m "Content added to readme.md"
[main 064283c] Content added to readme.md
 1 file changed, 1 insertion(+)
PS C:\Users\aslam\Desktop\Github-Testing> git log
commit 064283cff4a5bdd0cd97e17f27be487025ee12a0 (HEAD -> main)
Author: Aslam <aslammoinuddin4@gmail.com>
Date:   Wed Jul 24 17:06:44 2024 +0530

    Content added to readme.md

commit bba796422a36e68fed37853f82049e8cab7e8ffc (origin/main, origin/HEAD)
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:00:32 2024 +0530

    Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git remvote -v 
git: 'remvote' is not a git command. See 'git --help'.

The most similar command is
        remote
PS C:\Users\aslam\Desktop\Github-Testing> git remote -v
origin  https://github.com/Aslam-Moinuddin/GitHub-Testing.git (fetch)
origin  https://github.com/Aslam-Moinuddin/GitHub-Testing.git (push)
PS C:\Users\aslam\Desktop\Github-Testing> git push origin main 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 279 bytes | 279.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/GitHub-Testing.git
   bba7964..064283c  main -> main
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
064283c (HEAD -> main, origin/main, origin/HEAD) Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git log
commit 064283cff4a5bdd0cd97e17f27be487025ee12a0 (HEAD -> main, origin/main, origin/HEAD)
Author: Aslam <aslammoinuddin4@gmail.com>
Date:   Wed Jul 24 17:06:44 2024 +0530

    Content added to readme.md

commit bba796422a36e68fed37853f82049e8cab7e8ffc
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:00:32 2024 +0530

    Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git remote add upstream
usage: git remote add [<options>] <name> <url>

    -f, --[no-]fetch      fetch the remote branches
    --[no-]tags           import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --[no-]track <branch>
                          branch(es) to track
    -m, --[no-]master <branch>
                          master branch
    --[no-]mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from

PS C:\Users\aslam\Desktop\Github-Testing> git remote add upstream https://github.com/Aslam-moin/GitHub-Testing.git
PS C:\Users\aslam\Desktop\Github-Testing> git remote -v
origin  https://github.com/Aslam-Moinuddin/GitHub-Testing.git (fetch)
origin  https://github.com/Aslam-Moinuddin/GitHub-Testing.git (push)
upstream        https://github.com/Aslam-moin/GitHub-Testing.git (fetch)
upstream        https://github.com/Aslam-moin/GitHub-Testing.git (push)
PS C:\Users\aslam\Desktop\Github-Testing> git fetch upstream main
remote: Enumerating objects: 8, done.
remote: Counting objects: 100% (8/8), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), 1.77 KiB | 39.00 KiB/s, done.
From https://github.com/Aslam-moin/GitHub-Testing
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> upstream/main
PS C:\Users\aslam\Desktop\Github-Testing> git fetch --all --prune
Fetching origin
Fetching upstream
PS C:\Users\aslam\Desktop\Github-Testing> git branch
* main
PS C:\Users\aslam\Desktop\Github-Testing> git log
commit 064283cff4a5bdd0cd97e17f27be487025ee12a0 (HEAD -> main, origin/main, origin/HEAD)
Author: Aslam <aslammoinuddin4@gmail.com>
Date:   Wed Jul 24 17:06:44 2024 +0530

    Content added to readme.md

commit bba796422a36e68fed37853f82049e8cab7e8ffc
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:00:32 2024 +0530

    Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git reset --hard upstream
fatal: ambiguous argument 'upstream': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
PS C:\Users\aslam\Desktop\Github-Testing> git reset --hard upstream/main
HEAD is now at 488df3d Update README.md
PS C:\Users\aslam\Desktop\Github-Testing> git log
commit 488df3d21e8d283126c6ce76104ef999dc0a4e57 (HEAD -> main, upstream/main)
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:13:22 2024 +0530

    Update README.md

commit bf7fa63e0538ef257f0d1b7524ea98fb3e0c05b2
Merge: bba7964 064283c
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:10:03 2024 +0530

    Merge pull request #1 from Aslam-Moinuddin/main

    Content added to readme.md

commit 064283cff4a5bdd0cd97e17f27be487025ee12a0 (origin/main, origin/HEAD)
Author: Aslam <aslammoinuddin4@gmail.com>
Date:   Wed Jul 24 17:06:44 2024 +0530

    Content added to readme.md

commit bba796422a36e68fed37853f82049e8cab7e8ffc
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:00:32 2024 +0530

    Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> 
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
488df3d (HEAD -> main, upstream/main) Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c (origin/main, origin/HEAD) Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git pull origin main
From https://github.com/Aslam-Moinuddin/GitHub-Testing
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git push origin main
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 1.79 KiB | 1.79 MiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/GitHub-Testing.git
   064283c..488df3d  main -> main
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git fetch --all --prune
Fetching origin
Fetching upstream
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 923 bytes | 16.00 KiB/s, done.
From https://github.com/Aslam-moin/GitHub-Testing
   488df3d..984080b  main       -> upstream/main
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
488df3d (HEAD -> main, origin/main, origin/HEAD) Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git pull origin main
From https://github.com/Aslam-Moinuddin/GitHub-Testing
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\aslam\Desktop\Github-Testing> git fetch upstream 
PS C:\Users\aslam\Desktop\Github-Testing> git merge upstream/main
Updating 488df3d..984080b
Fast-forward
 index.html | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 index.html
PS C:\Users\aslam\Desktop\Github-Testing> git push origin main
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/GitHub-Testing.git
   488df3d..984080b  main -> main
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
984080b (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline --graph --all
* 984080b (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create index.html
* 488df3d Update README.md
*   bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
|\
| * 064283c Content added to readme.md
|/
* bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git log origin/main --oneline
984080b (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git pull origin main
From https://github.com/Aslam-Moinuddin/GitHub-Testing
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\aslam\Desktop\Github-Testing> git fetch origin     
PS C:\Users\aslam\Desktop\Github-Testing> git reset --hard origin/main
HEAD is now at 984080b Create index.html
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
984080b (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git log upstream/main --oneline
984080b (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git fetch upstream
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 924 bytes | 26.00 KiB/s, done.
From https://github.com/Aslam-moin/GitHub-Testing
   984080b..a9fa260  main       -> upstream/main
PS C:\Users\aslam\Desktop\Github-Testing> git merge upstream
merge: upstream - not something we can merge
PS C:\Users\aslam\Desktop\Github-Testing> git merge upstream/main
Updating 984080b..a9fa260
Fast-forward
 styles.css | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 styles.css
PS C:\Users\aslam\Desktop\Github-Testing> git status    
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
a9fa260 (HEAD -> main, upstream/main) Create styles.css
984080b (origin/main, origin/HEAD) Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git push origin main
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/GitHub-Testing.git
   984080b..a9fa260  main -> main
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
a9fa260 (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create styles.css
984080b Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git log
commit a9fa26050db9864664cbbcf9ee2ec1d8ca97874a (HEAD -> main, upstream/main, origin/main, origin/HEAD)
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:43:18 2024 +0530

    Create styles.css

commit 984080b102532dddf1f71006e556519ab0e99ba6
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:30:03 2024 +0530

    Create index.html

commit 488df3d21e8d283126c6ce76104ef999dc0a4e57
Author: Aslam-moin <aslammoinuddin04@gmail.com>
Date:   Wed Jul 24 17:13:22 2024 +0530
PS C:\Users\aslam\Desktop\Github-Testing> git log --oneline
a9fa260 (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create styles.css
984080b Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git upstream/main log--oneline
git: 'upstream/main' is not a git command. See 'git --help'.
PS C:\Users\aslam\Desktop\Github-Testing> git log upstream/main --oneline
a9fa260 (HEAD -> main, upstream/main, origin/main, origin/HEAD) Create styles.css
984080b Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git pull upstream main
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 1.10 KiB | 112.00 KiB/s, done.
From https://github.com/Aslam-moin/GitHub-Testing
 * branch            main       -> FETCH_HEAD
   a9fa260..c1fdb51  main       -> upstream/main
Updating a9fa260..c1fdb51
Fast-forward
 index.html | 12 +++++++++++-
 1 file changed, 11 insertions(+), 1 deletion(-)
PS C:\Users\aslam\Desktop\Github-Testing> git log upstream/main --oneline
c1fdb51 (HEAD -> main, upstream/main) Update index.html
a9fa260 (origin/main, origin/HEAD) Create styles.css
984080b Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git merge upstream/main 
Already up to date.
PS C:\Users\aslam\Desktop\Github-Testing> git log origin --oneline
a9fa260 (origin/main, origin/HEAD) Create styles.css
984080b Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> git status          
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\Github-Testing> git push origin main
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/GitHub-Testing.git
   a9fa260..c1fdb51  main -> main
PS C:\Users\aslam\Desktop\Github-Testing> git log origin --oneline
c1fdb51 (HEAD -> main, upstream/main, origin/main, origin/HEAD) Update index.html
a9fa260 Create styles.css
984080b Create index.html
488df3d Update README.md
bf7fa63 Merge pull request #1 from Aslam-Moinuddin/main
064283c Content added to readme.md
bba7964 Create README.md
PS C:\Users\aslam\Desktop\Github-Testing> 