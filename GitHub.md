Day1: Concepts
-----
1. How to access the code. Restictions on the code : Read, Write, Admin, Owner. : Just theoritical explanation.

2. Operations on code (check-out, check-in) : clone, add, commit, pull, push, fetch, revert, reset, rebase etc : Just theoritical explanation.

Practical Explanation:

	From Github End:
		2.1. Creating a repo under username.
		2.2. By default repo created with a branch called "master".
		2.3. auto genarted files .gitignore & README.md.
	From User end:
		2.4. Install GitScm & TortoiseGit. : https://git-scm.com/downloads , TortoiseGit: https://tortoisegit.org/download/
		2.5. Use github commands to upload the code. (Git) : Git 
			5.1. Clone the repo. Command: git clone <GitHubRepoURL> <destinationPath>.
			5.2. git add .
			5.3. git commit -m "Uploading a maven project for SampleJar".
			5.4. git push.
			5.5. Commit histroy.
			5.6. git pull
		2.6. Upload the code with the help of ToirtoiseGit.
		2.7. STS/Eclipse/Rad Setup.

3. Manage the code (branching, merging, taging): Organization, Repository : Just theoritical explanation.

-------------------------------------------------------------------------------------------------------------------------------------------------------
Day2: Concepts
-----

Day1: Pending concepts: 2.6, 2.7.

1. Multiple Branches.

	GitHub Repo/Project name : InternetBanking

	Branching Strategy-1:
		master: latest production code

		Sprint-1: AUG-R2-MAJOR-2018
			B1 : current dev branch

		Sprint-2: 
			B1 : 21-01-2018 : Prod code: lock the branch just before 5 to 10 days of implementation date : Merge B1 code to master branch after implementation day(22-01-2018). : And then create a new branch B2 from B1 (or) master branch (or) a particular tag/release since both have samme code.
			B2 : current dev branch.

		Sprint-3:
			B1 : Remove.
			B2 : Prod code: lock the branch just before 5 to 10 days of implementation date : Merge B2 code to master branch after implementation. : And then create a new branch B3 from B2 (or) master branch (or) a particular tag since both have samme code.
			B3 : current dev branch

	Branching Strategy-2:
		UK_Master : latest production code
		HK_Master : latest production code
		IN_Master : latest production code
		Sprint-1:
			Branch-1: Branch-name: UK_R1
			Branch-2: Branch-name: HK_R1
			Branch-3: Branch-name: IN_R1
		Sprint-2:
			Branch-1: Branch-name: UK_R2
			Branch-2: Branch-name: HK_R2
			Branch-3: Branch-name: IN_R2

2. Pull & push for each branch. : git pull Vs git pull origin <branchName> AND git push Vs git push origin <branchName>

3. Switch from one branch to other branch. : git checkout  <branchName>

5. Organization & Repos under Organization.

	ORG1: Prodcution : DIGITALAPPLICATION
	ORG2: TESTING proj. : DIGITALAPPLICATION-SELENIUM
	ORG2: SANDBOX : only Build
	ORG4: TOOLS

6. Teams.

7. Protect Branch, i.e., branch wise restiction.

-------------------------------------------------------------------------------------------------------------------------------------------------------
Day3: Concepts
-----

Day2: Pending concepts: 6, 7.

1. Create teams.

2. Protect branches. i.e., branch wise protection.

3. Create branch from command line. git checkout -b <newbranchName>, git push origin newbranchName.

4. Transfer a git repo from one organisation to another username or Organization.

5. Rename the existing github branch.

6. Create an orphan branch. (Before that show what is forked branch).

7. Other github basic commands:

	7.1. differences between two commit-ids: git diff <commitId1> <commitId2>

	7.2. git diff <commitId1> <commitId2>  > diff.patch : creating path file with the changes between two commits.

	7.3. list of branches: git branch, git branch -a, git branch -r.

	7.4. git log

Try to practice the same on https://bitbucket.org/ AND https://gitlab.com/ (since all are similar but minor differences are there). So that at  time, you will get some idea on all 3 tools GitHub, BitBucket, GitLab. Google to know the differences between the tools.




