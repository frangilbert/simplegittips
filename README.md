#Simple Git Tips

##Reset Remote revision
`git reset --hard HEAD^` (only reverts one revision)  
`git push --force`

##Amend last commit message
`git commit --amend -m "New commit message"`

##Check branches merged to master
`git branch --merged master`  
`git branch --no-merged` (branches not merged)

##Delete branches
`git branch -d the_local_branch` (Local)  
`git push origin :the_remote_branch` (Remote)

#Git Logs
`git log [-- filepath]`  
`shift` + Q

#Rollback a commit
`git reset --hard HEAD~3` # Go back 3 commits.

#Move the most recent commit(s) to a new branch
`git branch newbranch`  
`git reset --hard HEAD~3` # Go back 3 commits. You *will* lose uncommitted work.*1  
`git checkout newbranch`  

#Reset master branch to remote state
`git reset --hard origin/master`

#Switch to branch before pushing
`git symbolic-ref HEAD refs/heads/not-master`