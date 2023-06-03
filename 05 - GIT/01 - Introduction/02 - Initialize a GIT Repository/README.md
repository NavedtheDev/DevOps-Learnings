* Let's initialize a local GIT repository. We can do so with the following command,

```
git init
```

* To list all the contents of the folder including hidden ones, use

```
ls -a 
```
You will see that a .git folder has been created. 

* Suppose you created a file and added some content to it. Now you want to check the status of GIT, use

```
git status
```

* Storing changes in a local GIT repository is called committing. With every commit, we save the current state of the repository.

* Till now we haven't told GIT what do we want to do with our file. So they are still untracked. 

* We need to tell GIT that we want to add it to our local repository. Before we can commit a file, we first have to put it in the staging area. We can do so with the command,

```
git add <file_name>
```

* Now it's time to commit our change. But before that we must configure the git user who will be the owner of the commit. We do so using the following commands,

```
git config user.email <your_email>

git config user.name <your_name>
```

* Now, In order to commit the files that are currently in the staging area, use, 

```
git commit -m " "
```
Here, -m is a flag for a message. <br>
A commit records the change of a repository compared to its previous state.
