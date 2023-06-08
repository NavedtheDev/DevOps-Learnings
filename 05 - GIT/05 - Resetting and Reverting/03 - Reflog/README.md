* Suppose you thought that the commit you just made is of no use, and you hard resetted it. But then you realized that the commit you just hard resetted was actually of importance. No need to panic.

* The git reflog command shows us all the actions that have been taken on our repo. 

```
git reflog
```

* You can easily undo your mistake by restting HEAD based on the information that reflog gives us. 

* To point HEAD back to where it was, 

```
git reset --hard HEAD_ID_obtained_from_the_reflog_command
```
Example,
```
git reflog --hard 8ad5
```
Now our repo has been reset to its previous state. 



### git log vs. gi reflog ##

* git log only shows information only about the commits and not about the state of the repository like git reflog does. 
