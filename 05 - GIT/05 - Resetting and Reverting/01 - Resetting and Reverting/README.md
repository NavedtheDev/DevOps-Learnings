* It can happen that we have committed certain changes that we actually didin't want to commit. In that case, we have several options to undo that commit.  
* First option is to revert it. The git revert command creates a new commit, which literally reverse all the changes that were made on the commit that we specified. 

```
git revert <hash_ID>
```

* Reveret command is useful if you want to undo changes and keep those changes in your Git history. 

* Another way of undoing changes is with the git reset command. There are two ways to reset the commit in order to undo it, either with the --soft flag, in which case, we still want to keep all the changes that were made, or with the hard flag in order to lose all the changes that were made on that commit. 

* The reset command also recieves the amount of commits that we want to reset. 

```
git reset --soft HEAD~1
```

* Since we used the soft flag, we still have access to the changes that were made by that commit. We can see that using git status. 

* If we use the hard flag, the commit will be resetwithout saving all those changes. 

```
git reset --hard HEAD~1
```
