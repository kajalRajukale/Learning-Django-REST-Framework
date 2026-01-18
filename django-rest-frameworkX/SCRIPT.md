\#In this session we are talking about virtual environment

## Findout what Python we are using

Find out which python we are using


> (Get-Command python).path
> C:\Users\Lenovo - 5\AppData\Local\Programs\Python\Python312\python.exe

This is not the Python of out virtual environment


Look in the project folder, there is no virtual environment

So lets create one

## Create virtual environment

We create it in the main folder of the django project. Its the folder where the file manage.py is located

C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework


python -m venv .venv

Is say: "run python program and start module **venv** with parameter **.venv**"

And it means

the Module venv will create a virtual environment in the folder .venv

## Activate the virtual environment

In the virtual environment folder .venv there is a file Activate.bat in the scripts folder

In fact there are three files for activatiog, depending on the shell you use

Linux (sh, bash) then use active

Windows Command then use activate.bat

Windows Poweshell then use Activate.ps1


You must use the correct file depending on yout shell.

Try the Poweshell script

PS C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework> .\.venv\Scripts\Activate.ps1
(.venv) PS C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework>


It worksand you see the the prompt has changes

| State  | Prompt                                                                              |  |
| ------ | ----------------------------------------------------------------------------------- | - |
| Before | PS C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework>              |  |
| After  | **(.venv)** PS C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework> |  |


Now lets check again the Python Program

(.venv) PS C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework> (Get-Command python).path
**C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework\.venv**\Scripts\python.exe


Now its correct, we use the Python from our virtual environment

## What happened if we start a new Terminal

(.venv) PS C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework> (Get-Command python).path
C:\Coding4Beginner\Workspace.Django\Learning-Django-REST-Framework\.venv\Scripts\python.exe


Also correct Path.

But when you reastart VSCode or your Computer this information is gone.

So befor starting  with Python always

- activate the virtual environment
- check the current python path
-
