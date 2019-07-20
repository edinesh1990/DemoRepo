This is a text file
------------------------------------------------
Git/GitHub Integration with Jenkins
------------------------------------------------

Requirement: Whenever there is new commit in Github--Jenkins should pull that commit and run a build


On Node Machine(where jenkin runs):
1. Install python : sudo apt-get update && sudo apt install python
2. Install git : sudo apt install git
3. Create a folder: 	mkdir PythonProject && cd PythonProject 
4. Create some randome python file:	demo.py
5. Initialize a git repo: 		git init
6. Add remote origin (Github): 		git remote add origin <url_of_remote_repo>
7. Stage and Commit:			git add . && git commit -m "First Commit"
8. Push to Remote:			git pull origin master && git push origin master (You need to generate ssh key and add to github)

9. Create a freestyle job in jenkins
10. Under Build--> Excute shell to check if the job creates build:
	cd <PythonProject folder>
	python demo.py #to run the program
11. Run build now to test if the job success
12. Now configure Job:	
		Add git : <github_url>
		Build trigger: poll scm : * * * * * (every minute- scans for every min and triggers build if any commit)
13. Add chnages to git local (add random readme.txt file)
14. Push to Github and check if the build is started

