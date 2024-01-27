# This is my end to end Project
```
1. Connect with github account by using below commands
2. git config --global user.email "you@example.com"
3. git config --global user.name "Your Name"
4. Create a Folder for project in your system 
5. Now open this folder with vs coad
6. Creating a new repository in github account
7. git init
8. in current folder creat 'README.md' file
9. git add abc.txt
10. git add .
	- for all file add
11. git status
12. git commit -m "this is my first commit"
13. Copy your remote repository's URL from GitHub
   - The HTTPS or URL is copied from the given GitHub account, which is the place of the remote repository.
14. git remote add origin 'your_url_name'
15. git push -u origin main
16. create .gitignore file in where you created new repository
17. git pull 
  - fetch and download content from a remote repository and immediately update the local repository to match that conten
18. creat file 'init_setup.sh' in current folder and put below commands init_setup.sh file
	echo [$(date)]: "START"
	echo [$(date)]: "creating env with python 3.8 version"
	conda create --prefix ./env python=3.8 -y
	echo [$(date)]: "activating the environment"
	source activate ./env
	echo [$(date)]: "installing the dev requirements"
	pip install -r requirements.txt
	echo [$(date)]: "END"
19. init_setup.sh file only works in git bash command prompt for run init_setup.sh file command is "bash init_setup.sh"
```