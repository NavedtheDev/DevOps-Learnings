* pwd -> This should print the present directory you are on.

* ls -> to see the contents of a directory.

* mkdir -> to create a new directory. 

* cd -> It will automatically change the directory to the home directory from any location in the system. 

* mkdir dir1/dir2 -> to create a directory inside a directory without going inside dir1.

* An alternative to the CD or change directory is the PUSHD command. This command remembers the current working directory before changing to the directory specified in the command argument. 

* mv -> moves a directory or a file from one place to another. This command requires two arguments. The first argument is the source file or directory, and the second argument is the destination directory where we want to be moved. Example,

```
mv /home/naved/football/stumps /home/naved/cricket/
```
This will move the directory from football to Cricket. Notice that we have used absolute path. We can also use the relative path to achieve this, by, 

```
mv football/stumps cricket/
```
Here make sure that you are in the /home/naved directory.

* We can also use mv command to rename a file. We can do this by running the same mv command as before. Example,

```
mv Asia/India/Lucnow Asia/India/Lucknow
```
The first argument is the directory, which has to be renamed, and the second argument is the relative path to the correct directory name. 
