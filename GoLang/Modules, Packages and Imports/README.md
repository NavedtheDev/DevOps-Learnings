## Repository ##

* A place in the version control system, where the source code for a project is stored. 

## Module ##

* Root of a Go library or application stored in a repository. 

* They consist of one or more packages, which give the module orgnization and structure. 

* We can store more than one module in a repository, it is not encouraged. 

* Everything within a module is versioned together. 

* Maintaining two modules in one repository means tracking separate versions for two different projects in a single repository. 



## How to create a module ##

* Go to the directory where you will be storing your source code. 

* After that create a directory where we would be storing our project. Then, cd into that directory.

* <b>For this dircetory to become a Go module, we use the command 'go mod init <module_path>'.</b>

* This module path is a globally unique identifier. It could be something like github.com/username and then your repository name. Example, example.com/learn.
