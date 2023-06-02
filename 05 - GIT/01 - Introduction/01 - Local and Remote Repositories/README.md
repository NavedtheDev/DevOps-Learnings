* Git has two repository types, <b>local</b> and <b>remote</b>.

## Local Repository ##

* It is on your own machine, so you have direct access to it. 

* It consists of three stages. 

   1. Working area: are all ypur active changes. Git doesn't know what to do with them yet, it just know that these files contain some updates. 
   2. Staging area: contains new changes that will soon be committed.
   3. Committed files.

* The files that should be included in the commit are first added to the staging area. A commit gets created when a developer actually commits those files. 

## Remote Repository ##

* It is usually a centralized server and is entirely optional. 

* We can save the changes that we made locally on this remote server. 

* It is very useful when you want to have a backup of your data.

* Teammates can initialize their own local repository, on their own computers, and simply pull the data from the remote repository in order to start working on your project. 

* When a team member has made changes, they can push these changes to the remote repository. 

<b>NOTE: </b> In order to keep your local and remote repository in sync, you can then pull these changes from the remote repository into your local repository. 
