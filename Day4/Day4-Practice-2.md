# Practice-2

## 1. By default your repository has one branch named "master" which is considered to be the definitive/conclusive/final/ultimate branch. But dont assume like 'master' branch is special. Its like other branches. We can remove/rename this branch.

### Practice-1.1:-
        -->Checkout the code to your machine:
          1.1.1. Clone the specific branch you want.
            Command: git clone -b <brach_name> --single-branch <git_repo> <destination>
            Ex: git clone -b Mx_Dev --single-branch https://github.com/venkatasykam/JarProjects.git /d/hari/git/dummy/JarProjects_mx

        -->Update code & check-in to git "local" repo:-
          1.1.2 Update the code on local, commit to local repo and then push to your git repo.
          1.1.3. Modify a file and ADD a new file and run the comamnd "git status -s".
            -->Added a new line in the file.
            -->Updated the exisitng line.
            -->Removed few number of lines.
          1.1.4. See the diff b/w remote repo and local repo "git diff".
          1.1.5. Command: git commit -m "updated few files".-->committed to local repo.

        -->Push the local repo to GIT repo.
          1.1.6. Command: git push.


### Practice-1.2:- Switch to other branch: git checkout <branchName>

          Clone the branch(Dev_Branch) other than 'master' (i.e., default branch) and modify the files and then commit to the repository branch 'Dev_Branch'.

          1.2.1. Clone: http://stackoverflow.com/questions/17383217/clone-from-a-branch-other-than-master

            git clone --help

            Option-1:- Cloning "master" (default branch) and then switch to other branch.
            ----------
              Command: git clone <url> <destination>

              Ex: git clone https://github.com/venkatasykam/hello-world.git Dev_Branch

              Command: git branch -l
              Command: git checkout <branchname> or git checkout -b <branchname> 
              [
              This is shorthand for: 
              git branch <branchname>
              git checkout <branchname>
              ]

              Ex: git checkout -b Dev_Branch

              Command: git branch -l

            Option-2:- Clone the particular branch
            ----------
              Command: git clone -b <branch> <remote_repo>

                Ex: git clone -b Us_Dev https://github.com/venkatasykam/hello-world.git hello_world_us

          1.2.2. Updated something and commit to the branch.

              Command: git commit -m "updated AddNumbers.java file with subtraction method"

          1.2.3. Command: git push

        Practice-1.3:- Delete a branh:

            Command: git branch -d <branchname> or git branch -D <branchname> (force delete to unmerged branch).

## 2. DIFF: (Create patch file and apply patch file):

          git log --oneline --all
          2.1. Diff b/w two revision numbers: git diff from-commit to-commit > output-file
              from-commit – the point at which we want the patch to start. 
              to-commit – the patch will span the changes up to and including this point.
              output-file – the patch will be written here

          2.2. Assume I had checkout the code and now my repo origin is 'Dev_Branch'. Then, modified few files. Checking the diff b/w local and remote repo.
              git diff>patch.diff

              git apply patch.diff

          git diff $(git merge-base <public branch> <experimental branch>) > <output file>

            Example: git diff $(git merge-base master Dev_Branch) > anotherPatch.diff

          git am 0001-updated-readme-file.patch --ignore-whitespace --no-scissors --ignore-space-change [not working]

## 3. GIT merging two branches: https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging

## 4. Rename the existing branch:
          4.1. switch to branch which needs to be renamed: git checkout -b <old_name>
          4.2. git branch -m <new_name>
          4.3. git push origin :<old_name>
          4.4. git push origin <new_name>:refs/heads/<new_name>

          OR

          4.1. git branch -m Dev_Branch Mx_Dev
          4.2. git push origin :Dev_Branch
          4.3. git push origin Mx_Dev

          -->git branch -a -->Display all the branches which are there under the repo.

          -->We can change the default branch from "master" to anyother. Click on the project(repo)-->settings-->branches-->here we can project the branches, and update default branch.

          -->Rename/delete/transferOwnership/chnage the mode public or prtivate
              repo: repo-->settings-->options

          -->Adding user: repo-->settings-->collaborators

          -->Check WebHooks on repo-->settings-->WebHooks in office

          http://githooks.com/

