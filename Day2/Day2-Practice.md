# Day2: Practice

  1. Go to https://github.com/.
  
  2. Signup/Signin.
  
  ### Practice-1: Add a new project to GitHub repo under the ORGANIZATION. i.e., add your local project to github ORGANIZATION.
  ### Practice-2: Do some changes in server level, and update your local workspace (git pull).
  
      1. Create an ORGANIZATION.
      
      2. Create a new repository under the organization. (not under your github username).
      
        Note:
          1. Download the git scm from https://git-scm.com/ which is the client to communicate with the serevr GitHub.com.
          2. Download the tortoiseGit from https://tortoisegit.org/ (this is also a client, just try this. Restart your machine if you don't see the colors on the local repo folders/files.)       

      3. Clone the GitHub repo to your local machine. (using any client Git bash, TortoiseGit, etc)

        Syntax: git clone <gitURL> <destinationPath>

        Ex: git clone https://github.com/<ORGNAME>/FirstJavaProject.git <destinationPath>

      4. Configure username & emailid.
      
          git config --global user.email "you@example.com"
          git config --global user.name "Your Name"

      5. Add the new files/code to repo.

        Syantax: git add <fileName>  OR git add .

        Ex: git add MyFirstJava.java

      6. Commit to local repo.

        Syntax: git commit -m "commit message"

        Ex: git commit -m "adding my first project"

      7. Push the commits to server.

        Syntax: git push

        ex: git push
        
      8. Do some changes from Server level (Github.com), update your workspace with latest changes.
      
        Synatx: git pull Or git pull origin <branchName>
        
        Ex: git pull origin master
      
      9. Create a new branch in local and then push your new branch to server. 
      
        Syantax: git checkout -b <newBranchName>.
        
      10. Update two files. Commit each file individually, and see the log locally how the commits created (date & date, commit-id, HEAD, origin branch etc). "git log".
      
      11. From the above step-10, push only one commit.
      
        Syntax: git push origin <commit-id>:<branchName>
        
 # Bitbucket & GitLab
 
      Practice the same above steps with Bitbucket https://bitbucket.org/ and GitLab https://gitlab.com/ (This is the similar tool to GitHub).
      
      Parallelly you can learn both the tools since operations(git commands & worlflow, branching, merging, tagging etc) wise both are same.


# What you learned

      1. How to update your local workspace if someone pushed their code chnages into GitHub server.
      2. How to create a repo in GitHub under the ORGANIZATION & the purpose of the ORGANIZATION.
      3. Organization name is unique for entire github server.
      4. Difference between the code maintain under your username & organization.
      5. How to delete a repo.
      6. How to create a new branch from command line.
      7. Inviting users i.e., adding users to your organization.
      8. Pushing selective commit.
      
     
