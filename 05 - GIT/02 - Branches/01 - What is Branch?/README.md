* A branch is a pointer to the last commit. 

## Some useful commands when working with branches ##

* To create a new branch,

```
git branch <branch_name>
```

* To switch to a branch,

```
git checkout <branch_name>
```

* To create a new branch and immidiately switch to this new branch,

```
git checkout -b <branch_name>
```

* To delete a branch,

```
git branch -d <branch_name>
```

* To list all the branches,

```
git branch
```



# HEAD #

* A HEAD is where we are right now in the git repository. The HEAD points to the last commit in the branch that you are currently on. 

* When you switch branches, the HEAD moves with you. 
