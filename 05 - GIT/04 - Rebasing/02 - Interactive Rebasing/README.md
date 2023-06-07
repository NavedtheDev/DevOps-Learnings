* Interactive rebasing is a feature in Git that allows you to modify, reorder, squash, or edit commits during the rebase process. It gives you more control over the commit history by providing an interactive interface where you can selectively apply changes to individual commits.

* Interactive rebasing allows you to refine the commit history, combine related changes, and ensure a clean and organized history before merging into the main codebase.

* We can change the history of a git branch with an interactive rebase. We do so using the -i flag in the git rebase command. Also, we have to specify which commits we want to update. Suppose want to modify the first four commits. So we will use the command,

```
git rebase -i HEAD~4
```

* Through the above command we are telling git that we want to interactively rebase the last four commits. 

* Use the squash command to meld the three commits into the first commit. Change their command from pick to squash. 

* We have successfully rebased the three extra commits and created a new commit that contains the changes of all four commits combined. 
