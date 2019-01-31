### Git Commands

1. clone

1. add

1. pull

1. commit

1. push

1. merge

1. cherry-pick 

1. fetch

1. config

1. log

```
git log

git log --oneline

git log -p (if you want to see the actual changes in each file & each commit)

git log --abbrev-commit --pretty=oneline

git log --oneline --decorate

git log --graph --oneline --decorate

git log --pretty=format:"%cn committed %h on %cd"

git shortlog or git shortlog -n (git shortlog sorts the output by author name, but you can also pass the -n option to sort by the number of commits per author.)
```

1. status

1. branch

1. show

1. tag

1. reset

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
