* There is a common phrase associated with Linux that goes like this, “Everything is a file in Linux.” What this phrase tries to convey is every object in Linux can be considered to be a type of file. 

* There are three types of files, regular, directory and special files. 

## Regular Files ##

* Regular files, these are the most common type of files that contains some text, data or images. Examples are configuration files, shell scripts or code, JPG files, etc. 

## Directory ##

* Directory is a type of file as well that stores other files and directories within. The simplest example of this is your home directory. 

## Special Files ##

* Special files can be subcategorized into five other file types. 

   1. Character files: These files represent devices under the /dev file system that allows the OS to communicate to IO devices serially. Examples include devices such as the mouse and the keyboard. 
   
   2. Block files: These are files representing block devices also located under /dev. Examples of a block device are hard disks and RAM. 
   
   3. Links: Links in Linux is a way to associate two or more file names to the same set of file data. There are two types of links. The hard link associates two or more file names that share the same block of data on the physical disk. The symbolic link or symlink can be loosely compared to a shortcut in Windows. They act as pointers to another file. Deleting a symlink does not affect the data in the actual file. 
   
   4. Socket: A socket is a special file that enables the communication between two processes. 
   
   5. Named Pipes: This is a special type of file that allows connecting one process as an input to another. The data flow in a pipe is unidirectional from the first process to the second. 
 




* Let us now see how to identify the different file types in Linux. 

-> One way to do this is by making use of the file command like this,

```
 $ file /home/naved-ahmad
/home/naved-ahmad: directory
```

In this example, running the command file with the file or directory name displays the file type. 



-> Another way to do this is by running an ls or list storage command with the -l flag with the file or directory as the argument. 

```
ls -ld /home/naved-ahmad
drwxr-xr-x 1 naved-ahmad naved-ahmad 4096 May  1 11:26 /home/naved-ahmad
```

From the command output, look at the first character. The letter d denotes that this is a directory. Similarly, we can identify the rest of the file types by checking the first letter in the ls -l output. Regular files can be identified by a dash, character devices by the letter c, link, by the lowercase letter l, socket file by the letters, named pipes by the letter p, and finally, block device by the letter b.