## 5. Transfer the repo to another organization or owner: https://help.github.com/articles/transferring-a-repository-owned-by-your-organization/

          5.1. Go to project repo "JarProjects" under the organization "MainLinee-FP9".  https://github.com/MainLine-FP9/JarProjects
          5.2. Settings-->Danzer Zone-->Click on "Transfer" button at "Transfer ownership".
          5.3. In the window-->enter the repo name "JarProjects" and target "organization" name "Maintenance-FP9".

## 6. Creating a new repo(in same organization or other organization) from exisitng repo with particular branch.
         http://stackoverflow.com/questions/9527999/how-do-i-create-a-new-github-repo-from-a-branch-in-an-existing-repo

          6.1. Create a new_repo. 
              Ex: https://github.com/MainLine-FP9/new_repo.git [in anotehr org]
              Ex: git push https://github.com/venkatasykam/new_repo.git +Us_Dev:master [under the same user]
          6.2. Clone the existing repo to new folder or update("git pull") the cloned existing repo.
              Ex: Existing repo https://github.com/venkatasykam/hello-world.git 
              This repo has 3 branches Us_Dev, Mx_Dev, master, Now I want a new repo with the code base "Us_Dev".
          6.3. git push https://github.com/MainLine-FP9/new_repo.git +Us_Dev:master
             git push tps://github.com/venkatasykam/new_repo.git +Us_Dev:master

## 7. Branch to branch merge: https://help.github.com/articles/merging-a-pull-request/

          7.1. https://github.com/venkatasykam/JarProjects has 3 branches. Us_Branch and Mx_Branch and master.
          7.2. Updated a java file on "Us_Branch" and commited the changes. 
          7.3. Master needs to be updated with "Us_Branch". Now, create Pull Request.
          7.4. Here, "master" should be "base" and "compare" should be "Us_Branch". Otehrwise, GITHUB will not allow merge.
          7.5. Now, "Us_Branch" & "Mx_Branch" have changes individually. Added a comment in the same line and both have different content.
            7.5.1. If Auto-merge is NOT possible in this case, we have to update the file(s) Manually and resolve the conflicts.
            Ex: base:Mx-branch , compare:Us_Branch
            The manually resolved conflicts(i.e., the changes) will be saved to both the branches to not to repeat this same conflict again in future.

            7.5.2. If Auto-merge is possible, only the "base" branch will be merged with the changes from "compare". The changes in "compare:Us_Branch" will be remain same.

## 8. Merge from one organization/repo to anotherOrganization/repo.

          8.1. There should be a fork betweeen the two organizations. Ex: Created a fork b/w https://github.com/venkatasykam/JarProjects, and https://github.com/MainLine-FP9/, then the "JarProjects" has been created newly on https://github.com/MainLine-FP9/JarProjects. If the repo "JarProjects" is lareayd there in "MainLine-FP9", then GIT will create a new repo as "JarProjects-1". [Once if you create a "fork" b/w organization, we cant un-fork even if you re-name the repo.]
          8.2. Made some changes in one java file "AddNumbers.java" from "venkatasykam/JarProjects". Now, Open a pull request.
          8.3. Pull the changes from "venkatasykam/JarProjects" into "MainLine-FP9/JarProjects".
          8.4. Now, making some chnages in one java file "AddNumbers.java" from "MainLine-FP9/JarProjects". Now, Open a pull request.
          8.5. Pull the changes from "MainLine-FP9/JarProjects" into "venkatasykam/JarProjects".
          8.6. Making changes in both the repos. Added a comment in the same line and both have different content.
          8.7. Auto-merge is not possible in this case. Manually we have to update the file(s) and resolve the conflict(s).

## 9. Merge from one git repo to another repo.

          Basic example: merge repo B into repo A
          git clone A
          git clone B
          cd A
          git remote add B ../B
          git fetch B
          git branch B-master B/master [whichever branch you want to merge]
          git merge B-master
        ----------------------OR
          cd path/to/project-b
          git remote add project-a path/to/project-a
          git fetch project-a
          git merge --allow-unrelated-histories project-a/master # or whichever branch you want to merge
          git remote remove project-a

