# Day1: Practice

  1. Go to https://github.com/.
  
  2. Signup/Signin.
  
  I just want to add a new java project to GitHub repo.

      1. Crate a new repository in GitHub. 
      
      Note: Download the git scm https://git-scm.com/ which is the client to communicate with the serevr GitHub.com.

      2. Clone the GitHub repo to your local machine. (using any client Git bash, TortoiseGit, etc)

        Syntax: git clone <gitURL> <destinationPath>

        Ex: git clone https://github.com/venkatasykam/FirstJavaProject.git <destinationPath>

      3. Configure username & emailid.
      
          git config --global user.email "you@example.com"
          git config --global user.name "Your Name"

      4. Add the new files/code to repo.

        Syantax: git add <fileName>  OR git add .

        git add MyFirstJava.java

      5. Commit to local repo.

        Syntax: git commit -m "commit message"

        Ex: git commit -m "adding my first project"

      6. Push the commits to server.

        Syntax: git push

        ex: git push 
