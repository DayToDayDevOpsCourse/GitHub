### Git Commands

1. clone

            git clone GitURL

            git clone GitURL destinationPath

            git clone -b <branchName> <gitURL> <destinationPath>

1. status

            git status

1. add

            git add file1 file1

            git add dir/

            git add .
            
            git add dir/ -v

1. rm

            git rm fileName
            
            git rm -rf .
            
            ex: git rm Dir/\*.txt ---> Removes all *.txt files from the index that are under the Documentation directory and any of its subdirectories.

1. fetch

            git fetch
            
            git fetch origin branchName

1. pull

            git pull
            
            git pull origin branchName
            
            git pull origin master
       
       fetch vs pull: practice
       
            local branche recent commitds are the in .git\refs\heads
            remote branche recent commitds are the in .git\refs\remotes
       
            Open all the files in notepad
            
            run the git command in the terminal - git fetch
            
            go to notepad and see which are the files are changed with commit ids - only the remove branch commit ids changed, and working tree will not be updated with remote chages
            
            now, run the git command in the terminal - git pull
            
            go to notepad and see which are the files are changed with commit ids - only the remove branch commit ids changed, and working tree will be updated with remote chages.

1. show

            git show or git show HEAD - it shows recent/head commit id changes

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

            git config --global user.email "you@example.com"

            git config --global user.name "Your Name"
            
            git config -e                                  
            
1. log: Refer: https://www.atlassian.com/git/tutorials/git-log

            git log

            git log -3

            git log --oneline

            git log -p (if you want to see the actual changes in each file & each commit)

            git log --abbrev-commit --pretty=oneline

            git log --oneline --decorate

            git log --graph --oneline --decorate

            git log --pretty=format:"%cn committed %h on %cd"
            
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

            git shortlog or git shortlog -n (git shortlog sorts the output by author name, but you can also pass the -n option to sort by the number of commits per author.)

            git reflog or git reflog show

1. branch

            git branch  or git branch -l
            
            git branch -v
            
            git branch -a
            
            git branch -av
            
            git branch -r
            
            git branch -vr
                        
1. tag

            git tag -a <tagName> <commitID> -m "message here"
            
            git push origin <tagName> --> to push this particular tag to remote github repo.
            
            git push --tags OR git push --tags origin <branchName> --> to push all the tags of particular branch.
            
            git diff <tagName1> <tagName2> --> Differences between two tags (indirectly its difference between two commit-id)
            
            git tag -l  --> list of tags, select a tag which one you wants to rename.
            
            git tag <newTagName> <oldTagName> --> rename tag.
            
            git tag -d <oldTagName> --> removing the old tag from local.
            
            git push origin :refs/tags/<oldTagName> --> removing the old tag from remote server.
            
            git push origin --tags --> pushing the local tags to remote server, so that the new server also pushed to remote server.
            
            git checkout tags/<tagName> --> Checkout the tag

1. reset

            git log -3

            git add .

            git commit -m "hard"

            git reset --hard origin/branchName

            git log -3

            git add .

            git commit -m "mixed"

            git reset --mixed origin/branchName

            git log -3

1. diff

            git diff commit-id-1..commit-id-2

            git diff commit-id-1 commit-id-2

            git diff --oneline --name-status commit-id-1

            git diff --oneline --name-status commit-id-1 HEAD

            git diff --oneline --name-status commit-id-1 commit-id-2

            git diff branch-1 branch-2

            git diff branch-1..branch-2

            git diff branch-1..branch-2 > diff-branch1-branch2.patch
            
            git diff <tagName1> <tagName2> --> Differences between two tags (indirectly its difference between two commit-id)
            
            git diff --name-only [commit-id|branchName|tagName] [commit-id|branchName|tagName]

1. checkout

            git checkout branchName
            
            Created  new forked branch:
            git checkout -b <newBranch>
            git push origin <newBranch>
            
            Created  new orphan branch:
            git checkout --orphan <newBranchName>            
            git rm -rf .            
            echo "new orphan branch" > README.md
            git add README.md
            git commit -a -m "adding new orphan branch"
            git push or git push origin <newBranchName>
            
            rename a branch:
            git branch -m <new_branch_name>
            git branch -m <old_branch_name> <new_branch_name>
            git push origin :<old_branch_name> <new_branch_name>            

1. rev-parse

            git rev-parse --> it will return the latest commitid
            
            git rev-parse --show-toplevel --> it will return the git project/repo path
            
1. rev-list
            
            git rev-list --all
            
            git rev-list --all --max-count=5
            
            git rev-list branch-1...branch-2
            
1. remote

            git remote -v
            
            ex:
            echo "# sample" >> README.md
            git init
            git add README.md
            git commit -m "first commit"
            git remote add origin https://github.com/DayToDayDevOpsCourse/sample.git
            git push -u origin master

1. revert 

            git revert commit-id

1. archive (try this on linux machine)
            
            ex: git archive --format=zip --output=zipName.zip HEAD:dir/subDir/

            ex: https://github.com/DayToDayDevOpsCourse/GitHubDayToDayCourse/blob/master/Day4/sampleDir/sample.txt

1. gitk

## Examples:

1. Clone only the subfolder and push


            git clone --no-checkout gitURL

            cd gitrepo

            git config core.sparseCheckout true

            echo "src/main/*"> .git/info/sparse-checkout

            git checkout master
            
            Update the code
            
            git status

            git add modified-files-path (don't use git add . )
            
            git status

            git commit -m "local commit"

            git push

1. Best Practice to Dev team or who frequently commiting code changes

           Eclipse/STS:

            1. right click on the git repo in eclipse/sts

            2. choose synchronize workspace 

            3. It will open a window with all the incoming changes (click on the modified files to see the changes)

            4. pull the changes if you want to update your workspace with those new changes

            5. go ahead with your development (your code commit & push)
            
          Command:
          
            1. git fetch first - git fetch origin [branch-name]
            
            2. git diff [branch-name] origin/[branch-name] 
            
            3. git pull
            
            4. go ahead with your development (your code commit & push)

1. Restore: Moved all the files from unstaged area to staged area, and realized that one file wants to move back to unstaged area, then use git restore command.

            1. git clone repo
            2. git add some file file1.txt file2.txt
            3. git status
            4. git restore --staged file1.txt
            5. git status
            
