# gitsetup2

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
1. Now repeat by creating a new branch and committing some new change. However this time, before attempting to merge, switch back to the main branch and make a change that will “conflict” with the new changes.
2. Now try to merge. There should be a conflict.
3. Resolve the conflict, and complete the merge.


## ➡️ Pull Requests and Code Reviews

See your Pull Request on GitHub
Add a link to your webpage on the main index.html. Commit the change.
Push again, and see your PR update
Add your partner as a “reviewer” (and vice versa)
Review your partners code, trying making some comments, and eventually “accept” your partner’s changes (and vice versa)
Try to merge back into the main branch. Probably there will be a merge conflict on index.html. Resolve it in the web interface and complete the merge.

