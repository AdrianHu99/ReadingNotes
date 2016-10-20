###3.1 Branches in a Nutshell  

* **git branch name** create a new branch.  
  **git log --decorate** can show you where the pointers are pointing.  
  **git checkout name** switch to another branch.  
  **git log --oneline --decorate --graph --all** will print the history of your commits, where the branch pointers are
  and how the history was diverged.
  
  
  
###3.2 Basic Branching and Merging

* **git checkout -b name** is equal to **git branch name** plus **git checkout name**.  
  Three way merge:  
  ![three way merge](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/3.2-Three-way-merge.png)  



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
  
 
 
* 
  
