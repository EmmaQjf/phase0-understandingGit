git--create checkpoints and snapshots during my project.
Git remember every saved version of the project, so you can compare versions and go back to previous codes and undo mistakes. 
It allows branches which allow you to explore and test codes.
It allows many people to collabrate and work on the same project without overwriting each other.
it is a good way to back up online. 


git init --Creates a hidden .git/ folder;Turns the current folder into a Git repository
git add . -- copy files from working directory to staing area; selecting which one goes to the next commit. 
git commit -m "message" --taking everything in the staging area and save a snapshot into Git History.

git branch feature  -- create a new branch so you can work on someother feature without breaking the code in the main
git checkout feature--move to the feature branch from the main

git checkout main--switch to main
git merge feature --merge the code from the branch to the main. Make sure the work in branch is done and not broken before you merge. 
Also, always pull from the main, before you merge. --->
--> git pull.... 
git checkout main
git pull origin main



git remote add origin <url> --Links your local repo to GitHub
git push -u origin main   ----Uploads commits from local → GitHub
 


difference between git merge feature and git merge main 
while working on branch, do i always need to git add . before git commit -m everytime or i can only use git commit -m 


git add file.js
git commit -m "Update logic"
Those up two lines = git commit -am "Update logic" (-a only stages tracked files,Git does not auto-track new files.)
