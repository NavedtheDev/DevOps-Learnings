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

* cp -> allows you to create a copy of a file or directory and place it in a specified location. This command also expects two arguments. The first argument is the source file or directory. The second argument is the destination. Example,

```
cp Cricket/rules.txt Football
```

* rm -> used to remove or delete files and directories. 

```
rm Sports/Cricket/Extras.txt
```

* cat -> to see the contents of a file.

* We can also use cat command to add data to a file, by, 

```
cat > example.txt
Hey everyone
```
Use ctrl + d to save and exit.

* touch -> to create a file.

* more -> you can view text files in a scrollable manner. It loads the entire file at once. 

* less -> allows you to view the contents of a file and navigate through the file. 

* what is < > -> displays a one-line description of what a command does. 

* man -> provide information about the command in detail.

<b>NOTE :</b> --help flag provide users with the options and use cases available in a command. 

* apropos -> will search through the man page names and descriptions for instances of a keyword. This is useful if you want to look up all commands within the system that contains a specific keyword. Example,

```
[~]$ apropos modpr
modprobe (8)         - Add and remove modules from the Linux Kernel
modprobe.d (5)       - Configuration directory for modprobe
```



















