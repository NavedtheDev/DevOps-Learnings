* We can change the history of a git branch with an interactive rebase. We do so using the -i flag in the git rebase command. Also, we have to specify which commits we want to update. Suppose want to modify the first four commits. So we will use the command,

```
git rebase -i HEAD~4
```

* Through the above command we are telling git that we want to interactively rebase the last four commits. 
