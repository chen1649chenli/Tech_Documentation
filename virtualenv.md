tutorial: https://www.youtube.com/watch?v=N5vscPTWKOk

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
