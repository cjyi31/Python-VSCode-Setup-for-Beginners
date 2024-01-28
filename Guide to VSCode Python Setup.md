**This document contains information for installing and setup of Python and VS Code.**

**Table of Contents:**

1. Installing Python
2. Installing Setting up VS Code with Extensions
3. Setting up Workspaces in VS Code
4. Creating Virtual Environment using VS Code (using venv method)
5. Installing Python Packages
6. Additional Tips


# 1. Installing Python
Check if you already have a python already installed in your computer:

Press windows button > type cmd > press Enter to open the command prompt. In the command prompt, type "python --version" and hit "Enter".

If python is installed, it will return the python version that is in your computer. Else you may skip to step 2.

Else it will return an error message like/similar to:
![Alt text](<data/raw/00 Check if Python already installed.jpg>)

If you do not have Python installed, proceed below. Go to <https://www.python.org/downloads/> to download the latest version of python.
Enable the selections below and click on install now.

![Alt text](<data/raw/02 Python Install_AddtoPATH.jpg>)

For first time python users, you may stop here and go to Step 2.

However, if you are a little bit more advance python user, where you need to install different python versions in your computer. You might want to **unselect** "Add python.exe to PATH". Instead, create a folder where you keep different python versions separately like so:

1. Create folders and make sure to name the folders with the python version. In this example, I've created 1 folder named "pyver" in "C:\Users\cjyi3\" and 1 folder inside "pyver" named "py31011" since I am installing python version 3.10.11 (in addition to the 3.12.1 which I've installed initially.)

2. Download the python version you wanted and select Customize Installation. Then follow the selections below and customize the install location where you've created the new folders. 
![Alt text](<data/raw/03 Custom Install_Save in pyver.jpg>)

3. Click Install and you are done.


# 2. Installing VS Code
Go to https://code.visualstudio.com/download and download VS code and install in your computer. Remember to select add to PATH.

## 2.1 Setting up VS Code using Extensions.
Once installation is complete, you need to install the following extensions. In the extension search bar, type the following and click install:
1. Python Extension Pack
2. Pylance
3. Jupyter
4. Path Intellisense
5. Code Snap
6. Material Icon Theme
7. Code Spell Checker (optional)
8. Codeium (optional)
9. Markdown Preview Enhanced (optional)
10. Path Intellisense
11. Prettier


# 3. Setting up Workspaces in VS Code
Useful settings for VS Code:
This is very useful if you have a .py file and you only want to run selected codes without running the entire .py file.
Good for productivity, highly recommend.
Go to Settings and type "Jupyter Interactive" in the search bar like below. Then select the checkbox.
![Alt text](<data/raw/15a VS Code Setup_Settings_Jupyter_interactive.jpg>)
![Alt text](<data/raw/15 VS Code Setup_Settings_Jupyter_interactive.jpg>)

# 4. Creating Python Virtual Environments
Once you have a chance of start using python, it might be time to consider setting up virtual environments. Python virtual environments help manage software dependencies and ensure code is reproducible. Virtual environments are useful ways of ensuring that the correct package/library versions are consistently used every time the software runs.
In this example we will use the **venv method** to create Python Virtual Environment.

In VS Code Open a workspace, then press ctrl + shift + p.
Then in the search bar type in Python Create Environment like so and select Venv:
![Alt text](<data/raw/16 Create Python Virtual Environment venv method in VS Code.jpg>)
![Alt text](<data/raw/17 Create Python Virtual Environment venv method in VS Code2.jpg>)
If you have more than 1 python installed, select the one that you want to use for the project.
![Alt text](<data/raw/18 Create Python Virtual Environment venv method in VS Code3.jpg>)

If you have a list of requirements/packages to installed, you may select requirements.txt. If you do not have, you may just click OK.
![Alt text](<data/raw/19 Create Python Virtual Environment venv method in VS Code4.jpg>)

Wait for a while as the virtual environment is creating.
Once it is done, you will see that you have a .venv file created in your workspace like so:
![Alt text](<data/raw/20 venv folder created in workspace.jpg>)

## 4.1 Select the virtual environment when working with Jupyter Notebook.
Open a new jupyter notebook using ctrl + shift + p and select "Create New Jupyter Notebook".
Then in the top right hand corner click on select kernal and select the one which you've just created. If you do not see it you may click on "select another kernel".
![Alt text](<data/raw/21 Select Kernel Virtual Env.jpg>)
Once selected, you will see something as below:
![Alt text](<data/raw/22 Select Kernel Virtual Env - Selected.jpg>)

# 5. Installing Python Packages
Click on Terminal > New Terminal. Once Terminal tab is open then type "pip install numpy" and hit enter.
Once done it will say successfully installed the packages.


# 6. Additional Tips
1. To preview markdown file (.md file), you may press ctrl + shift + v. Once the preview window opened, you may drag the window to the side to view it side by side as you make your edits.
2. To generate and export a list of all python packages installed in your computer, you may type "pip freeze > requirements.txt" in the terminal and hit "Enter".
3. Best practice, when documenting your project, remember to have a section on Requirements in the README.md file and specify the python version you are using for the project. This is to ensure reproducibility.