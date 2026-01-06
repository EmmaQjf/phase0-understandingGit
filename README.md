git--create checkpoints and snapshots during my project.
Git remember every saved version of the project, so you can compare versions and go back to previous codes and undo mistakes. 
It allows branches which allow you to explore and test codes.
It allows many people to collabrate and work on the same project without overwriting each other.
it is a good way to back up online. 


git init -- Creates a hidden .git/ folder;Turns the current folder into a Git repository
git add . -- copy files from working directory to staing area; selecting which one goes to the next commit. 
git commit -m "message" --taking everything in the staging area and save a snapshot into Git History.

git branch feature  -- create a new branch so you can work on someother feature without breaking the code in the main
git checkout feature -- move to the feature branch from the main 

git push -u origin feature ----u links your local feature to remote feature,After this, GitHub now has a copy of your branch.Later, just git push will update it

git checkout main--switch to main
git merge feature -- (while you are on the main, not on the branch)merge the code from the branch to the main. Make sure the work in branch is done and not broken before you merge. 
Also, always pull from the main, before you merge. --->
--> git pull.... (This is how you do it, check the next two lines)
git checkout main
git pull origin main  -- keep the main updated to the current condition.



git init
git remote add origin <url> --Links your local repo to GitHub
git push -u origin main   ----Uploads commits from local → GitHub
 


difference between git merge feature and git merge main 
while working on branch, do i always need to git add . before git commit -m everytime or i can only use git commit -m 


git add file.js
git commit -m "Update logic"
Those up two lines = git commit -am "Update logic" (-a only stages tracked files,Git does not auto-track new files.)


Differece betwen git merge feature & git merge main
1. git checkout feature
git merge main
Meaning
“Bring main’s latest changes into feature.”

2. git checkout main
git merge feature
Meaning
“Bring the feature work into main.”


🔑 Key takeaways
Command	               ----Location of branch/commit
git branch feature                 Local only
git checkout -b feature	           Local only, also switches to it
git commit -m "..."             	On current branch, local only
git push origin feature	           Copies your branch & commits to remote (GitHub)



🔑 Key takeaways
Case A:If nobody else has pushed new commits to main on GitHub, you can merge directly locally:

git checkout main
git merge explainConcepts  __>This merges your feature branch into local main
git push origin main

✅ No pull needed because your local main already matches remote main


Case B: Your main is behind remote (someone else pushed changes)
If someone else made commits on GitHub’s main, you must pull first to avoid overwriting their changes:
git checkout main
git pull origin main   # fetch + merge remote changes
git merge explainConcepts
git push origin main
----Pull ensures your local main is up to date with GitHub.
Then merge your branch safely