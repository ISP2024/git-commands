## 7. Commands for Remotes

1. To list all your remote repositories, with their URL, use:


2. To view details about a rempote repo named `origin`, including all the remote banches and local tracking branches for `origin` is:

3. You commit some files to `dev-foo` and try to "push" them to Github, but it fails:

   ```
   cmd>  git checkout dev-foo
   cmd>  git push
   fatal:  The current branch dev-foo has no upstream branch. 
   ```
   Explain this error.


4. What is the command to push `dev-foo` to `origin` as a new remote branch on `origin`?



5. Suppose your remote repository (Github or `origin`) has a branch named `beverages` that you don't have in your local repository.  What is the command to create a new local branch as a copy of the remote `beverages` branch that **tracks** the remote branch?
   - There are many commands that do this.  You can show one or more than one.


6. Consider this situation:
   - you have a local repository including a README.md file.
   - Your local repo is up-to-date with a remote Github repo (has identical README.md)
   - You edit README.md on Github using Github's web interface and save the changes.
   - On your local machine, you edit README.md, commit the changes and push it to Github.    
   What happens when you push? Explain why.



7. Suppose you want to move "origin" to a different URL. This can happen when:
   - you change the name of the repo on Github
   - you transfer ownership to someone else
   - you want to move from Github to another site, like Bitbucket
   What is the command to change the URL of "origin" `to https://github.com/newuser/newreponame`



8. You want to have a *second* remote repository for your work on Bitbucket.  What is the command to add a remote named "bitbucket" with the URL "https://bitbucket.org/your-username/git-commands"


   - What is the command to push the master branch to "bitbucket"?





> This actually works.
> Since you already have code in your local repo, you should create an *empty* repo on Bitbucket and "push" to it to copy all your work.
