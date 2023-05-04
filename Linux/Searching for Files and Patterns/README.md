* Run the locate command with the file name you are searching as the argument.

```
locate example.txt
```

-> This should return all paths matching the pattern. This command is useful to find files quickly in the Linux file system. It will print out all paths with the keyword in it. 

-> The downside to this command is that it depends on a database called "mlocate.db" for querying the file name. If you have just installed Linux or if the file you are trying to locate was created recently, this command may not yield useful results. This is because it is possible that the DB has not been updated yet. To manually update the DB, run the command updatedb, and then run the locate command again. 

<b>NOTE</b>: Please note that the updatedb command needs to be run as a root user to work. 

* Another way to do this is to make use of the find command. Use the find command followed by the directory under which you want to search. To search for a file by name, use the -name option, followed by the name of the file. 

## GREP ##

* To search within files, the most popular command in Linux is grep. Grep is commonly used to print lines of a file matching a pattern, but it offers a variety of other options as well. 

* Use the grep command followed by the word you want to search for, and finally, the file name. This should print out only the line matching the search pattern. 

* The grep command is case sensitive and will only print the lines matching the case of the pattern. To search case insensitive use the -i flag. 

* grep -r can be used to search for a pattern recursively within a directory. This is especially useful when you don't know which file contains the specific pattern that you are looking for. Example,

```
grep -r "Cricket" /home/naved
```
