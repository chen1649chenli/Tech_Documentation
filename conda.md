tutorial: https://www.youtube.com/watch?v=YJC6ldI3hWk
https://medium.freecodecamp.org/why-you-need-python-environments-and-how-to-manage-them-with-conda-85f155f4353c (Medium article)  
Note: the comand below is for Mac only. Windows may use slightly different command.
## Basic

Step 1. Create a directory for a project   
``` conda create --name mynewenv flask sqlalchemy```

Step 2. Activate the python environment   
run ```source activate mynewenv```

Step 3. Deactivate the python environment  
run ```source deactivate```


Step 4. Create a different environment
``` conda create --name mynewenv27 python= 2.7```


Step 5. remove/delete environment and packages
``` conda remove --name mynewenv --all```
