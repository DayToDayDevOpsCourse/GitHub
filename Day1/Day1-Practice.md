# Day1: Practice

  1. Go to https://github.com/.
  
  2. Signup/Signin.
  
  ### Practice: Add a new project to GitHub repo. i.e., add you local project to github server.

      1. Crate a new repository in GitHub. 
      
        Note:
          1. Download the git scm from https://git-scm.com/ which is the client to communicate with the serevr GitHub.com.
          2. Download the tortoiseGit from https://tortoisegit.org/ (this is also a client, just try this. Restart your machine if you don't see the colors on the local repo folders/files.)       

      2. Clone the GitHub repo to your local machine. (using any client Git bash, TortoiseGit, etc)

        Syntax: git clone <gitURL> <destinationPath>

        Ex: git clone https://github.com/venkatasykam/FirstJavaProject.git <destinationPath>

      3. Configure username & emailid.
      
          git config --global user.email "you@example.com"
          git config --global user.name "Your Name"

      4. Add the new files/code to repo.

        Syantax: git add <fileName>  OR git add .

        Ex: git add MyFirstJava.java

      5. Commit to local repo.

        Syntax: git commit -m "commit message"

        Ex: git commit -m "adding my first project"

      6. Push the commits to server.

        Syntax: git push

        ex: git push
        
        
 # Bitbucket
 
      Practice the same above steps with Bitbucket https://bitbucket.org/ (This is the similar tool to GitHub).
      
      Parallelly you can learn both the tools since operations(git commands & worlflow, branching, merging, tagging etc) wise both are same.


# Covered topics

      1. What are the unstaged & staged areas.
      2. How to create a repo in GitHub.
      3. Added a local project(code/files) to GitHub repo.
      4. We have Modified the files and committed and then pushed to repo.
      5. Modified two files & added only one file to stated area and then committed to local repo, finbally pushed to remote repository.

      
     
