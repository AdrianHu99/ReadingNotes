### 7.1 Revision Selection

* **git log --abbrev-commit --pretty=oneline** gives you the output that will use shorter values but keep them unique.   
  when we use **git log** and see all the commit numbers, we can use **git show CommitNO.** to show the specific commit.  
  also, we can use **git branchName** to see the last commit in that branch.  
  **git reflog** can give a log of where your HEAD and branch references have been for the last few months.  
  **git log -g** can give you more information about that.  



* We can place a * at the end of a reference to see the previous commit.  
  **git show HEAD^** will give you the parent of HEAD. We can also put a number after that meaning the nth parent of HEAD, that only works   if HEAD has more than one parent.  
  **git show HEAD~** has the same meaning as **git show HEAD^**. The only difference is when you want to add a number after that.  
  **git show HEAD~2** means the first parent of the first parent, which should be equal to **git show HEAD^^**.  
  
  
  
* If you want to what in this branch has not merged into another branch, you can do that by **git log A..B** which means "all commits       reachable by B that aren't reachable by A."  
  **git log origin/master..HEAD** would tell you what you need to merge in if you want to keep your HEAD up to date.    
  
      **git log refA..refB**  
      **git log ^refA refB**  
      **git log refB --not refA**  
      The three commands above are same.  
      **git log refA refB ^refC**  
      **git log refA refB --not refC**  
      These two commands are to see all commits that are reachable from refA or refB but not from refC.  
  
  

* **git log --left-right refA...refB** uses three dots to show all the non-common commits and the side of the range each commit is in.  



### 7.2 Interactive Staging

* **git add -i** can give you much more information of the files that are staged or not staged. You will have much more choices for       those files, as below shows: 

        $ git add -i
           staged     unstaged path
        1:    unchanged        +0/-1 TODO
        2:    unchanged        +1/-1 index.html
        3:    unchanged        +5/-1 lib/simplegit.rb

        *** Commands ***
          1: status     2: update      3: revert     4: add untracked
          5: patch      6: diff        7: quit       8: help
        What now>  
        
        

### 7.3 Stashing and Cleaning

* **git stash** takes the dirty state of your working directory – that is, your modified tracked files and staged changes – and saves it on a stack of unfinished changes that you can reapply at any time.  
  **git stash apply** or more specifically, **git stash apply stash@{2}** help you reapply the changes you stashed. But it will reapply the changes not the files that are staged. If you want to reapply exactly to the original position, you need to use **git stash apply --index** instead.  
  **git stash drop** will remove the stash and **git stash pop** will apply the stash and drop it from your stack.  
  **git stash --keep-index** will not stash anything that is already staged.  
  **git stash --patch** will work similar to **git add -p**.  
  
  
  
* If you have already worked on the branch for a while, you may get a confilict when you want to reapply the stashed work. In that case, you can run **git stash branch** which will create a new branch for you.  
  Be careful about **git clean**, you can run it with **-n** to double check or with **-i** to run it in an interactive mode. **-f** is force, **-x** is to remove any file matching the pattern in **.gitignore**.  
  
  
  
### 7.4 Signing Your Work (Security)



### 7.5 Searching



* **git grep
