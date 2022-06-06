# Let's Git It Part 2: Merges and Pull Requests

## ➡️ Becoming Merge Maestros 
#### Merge without conflicts
1. Go to a personal repo on the command line. 
2. Create a new branch off of your existing main branch using 
```git checkout -b newbranch```

4. Change one (or more) lines of code on the new branch, and add, commit
```
git add . #stage those changes 
git commit -m “added some new feature!” #commit those changes 
git log #use this to look at the log and see your new commit at the top 
```
4. Go back to the main branch. 
```
git checkout main #this switches back to your original branch
git log #use this to look at the log and see that your new commit ISN'T THERE
```
5. MERGE. Use git merge to bring in the changes from the newbranch into the main branch. 

```
git merge newbranch # this is the merge! it will bring in the new commit
git log #use this to look at the log and see that your new commit is now here 
```
6. Delete your newbranch since all of its new code has now been merged into main. 
```
git branch -d newbranch 
```
7. You should see that the main branch is updated with the changes merged in from newbranch!



#### Merge with conflicts
We're basically going to repeat the above. However this time, before attempting to merge, switch back to the main branch and make a change that will “conflict” with the new changes.


1. Go to a personal repo on the command line. Head to the main branch first. 

```git checkout main```

2. Create a new branch off of your existing main branch using 
```git checkout -b newbranch```

3. Now make some changes to a file. Then add and commit. 

```
git add -A # stage those changes

git commit -m "Added new feature!" # commit those changes

git log # look at the log, see your new commit at the top
```

4. Now switch back to the original branch. 
```
git checkout main 
git log # look at the log, see that your new commit isn't there
```

5. NOW, make some changes to the **same line in the same file** as you did above in step 3. Then add and commit those changes to the original branch. 

```
git add -A # stage those changes

git commit -m "Fixed a bug!" # commit those changes

git log # look at the log, see your new commit at the top
```

6. Try to merge your changes from `newbranch` into `main` now. 

```
git merge newbranch # this is the merge! but there's about to be a problem...
```

7. Resolve the conflict, and complete the merge.

The conflict might look like this, for example:

```
# UH OH! Merge conflict
# open up the file in vscode, and somewhere you will see something like this
`
<<<<<<< HEAD
color: brown;
=======
color: black;
>>>>>>> YOUR_BRANCH_NAME_new_feature
`
# in order to "resolve" the conflict, you have to remove all the << >> == stuff
# and combine/choose the code you want.
# e.g. the above changes to just:
```

8. To complete the merge, you will need to add and commit your changes: 

```
# now, you have to add and commit this change as a merge conflict resolution

git add -A

git commit -m "Fixed merge conflict"

git log # look at the log, see the merge commit at the top

git branch -d YOUR_BRANCH_NAME_new_feature # delete the feature branch now that it is merged in
```


## ➡️ Pull Requests and Code Reviews

[Follow along in the slides here!](https://docs.google.com/presentation/d/1sizTXbGXHQ_p8JIxlswmzoA1qZYOVvADwcNhXsQIgzk/edit#slide=id.g13136ca5fd0_2_139)
