tutorial: https://www.youtube.com/watch?v=YJC6ldI3hWk  
Note: the comand below is for Mac only. Windows may use slightly different command.
## Basic

Step 1. Create a directory for a project   
``` conda create --name my_app flask sqlalchemy```
note: need to pass in at least one package in the above command. Could use pip as a default.

Step 2. Activate the python environment   
run ```source activate my_app```

Step 3. Deactivate the python environment  
run ```source deactivate```


Step 4. Create a different environment
``` conda create --name my_app27 python= 2.7 flask sqlalchemy```


Step 5. remove/delete environment and packages
``` conda remove --name my_app --all```
