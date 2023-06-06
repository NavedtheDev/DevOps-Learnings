* We just updated the origin master branch by merging our branch into it. Our local repository(the cloned one) is not automatically aware of these changes. So we have to get these changes into our local repository. 

* We do so using,

```
git fetch origin master
```
in order to update the origin master branch in our local repo. 

* Now that we fetched the origin master, we can update our local master branch to point to the latest changes made on origin master. 

* To do that, we can merge origin master into the local master branch. 

```
git merge origin/master
```

* We now have all the latest changes avaialble locally. 

* Instead of individually fetching and then merging, we can also pull the origin master branch with this command,

```
git pull origin master
```

* git pull is actually two commands in one; git fetch and git merge. By typing the above command, we can fetch and merge the remote changes directly into our local master branch. 
