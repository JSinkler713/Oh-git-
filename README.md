## Oh-Git!

### What to do when you forget to add a .gitignore

Say you have forgotten to add a .gitignore and you upload a ton of files...


### First step - add the .gitignore
Either manually enter what you need to ignore or use something like **gitignore.io** 


### Second step - we are going to remove them from the cache
```
git rm -r --cached .
git add .
git commit -m "Removing all files in .gitignore"
```

### Check out the git commits to see what happened :)


