# Daily Practice with Git



Step-1. Update the workspace before you start working on your local git repo/branch.

	1.1. Synch the local git branch with remote git branch.
        1.1.1. Go to Git perspective --> Right click on the project --> Pull. (Eclipse or STS)
        1.1.2. Right click on the project Team --> Pull (Eclipse or STS).
        1.1.2. git pull origin <branchName> or git pull (command).
        
Step-2. Do your changes on your local workspace.

Step-3. git pull again before you commit your changes to local repo.

Step-4. Check if there is any confilict resolve it. Or commit & push your changes.

If you want to see the changes in remote repo (beofre the clone)

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
