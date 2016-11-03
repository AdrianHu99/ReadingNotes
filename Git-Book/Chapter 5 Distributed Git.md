###5.1 Distributed Workflows



###5.2 Contributing to a Project

* We can use **git diff --check** to see white space errors.    



* As a general rule, our commit messages should start with a single line that’s no more than 
  about 50 characters and that describes the changeset concisely, followed by a blank line, 
  followed by a more detailed explanation. 
  
  It's also a good idea to use the imperative present tense in these messages. Here is an example:    
  
      Short (50 chars or less) summary of changes

      More detailed explanatory text, if necessary.  Wrap it to
      about 72 characters or so.  In some contexts, the first
      line is treated as the subject of an email and the rest of
      the text as the body.  The blank line separating the
      summary from the body is critical (unless you omit the body
      entirely); tools like rebase can get confused if you run
      the two together.

      Further paragraphs come after blank lines.

        - Bullet points are okay, too

        - Typically a hyphen or asterisk is used for the bullet,
          preceded by a single space, with blank lines in
          between, but conventions vary here
          
 
 
* If you and another member pushes the work at the same time. When you want to share that work, you need to fetch and merge your master from origin/master if it has changed, and finally push to the master branch on the server. The general sequence is something like this:  
![](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Git-Book/5.2%20General%20sequence%20of%20events%20for%20a%20simple%20multiple-developer%20Git%20workflow.PNG)  



### 5.3 Maintaining a Project

* A cherry-pick in Git is like a rebase for a single commit. It takes the patch that was introduced in a commit and tries to reapply it on the branch you’re currently on. 
