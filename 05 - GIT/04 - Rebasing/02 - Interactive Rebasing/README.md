* We can change the history of a git branch with an interactive rebase. We do so using the -i flag in the git rebase command. Also, we have to specify which commits we want to update. Suppose want to modify the first four commits. So we will use the command,

```
git rebase -i HEAD~4
```

* Through the above command we are telling git that we want to interactively rebase the last four commits. 

* Use the squash command to meld the three commits into the first commit. Change their command from pick to squash. 

* We have successfully rebased the three extra commits and created a new commit that contains the changes of all four commits combined. 
