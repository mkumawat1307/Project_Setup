# This is my end to end Project
```
1. Connect with github account by using below commands
```
```
2. git config --global user.email "you@example.com"
```
```
3. git config --global user.name "Your Name"
```
```
4. Create a Folder for project in your system 
```
```
5. Now open this folder with vs coad
```
```
6. Creating a new repository in github account
```
```
7. git init
```
```
8. create 'README.md' file in current directory
```
```
9. git add abc.txt or git add .
	- . is add all files and folders from current directory
```
```
11. git status
```
```
12. git commit -m "this is my first commit"
```
```
13. Copy your remote repository's URL from GitHub
   - The HTTPS or URL is copied from the given GitHub account, which is the place of the remote repository.
```
```
14. git remote add origin 'your_url_name'
```
```
15. git push -u origin main
```
```
16. create .gitignore file in where you created new 
repository
```
```
17. create .LICENSE file in where you created new repository
```
```
18. git pull 
  - fetch and download content from a remote repository and immediately update the local repository to match that conten
```
```
19. create 'template.py' file in current directory and put all below commands in this file
    import os
    from pathlib import Path

    package_name="DimondPricePrediction"

    list_of_files=[
        "github/workflows/.gitkeep",
        f"src/{package_name}/__init__.py",
        f"src/{package_name}/components/__init__.py",
        f"src/{package_name}/components/data_ingestion.py",
        f"src/{package_name}/components/data_transformation.py",
        f"src/{package_name}/components/model_trainer.py",
        f"src/{package_name}/pipelines/__init__.py",
        f"src/{package_name}/pipelines/training_pipeline.py",
        f"src/{package_name}/pipelines/prediction_pipeline.py",
        f"src/{package_name}/logger.py",
        f"src/{package_name}/exception.py",
        f"src/{package_name}/utils/__init__.py",
        "notebooks/research.ipynb",
        "notebooks/data/.gitkeep",
        "requirements.txt",
        "setup.py",
        "init_setup.sh",
    ]


    # here will create a directory

    for filepath in list_of_files:
        filepath=Path(filepath)
        filedir,filename=os.path.split(filepath)
        
        """ how exist_ok works:if "directory" already exists, 
        os.makedirs() will not raise an error, and it will do nothing. 
        If "my_directory" doesn't exist, it will create the directory.
        """
        if filedir != "":
            os.makedirs(filedir,exist_ok=True)
            
        if (not os.path.exists(filepath)) or (os.path.getsize(filepath) == 0):
            with open(filepath,"w") as f:
                pass
        else:
            print("file already exists")

    # here will use the file handling
```
```
20. in 'init_setup.sh' file put below commands
	echo [$(date)]: "START"
	echo [$(date)]: "creating env with python 3.8 version"
	conda create --prefix ./env python=3.8 -y
	echo [$(date)]: "activating the environment"
	source activate ./env
	echo [$(date)]: "installing the dev requirements"
	pip install -r requirements.txt
	echo [$(date)]: "END"
```
```
21. init_setup.sh file only works in git bash command prompt for run init_setup.sh file command is "bash init_setup.sh"
```
```
22. git push -u origin main
```