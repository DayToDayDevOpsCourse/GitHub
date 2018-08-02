# Day4: Practice: Please spend some time and practice github as mentioned below.

      1. Create a repo under your username with README & .gitignore file, and then add any maven project.

      2. Create a repo under your username WITHOUT README & .gitignore file, and then add any maven project.

      3. Try to give access to others on the repo which you created under your username.

      4. Create an organization. (Note: Org name is unique across the GitHub server).

      5. Create a repo under your username with README & .gitignore file, and then add any maven project. OR transfer the repo (your repo which you recently created under username) to organization.

      6. Add few people as OWNER.

      7. Give read access to some group of people on the repo.

      8. Give write access to some group of people on the repo.

      9. Give admin access to some group of people on the repo.

      10. Give write access to some group of people on the repo on particular branhc only (i.e., protect branch OR branch wise restriction).

      11. Transfer the repo from one organization to another org. (create another repo and practice on it)

      12. Transfer the repo from one organization to another username. (create another repo and practice on it)

      13. Detele a repo (create another repo and practice on it).

      14. Delete an Organization (create another org and practice on it).

      15. Change the default branch from master to other branch.

      16. Delete the master or anyother branch.

      17. Create a forked branch on local and push to the remote repo.

      18. Create an orphan branch on local and push to the remote repo.

      18. See the diff between two commit ids (Syntax: git diff commitID1 commitID2)

      19. Create and apply the patches (google for it if you don't get it).

      20. practice the commands: https://orga.cat/posts/most-useful-git-commands , https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html

        20.1. git show : https://git-scm.com/docs/git-show
        20.2. git log :  https://git-scm.com/docs/git-log
        20.3. git branch Or git branch -l Or git branch -v Or git branch -av
        20.4. git branch -a
        20.5. git branch -r
        20.6. git reset --hard origin/<branchName>   (do some local changes with AND without commit and then run this command, then see what happends)
        20.7. git reset --mixed origin/<branchName>  (do some local changes with AND without commit and then run this command, then see what happends)
        20.8. git reset --soft origin/<branchName>   (do some local changes with AND without commit and then run this command, then see what happends)
        20.9. Create tag and push tags, diff between tags, rename tags:
            20.9.1. Command to create tag: git tag -a <tagName> <commitID> -m "message here"
            20.9.2. Command to psuh tags to remote repo.
                20.9.2.1. git push origin <tagName>  --> to push this particular tag to remote github repo.
                20.9.2.2. git push --tags OR git push --tags origin <branchName> --> to push all the tags of particular branch.
            20.9.3. Differences between two tags (indirectly its difference between two commit-id): git diff <tagName1> <tagName2>
            20.9.4. Rename the tag steps: 
                20.9.4.1. git tag -l  --> list of tags, select a tag which one you wants to rename.
                20.9.4.2. git tag <newTagName> <oldTagName> --> rename tag.
                20.9.4.3. git tag -d <oldTagName> --> removing the old tag from local.
                20.9.4.4. git push origin :refs/tags/<oldTagName> --> removing the old tag from remote server.
                20.9.4.5. git push origin --tags --> pushing the local tags to remote server, so that the new server also pushed to remote server.

        20.10. Create an orphan branch steps.
            20.10.1. git checkout --orphan <newBranchName>
            20.10.2. git rm -rf .
            20.10.3. echo "new orphan branch" > README.md
            20.10.4. git add README.md
            20.10.5. git commit -a -m "adding new orphan branch"
            20.10.6. git push or git push origin <newBranchName>
        20.11. try this command: gitk
        20.12. try this command: git re-parse <branchName>
        20.13. try this command: git reflog
        20.14. try this command: git log --abbrev-commit --pretty=online
        20.15. try this command: git log -g <branchName>
        20.16. try this command: git log --pretty=format: '%h %s' --graph
        20.17. try this command: git log -4 --pretty=format: '%h %s'
        20.18. try this command: git log branch1..branch2
        20.19. Git clone particular branch: git clone -b <branchName> <gitURL> <destination>
        20.20. Steps to create a new forked branch: 
            20.20.1. git checkout -b <newBranch> : this will create a new branch with the source code of current branch.
            20.20.2. git push origin <newBranch> : pushing the new branch to remote github.
        20.21. Steps to rename the branch:
            20.21.1. git branch -m <new_branch_name> : if you wants to rename the currect checkout branch.
                 git branch -m <old_branch_name> <new_branch_name> : if you wants to rename the other branch than the currect checkout branch.
            20.21.2. git push origin :<old_branch_name> <new_branch_name> : remove the old one and push the new to remove.
        20.22. to see the remote GitHub repo URL: git remote -v   OR git remote show origin
        20.23. Steps to revert: Explanation with a scenario.
            20.23.1. There are few commits C1, C2, C3, C4, C5 on a repo/project (on a particular branch).
            20.23.2. Now, we wanted to revert our changes to C3 commit-id. i.e., make the C3 changes as latest code in a branch. Commit C4 created because of some changes made on the C3 commit code.
            20.23.3. To do this, we need to revert the commit-id C4. (the changes made between C3 & C4 needs to be reverted).
                 Command is: git revert C4 (ex: git revert <commit-id>). Its trying to reverting the changes made between C3 & C4. 
            20.23.4. Resolve the conflicts if any. (if there are any conflicts in any file(s), we have to resolve them and then run the command "git add <fileName>" OR "git add .").
            20.23.5. commit the local changes: git commit -m "Reverting the changes to C3 commit-id".
            20.23.6. push the local changes to remote: git push or git push origin <branchName>.
      21. Prepare a document with best practice on GitHub for Dev or other teams.
            For example,
            Assume, there is a commit revision like C1, C2 & C3 on your branch. Here C3 is the latest commit-id on your both local & remote branches.
            You & your team member started working at same time. You made some changes on your local and then committed LC4 (not yet pushed).
            Your team member made come changes locally and then committed and then pushed his local commit and then commit-id created as RC4. (remote commit 4).
            Now, if you look at your workspace, your local code is not the latest code. Because there is another remote commit-id Rc4 on the server.
            Now again, you are trying to push your local commit-id LC4 to remote, but its failing and showing some error message non-fast-forward (there is an option to force push but this force push disabled in real time, so force push is not recommended. But do force push and see what happens).
            If you want to push your local commits, first you needs to update local workspace make sure its sync with remote. "git pull origin branchName" to update your local workspace with remote changes.
            This time, the RC4 is trying to merge with your LC4 and then git created another commit-id MC5 (merge commit-id 5).
            Finally, "git push origin branchName" will works fine.

            Here you have to observe, why git is creating a merge commit-id?
                a. if you forgot to "pull" before you commit, a commit-id created locally with your changes.
                b. after that, When try push, its failing.
                c. If you try to "pull" now, the latest commit-id from remote will be merged with your local commit-id and then git creates a merge commit-id.
                d. You may face some conflicts when remote commit-id merged with your local commit-id (conflicts occured when only the changes made in same file, same line by other member too).
                e. To avoid merge commits, you better to pull before you commit your changes.

            What is the best solution/practice to avoid merge commits?

            21.1. Every time, please "pull" before you start working on your local workspace. i.e., before you made any chnages.
            21.2. Made your changes (but dont commit now).
            21.3. Please "pull" again once you are ready to commit.
            21.4. Resolve if any conflicts. (conflicts occured when only the changes made in same file, same line by other member too).
            21.5. "push" now.

            So, this is the best practice on GitHub for Dev or other teams. Please share me if you have any other ideas.

      22. GIT MERGE: I will share it to you soon.
            Case-1: Branch to branch merge (without skip any project or file).
            Case-2: Branch to branch merge (with skipping some of the projects/files).

      23. Git rebase: Rebase is to synch the brnaches in development & release cycle.

        Assume there are commints C1, C2, C3, C6 in master branch, and C4, C5 in feature branch.

        git checkout master
        git log --oneline (only the master branch commits you will see i.e., C1, C2, C3, C6)
        git checkout feature
        git log --oneline (only the feature branch commits you will see i.e., C1, C2, C3, C4, C5)
        git rebase master
        git log --oneline (all C1, to C6 commits will be added to feature branch)
        git checkout maser
        git merge feature (C1, to C6 all commits will be merged to master branch)
        now, both the branches are in synch.


      24. Git Clone to STS/Eclipse, and then commit, pull, switch, add new proj, push: I will share it to you soon.

      25. Synchronize workspace on STS/Eclipse: I will share it to you soon.

      26. Git reset vs revert vs rebase: I will share it to you soon.

      27. Save the credes in windows: git config --global credential.helper wincred

      === Preapre a document if you find something new and share with all our DevOps team members. ===
