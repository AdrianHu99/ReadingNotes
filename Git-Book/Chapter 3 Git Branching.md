###3.1 Branches in a Nutshell  

* **git branch name** create a new branch.  
  **git log --decorate** can show you where the pointers are pointing.  
  **git checkout name** switch to another branch.  
  **git log --oneline --decorate --graph --all** will print the history of your commits, where the branch pointers are
  and how the history was diverged.
  
  
  
###3.2 Basic Branching and Merging

* **git checkout -b name** is equal to **git branch name** plus **git checkout name**.  
  Three way merge:  
  ![three way merge](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Git-Book/3.2-Three-way-merge.png)



* There will be conflicts if you changed the same part of the code in the two branches you are merging. 
  Git won't do that merge.
  
  
  
###3.3 Branch Management

* **git branch** will give you the list of current branches.  
  **git branch -v** can see which branches are already merged into the branch you're on.  
  **git branch --merged/--no-merged** will filter the list to branches that you have or have not merged to 
  the branch you are currently on.   
  Notice: you can not delete the branch that is not merged in to the current pointed branch. The only way to delete 
  it is to use it with **git branch -D file**.
  
  
  
###3.4 Branching Workflows

* We can have different branches at various levels of stability; when they reach a more stable level, they're 
  merged to the branch above them.
  ![](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Git-Book/3.4%20progressive-stability%20branching.png)
  
  
###3.5 Remote Branches

* When you clone code from the remote repository, the master online will be named "origin/master" locally, and you will have 
  a master branch which is your local master.  
  Right now when you work on your master branch, someone might push some updates to the remote repository, as long as you do 
  not connect to the remote repository, your origin/master will not move.  
  To synchronize the work, you can use **git fetch origin**

 
 
* We can also have multiple remote servers, to add another remote server, we can use **git remote add name URL**.  
  Then you can run **git fetch name** to only fetch the code from that branch, and there will be another pointer pointing to   the commit the new branch has.  
  ![](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Git-Book/3.5%20remote%20tracking%20branch.png)  
  
  
  
* We can push our local branch to remote to work with others by run **git push remotename branchname**, also if we want to     change the branch name on the remote, we can run **git push origin name:newName**.  
  After the push, when someone fetches it from the server, he will not automatically have local copy of them. Instead, he       will only have a pointer that can't be modified.  
  If you want to merge that work into the current branch, you can run **git merge origin/newbranch**. Or, **git checkout -b     name origin/newbranch** could be used to give you a local branch that starts where origin/newbranch is.
  
  
  
* Tracking branch is the local branch that has a direct relationship to a remote branch; upstream branch is the branch it     tracks. Running **git checkout -b [branch] [remoteName]/[branch]** will switch to the new branch and track it from origin.   If you already have a local branch and you want to set it to a a remote branch or change the upstream branch, you can use   **git branch -u/--set-upstream-to origin/branchName** to set up the branch to track remote branch branchName from           origin.  



* **git branch -vv** could be used if you want to see what tracking branches you have set up, and if your local branch is       ahead, behind or both. Then if you want to update all the branches, you can run **git fetch --all**.   



* **git fetch** will fetch down all the changes but will not modify your work directory, which means you need to merge it       yourself. While **git ** will do **git fetch** and **git merge**.   




* **git push origin --delete branchName** will delete the branch from the server. Basically all it does is to remove the       pointer from the server. The git server will keep the data until a garbage collection runs.   



###3.6 Rebasing   



* **git rebase** is another way to integrate changes from one branch into another other than **git merge**.   
  **In the case below, if we run **git checkout experiment** and **git rebase master**:   
  ![](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Git-Book/3.6%20rebase.png)  
  After that, you can do **git checkout master** and **git merge experiment** to do a fast-forward merge.   
  Actually, the endpoint of rebase and merge is totally the same, the only difference is the history. Rebasing replays         changes from one line of work onto another in the order they were introduced, whereas merging takes the endpoints and         merges them together.   
  
  
  
* Another example, if you have three branches with a topic branch off another topic branch as the picture below shows:   
  ![](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Git-Book/3.6%20a%20topic%20branch%20off%20another%20topic%20branch.png)
  Then you decide to merge the client-side changes into the mainline. What you can do is by running **git rebase --onto         master server client**. This will merge the difference between **client** and the common ancestor of **client** and           **server** branch. As the picture below shows:   
  ![](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Git-Book/3.6%20rebase%20a%20topic%20branch%20off%20another%20topic%20branch.png)
  Basically the format is **git rebase [baseBranch] [topicBranch]**    
  The way to remove the branch is by running **git branch -d [branchName]**    
  
  
  
* To avoid something bad happens, we should always use **git pull --rebase**.   
  Remember: If you treat rebasing as a way to clean up and work with commits before you push them, and if you only rebase     commits that have never been available publicly, then you’ll be fine. If you rebase commits that have already been pushed   publicly, and people may have based work on those commits, then you may be in for some frustrating trouble.    
  
  
  
  
