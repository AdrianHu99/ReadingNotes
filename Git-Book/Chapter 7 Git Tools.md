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
