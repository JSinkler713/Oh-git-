## Oh-Git!

### What to do when you forget to add a .gitignore

Say you have forgotten to add a .gitignore and you upload a ton of files...
This might be node_modules if in an express app, or .env if you are in a djano app like this example is.

### First step - add the .gitignore
At the top level of our repo ```touch .gitignore```
Either manually enter what you need to ignore or use something like **gitignore.io** 

If in express you will want to at least add the following
```
node_modules/
DS_STORE
```

In a django app I would at least add 


### Second step - we are going to remove them from the cache
At the top level of our directory we run
```
git rm -r --cached .
```
This will remove all our files, which is ok, since we can add them back in in a moment.
```
git add .
```
We now add the files we want back in, but since our .gitignore is in place, git will now ignore the ones we don't want.
```
git commit -m "Removing all files in .gitignore"
```


### Check out the git commits to see what happened :)


