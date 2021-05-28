# Here is the SPA (Single Page Application)

## INTRO
The Web application "Departmemts and Employees" consists of two parts: 
backend - folder "DjangoAPI" (which is implemented on Django) and 
frontend - folder "react-crud" (which is implemented on React). 

Thanks to the dependency settings, we will be able to raise the Django and React with command:

`npm start`

When setting up the application, we will need two terminals (I used "Visual Studio Code"). For work with backend, you will need to activate the virtual environment (below will be the cover instructions on how to create a "venv" and how to activate it). You do not need to create / activate a virtual environment to work with a frontend, just use a regular terminal.

Additionally. SPA was developed on Windows. During development I used "Visual Studio Code", "pip", "Node Package Manager", "Node.js", "SQLiteStudio", "Postman".
If this is your first SPA using React, then you needed to install "Node.js" and "Node Package Manager".

There are several options for structuring the DjangoReact project. I decided that in the root folder I would have folders with: 
a Django project ("DjangoAPI") - backend, 
a second folder - with a virtual environment ("djangoreact_venv"), 
and third folder - React project ("react-crud") - frontend.
A "DjangoAPI" will consist of one application - EmployeeApp.

# So, let's do it (Django + React = App "Departmemts and Employees")

In order to start the site, you need to enter the following commands step by step in the first or second terminal "cmd" according to the instructions.

## Setting environment DJANGO (first terminal)

### Create and activate a virtual environment in the "reactCRUD_djangoAPI" folder (ie the newly created "my_venv" folder will appear on the same level as the "reactCRUD_djangoAPI" folder). Type in cmd terminal following for create and activate venv:

`python -m venv my_venv`

`cd my_venv`

`cd Scripts`

`activate`

### Next step - switch to folder "DjangoAPI" and set up dependens. 
For it, enter the following step by step:

`cd..` ----- (the command will move to the directory by "Scripts" to "my_venv")

`cd..` ----- (the command will move to the directory by "my_venv" to "reactCRUD_djangoAPI")

`cd DjangoAPI`

`pip install -r requirements.txt`(for Windows)

`python manage.py runserver` (We raise the Django server for React to see the backend. So run this command and leave the cmd terminal active.)

## Setting REACT (open second cmd terminal)
Check availability Node.js and Node Package Manager (if they do not exist, then install them). 
Commands for check exist:

`node --version` (for ex. result >>> v14.16.0)

`npm --version` (for ex. result >>> 6.14.11)

For work with REACT you need open in parallel second terminal, where also need activate venv.
Afte instalation / checking the version  Node.js and Node Package Manager, enter following in cmd terminal for REACT (in folder "mainapp-ui"):

`npm install react-scripts --save`  >>> (create folder "node_modules" in folder "react-crud")

`npm start`

### Optional setting REACT 
If these settings are not enough for work SPA, then try to enter the next command in turn:

`npm install --save bootstrap`

`npm install --save react-router-dom`

`npm run build` >>> (create folder "build")

Enter the following again:

`npm start` >>> (After these commands server http://127.0.0.1:8000/ will rise.)

My congratulations! The program should start!


If again these settings are not enough for work SPA, then try to enter the next command in turn:
### Optional setting DJANGO 

Return to first terminal where activated venv (navigate to the "DjangoAPI" folder). 

Next step - create superuser (administrator) to access the link http://127.0.0.1:8000/admin/
Through the DjangoAdmin you can change categories and posts. Let's create:

`python manage.py createsuperuser`

`python manage.py makemigrations`

`python manage.py migrate`

`python manage.py collectstatic` (>>> Type 'yes')

`python manage.py runserver`

## Then run server (second terminal):

`npm start`

After these commands you activate the virtual environment and the site (Django + React) on the server http://localhost:3000/ will rise.
