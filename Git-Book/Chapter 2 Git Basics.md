###2.1 Get a Git repository



###2.2 Recoding changes to the repository

* **git status -s**  
 M README  
MM Rakefile  
A  lib/git.rb  
M  lib/simplegit.rb  
?? LICENSE.txt  

        The left-hand column indicates the status of the staging area.
        The right-hand column indicates the status of the working tree.  

        **FOR EXAMPLE**: The README file is modified in the working directory but not yet staged. 
        lib/simplegit.rb file is modified and staged.
        Rakefile was modified, staged and then modified again so there are changes both staged and unstaged.  



* Sometimes you’ll have a class of files that you don’t want Git to automatically add or even show you as being untracked. 
Then we can configure the .gitignore file to set some rules that Git will not add certain files.  

        Or, **git rm --cached README** will do that for you if you forgot to set the .gitignore 
        and want to remove it from staging area but still want to keep it int the hard drive.



* Glob patterns are like simplified regular expressions that shells use. 

        An asterisk (*) matches zero or more characters; 
        [abc] matches any character inside the brackets (in this case a, b, or c); 
        A question mark (?) matches a single character; 
        Brackets enclosing characters separated by a hyphen ([0-9]) matches any character between them (in this case 0 through 9). 
        You can also use two asterisks to match nested directories; a/**/z would match a/z, a/b/z, a/b/c/z, and so on.



* **git diff** show the exactly difference of the change.  
  **git diff --staged** or **git diff --cached**  show you the staged difference.  
  **git rm file** will stage the file's removal, while **rm file** will not stage it.  
  
      **FOR EXAMPLE**: **git rm log/\*.log** will remove all files that have the .log extension in the log/ directory.
  
  
  
* **git mv** TBD



###2.3 Viewing the commit history

* **git log**  
  **git log -p** will list all the detailed differences.  
  **git log -p -2** will limit the output to 2 entries.  
  **git log --stat* will briefly summarize the changes for all entries.  
  **git log --pretty=oneline/short/full/fuller** will show the log less or more depending on the value of pretty.  
  **git log --pretty=format** TBD
  **git log --author/committer=** limit the author/committer  
  **git log --since/after/before/until=** limit the time  
  
  
  
###2.4 Undoing things

* **git commit --amend** you end up with one commit, the second commit replaces the results of the first.  
  **git reset HEAD file** unstage a staged file.  
  **git checkout -- file** unmodifing a modified file.  
  
  
  
###2.5 Remotes TBD
  
  
  
###2.6 Tagging TBD  



###2.7 Alias 

* **git config --global alias.unstage 'reset HEAD --'** will make an alias for reset HEAD so that 
**git unstage file** is same as **git reset HEAD --file**  
        **FOR EXAMPLE**:   
        **git config --global alias.last 'log -1 HEAD'**  
        **git config --global alias.co checkout**  
        **git config --global alias.br branch**  
        **git config --global alias.ci commit**  
        **git config --global alias.st status**  
        
        
        
                          


