* We can merge a command to the main branch with the command,

```
git merge <branch_name>
```

* This command recieves the name of the branch that we want to merge into our current branch. 

* There are two types of merges that GIT can perform, a fast-forward merge and a no-fats-forward merge. 

* A fast-forward merge can happen when the current branch has no extra commits compared to the branch that we're merging. 

* We will first try to perform the easiest option, the fast-forward. This type of merge doesn't create a new commit, but rather merges the commits on the branch that we are merging right into the current branch. But its a very rare case. 

* With a no-fast-forward merge, Git creates a new merging commit on the active branch.
