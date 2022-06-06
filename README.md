# gitsetup2

## ➡️ Becoming Merge Maestros 
#### Merge without conflicts
1. Go to a personal repo on the command line. 
2. Create a new branch off of your existing main branch using “git checkout -b newbranch”
3. Change one (or more) lines of code on the new branch, and add, commit
```
git add .
git commit -m “new branch changes”
```
4. Go back to the main branch, and do git merge to bring in the changes
```
git checkout main
git merge newbranch
```
5. Delete the merged branch
```
git branch -d newbranch 
```
6. You should see that the main branch is updated with the changes merged in from newbranch!

#### Merge with conflicts
1. Now repeat by creating a new branch and committing some new change. However this time, before attempting to merge, switch back to the main branch and make a change that will “conflict” with the new changes.
2. Now try to merge. There should be a conflict.
3. Resolve the conflict, and complete the merge.


## ➡️ Pull Requests and Code Reviews
