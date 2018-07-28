tutorial: https://www.youtube.com/watch?v=N5vscPTWKOk
## Basic
Install virtualenv  
```pip install virtualenv```

Step 1. Create a directory for a project   
``` virtualenv project_1```

Step 2. Activate the python environment   
```source project_1/bin/activate```

Step 3. run ```pip list``` to see the installed packages in the new environment

Step 4. run ```pip install``` to install the required packages


Step 5. run ```pip freeze --local > requirements.txt``` to export the needed packages

Step 6. get out of the virtual environment, run ```deactivate```

Step 7. remove/delete a virtual environment  
```rm -rm project_1```

## Advanced
Step 1. Specify the python version to use when creating a project
``` virtualenv -p /usr/bin/python2.6 project_2```

Step 2. Install packages from a requirement.txt file  
```pip install -r requirements.txt```

Note: please separate the project files from the environment folders.
