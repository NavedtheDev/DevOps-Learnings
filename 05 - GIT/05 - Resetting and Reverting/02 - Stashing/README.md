*  Stashing is a feature that allows you to save your local modifications in a temporary storage area, known as the "stash." It's useful when you're working on a specific branch but need to switch to a different branch or perform some other operation without committing your changes. 

* We can stash all changes in the working area with the command,

```
git stash
```

* To get the changes back to the working area,

```
git stash pop
```

* The stash can be seen as a pile of books. We can keep on pushing to the stash, and the changes will simply pile up. 

* To see all the stashes that are currently on the stash, 

```
git stash list
```

* To see the contents of a certain stash, 

```
git stash show stash@{1}
```

* To pop a specific stash,

```
git stash pop stash@{1}
```
