* Before starting to develop your script, it is important to have a clear idea on what you are developing it for. You should note down all the required tasks in a sequence.

* To create a shell script to perform all of these tasks, we create a file and we move all the commands to this file in the order that we want them to be executed. 

* Extension .sh indicates that it is a shell script. 

* That is the simplest form of creating a shell script. 

* We can now execute the shell script using the bash command. When it is executed, it runs each line in the script one after the otheruntil all lines are completed.

* There are other ways to execute a shell script. We can also configure a shell script to run like a command as an executable. Using this method, we need to configure it as a command.

* To add our script as a command, append the path to the directory containing the script to the end of the path variable. Example, 

```
echo PATH=$PATH:/home/naved
```

* For a shell script to work, we must set the correct permissions to the file, else it will show a permission denied error. The execute bit needs to be set for the file to be considered as an executable. 

* We can add that using the chmod command and make it executable. Example,

```
chmod +x /home/naved/run.sh
```



## Best Practices ##

* Give your script a name that makes sense.

* If you want to make your script executable, to be run like a command, then leave out the .sh extension. 
