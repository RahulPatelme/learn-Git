# Git and Github Notes

## Overview
Git is a version control system (VCS).
Version control is a software that tracks and manages changes to files over time.

Fork can be seen as an alternative route.

Git vs Github
1. Git is a VCS that runs locally on our computer. We can use git without never touching Github.
2. Github is a web service that hosts git repositories in the cloud.
3. Git is primarily a terminal tool.


## Basics of Git
A git repository is a workspace which tracks and manages files within a folder locally.

1. **git status** command gives information on the current status of a git repository and its contents.

2. **git init** command is used to create a new git repository. Before we do anything git related,
we must initialise a repository first.

Do not init a repo inside of a repo.
Before running git init, use git status to verify that you are not currently inside of a repository.

3. Use **git add** command to stage changes to be committed.

Working Directory -> git add -> Staging Area ->
git commit -> repository

4. Use the **git commit** command to commit changes from the staging area.
**git commit -m "message"**

5. **git log** command shows logs of commits.

6. **git add .** command to stage all changes at once.


## Commits in Detail
When possible, a commit should encompass a single feature, change, or fix. In other words,
try to keep each commit focused on a single thing.

This makes it much easier to undo or rollback changes later on. It also makes your code
or project easier to review.

Use present tense for writing commit messages.

*(CMD + Shift + >)* to see hidden files. Press again to hide.


## Working with Branches
In git, we are always working on a branch. The default branch name is master/main.

1. Use **git branch** to view your existing branches.

2. Use **git branch branch-name** to make a new branch.
This just creates the branch. It does not switch you to that branch (the HEAD stays the same). 

3. Once you have created a new branch, use **git switch branch-name** to switch to it.

4. Use **git switch -c branch-name** to create a new branch and switch to it all in one go.
-c is short for "create".

5. **git branch -d branch-name** to delete a branch.

6. **git branch -D branch-name** for force delete.

7. **git branch -m new-name** to rename a branch.


## Merging Branches 
We merge branches, not specific commits. 
We always merge to the current HEAD branch. 

1. Switch to the branch you want to merge the changes into (the receiving branch). 

2. Use **git merge branch-name** to merge changes from a specific branch into the current branch. 

Merge conflicts needs to be resolved manually. 
