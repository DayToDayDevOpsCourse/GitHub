### Git Commands

1. clone

            git clone GitURL

            git clone GitURL destinationPath

            git clone -b <branchName> <gitURL> <destinationPath>

1. add

            git add file1 file1

            git add dir/

            git add .
            
            git add dir/ -v

1. fetch

            git fetch
            
            git fetch origin branchName

1. pull

            git pull
            
            git pull origin branchName
            
            git pull origin master
       
       fetch vs pull:
       
            local branche recent commitds are the in .git\refs\heads
            remote branche recent commitds are the in .git\refs\remotes
       
            Open all the files in notepad
            
            run the git command in the terminal - git fetch
            
            go to notepad and see which are the files are changed with commit ids - only the remove branch commit ids changed, and working tree will not be updated with remote chages
            
            now, run the git command in the terminal - git pull
            
            go to notepad and see which are the files are changed with commit ids - only the remove branch commit ids changed, and working tree will be updated with remote chages.

1. show

            git show or git show HEAD

1. commit

            git commit -m "commit message"

            git commit --amend -m "commit message"

            practice: 
            git show

            git log -3

            update the files

            git add .

            git commit -m "commit message"

            git show 

            git log -3

            update the files

            git add .

            git commit --amend -m "commit message"

            git log -3

            git show

1. push

            git push

            git push origin branchName

            practice:

            git checkout branch-1

            do some commit but don't push

            git checkout branch-2

            do some commit but don't push

            git push origin branch-1

            git push origin branch-2 or git push (since we are in the working tree branch-2)

1. merge

            git merge bracnhName
            
            git merge --abort (Abort the current conflict resolution process, and try to reconstruct the pre-merge state.)
            
            git merge --continue (After a git merge stops due to conflicts you can conclude the merge by running this command)

1. cherry-pick 

            git cherry-pick commit-id
            
            git cherry-pick commit-id-1..commit-id-2
            
            git cherry-pick --continue
            
            git cherry-pick --quit
            
            git cherry-pick --abort

1. config

1. log: Refer: https://www.atlassian.com/git/tutorials/git-log

            ```
            git log

            git log -3

            git log --oneline

            git log -p (if you want to see the actual changes in each file & each commit)

            git log --abbrev-commit --pretty=oneline

            git log --oneline --decorate

            git log --graph --oneline --decorate

            git log --pretty=format:"%cn committed %h on %cd"

            git shortlog or git shortlog -n (git shortlog sorts the output by author name, but you can also pass the -n option to sort by the number of commits per author.)

            git log --after="yesterday"

            git log --after="2019-01-30"

            git log --after="2019-1-28" --before="2019-01-30"

            git log --author="username"

            git log --author="user1\|uder2" (user1 or user2)

            git log --grep="commit message"

            git log -- filename.py filename.java

            git log -S"content" (search the code in the file)

            git log -G".*line.*" (If you want to search using a regular expression instead of a string, you can use the -G"<regex>" flag instead)

            git log master..branch-1 (The master..branch-1 range contains all of the commits that are in the branch-1 branch, but aren’t in the master branch. In other words, this is how far branch-1 has progressed since it forked off of master.)

            git log --no-merges (Filtering Merge Commits)

            git log --merges (lists the merge commits)

            ```

1. status

1. branch

1. show - it shows recent/head commit id changes

1. tag

1. reset

            ```
            git log -3

            git add .

            git commit -m "hard"

            git reset --hard origin/branchName

            git log -3

            git add .

            git commit -m "mixed"

            git reset --mixed origin/branchName

            git log -3

            ```

1. diff

            ```
            git diff commit-id-1..commit-id-2

            git diff commit-id-1 commit-id-2

            git diff --oneline --name-status commit-id-1

            git diff --oneline --name-status commit-id-1 HEAD

            git diff --oneline --name-status commit-id-1 commit-id-2

            git diff branch-1 branch-2

            git diff branch-1..branch-2

            git diff branch-1..branch-2 > diff-branch1-branch2.patch
            ```

1. checkout

1. rm

1. reflog

1. re-parse

1. remote 

1. revert 

1. rebase 

1. archive 

1. gitk