## 10. Git: ignore some files during a merge [not working]

          Let's say you want to exclude the file config.php


          -->On branch A:

            1. Create a file named '.gitattributes' in the same dir, with this line: config.php merge=ours. This tells git what strategy to use when mergin the file. In this case it always keep your version, ie. the version on the branch you are merging into.
            2. Add the .gitattributes file and commit.

          -->On branch B: repeat steps 1-2

          Try merging now. Your file should be left untouched.

          git merge --no-commit <merge-branch>
          git reset HEAD myfile.txt
          git checkout -- myfile.txt
          git commit -m "merged <merge-branch>"

        http://stackoverflow.com/questions/8781240/a-way-to-restrict-git-branch-access
        https://help.github.com/articles/defining-the-mergeability-of-pull-requests/


## 11. git log --diff-filter=D --summary | grep delete
        http://stackoverflow.com/questions/31250359/git-repository-how-to-recover-deleted-files

## 12. Create new repository from particular branch of another repository. 
        http://stackoverflow.com/questions/9527999/how-do-i-create-a-new-github-repo-from-a-branch-in-an-existing-repo

## 13. Merge from one branch to another branch: https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
        https://git-scm.com/book/en/v2/Git-Tools-Rerere
        After you resolved the conflict manually run the command "git add <fine_name>". Or use the TortoiseGit to resolve the conflicts.

        git branch -->list all the branches
        git branch -v -->To see the last commit on each branch
        git branch --merged and --no-merged -->options can filter this list to branches that you have or have not yet merged into the branch you’re currently on.
        git branch -d <branch_name> -->Delete the branch. Delete will be failed, If the branch <branch_name> is not yet merged to another branch.
        git branch -D testing -->Delete the branch by force.

## 14. Restore deleted branch. http://stackoverflow.com/questions/4674226/does-github-keep-deleted-remote-branches-in-history-if-so-can-those-be-restore

        -->git reflog show --all
        -->Choose the commit ID from the result.

## 15. How to create an empty branch http://www.bitflop.dk/tutorials/how-to-create-a-new-and-empty-branch-in-git.html

        git checkout --orphan NEWBRANCH
        git rm -rf .

        20 jars projects are there in 'master' branch. [as per my requirement, 15 jars should be in Us_Dev, and 16 in Hk_Dev branch].

        -->cloned the 'master' to local machine.
        -->git checkout --orphan Us_Dev.
        -->git rm -rf .
        -->git add . -->Copied and added 15 jas to Us_Dev branch.
        -->git commit -m "adding local projects to github Us_Dev branch repo".
        -->git push --set-upstream origin Us_Dev.

        done some chanegs in jar16 project, now I wanted to merge the changes to master.

        -->git checkout master
        -->git merge --no-commit Us_Dev or git merge --no-commit --allow-unrelated-histories Us_Dev.
        -->git reset HEAD pom.xml [root pom]
        -->git reset HEAD */pom.xml [all other poms]
        -->git reset HEAD artifacts.txt [other files if any]
        -->git checkout -- artifacts.txt
        -->git checkout -- */pom.xml
        -->git checkout -- pom.xml
        -->git commit -m "merged the chnages from jar16 project from us_dev to master".

        If you are sure that you want to overwrite selected folder/file, then you do as below.
        //pull the latest changes on Us_Dev from remore repo
        -->git checkout Us_Dev
        -->git pull
        //pull the latest changes on master from remore repo
        -->git checkout master
        -->git pull
        //merge the changes from Us_Dev to master only on  JarProject16
        -->git checkout Us_Dev -- JarProject16
        -->git reset HEAD JarProject16/pom.xml
        -->git checkout -- JarProject16/pom.xml
        -->git commit -m "'Merge' these changes from us_dev to master on jar proejct16"
        -->git push

        If you are sure that you want to merge selected folder/file, then merge do as below.
        //pull the latest changes on Us_Dev from remore repo
        -->git checkout Us_Dev
        -->git pull
        //pull the latest changes on master from remore repo
        -->git checkout master
        -->git pull
        //merge the changes from Us_Dev to master only on  JarProject16
        -->navogate to specific project JarProject16.. cd JarProject16
        -->git merge --no-commit --allow-unrelated-histories Us_Dev
        -->git reset HEAD JarProject16/pom.xml
        -->git checkout -- JarProject16/pom.xml
        -->git commit -m "'Merge' these changes from us_dev to master on jar proejct16"
        -->git push
