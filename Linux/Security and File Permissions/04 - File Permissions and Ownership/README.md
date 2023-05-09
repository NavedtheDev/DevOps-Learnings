* Use th ebelow command we can determine the file type and the permissions it has,

```
ls -l <name_of_file>
```

![Screenshot (144)](https://user-images.githubusercontent.com/98219227/236995064-09dd47e5-d20b-4643-9478-0ebbb9c3e6a4.png)

![Screenshot (145)](https://user-images.githubusercontent.com/98219227/236995227-72bea148-1446-4abb-9f19-e7842b8cdf5d.png)


* Now that we know hoe file permission sarte represented in Linux, let us change permisssions of some files.

* Command used to modify the permissions of a file is called chmod. Syntax,

```
chmod <permission> <file_name>
```

* Permissions can be modified in two ways, symbolic mode and numeric mode. Both lead to the same result. 

   1. In symbolic mode, the first characters following the chmod command specify whose permissions you want to change. For user use u, g for group and o for others. After these characters, we need to specify if we want to grant access using plus symbol or revoke existing access with the minus symbol. Finally, we provide the file or directory for which the permissions have to be changed. Example,
   ```
   chmod ugo+r-x example.txt -> Provide read access to owners, groups, and others, Remove execute access.
   ```
   2. In numeric mode, we specify the permission to be updated in terms of the three digit octal values. The first among the three digit is for the owner, second one is for group and third one is for others. 
   ```
   chmod 555 example.txt -> Provide read and execute access to owners, groups and others.
   ```
