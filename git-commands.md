### Git Commands

1. clone

```
git clone GitURL

git clone GitURL destinationPath

git clone -b <branchName> <gitURL> <destinationPath>

```

1. add

1. pull

1. commit

1. push

1. merge

1. cherry-pick 

1. fetch

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
