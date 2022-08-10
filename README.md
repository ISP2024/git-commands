> **Instructions**
> 
> 1. Answer these questions using [Markdown format][markdown-cheatsheet] ([Github Markdown][github-markdown]). 
> 2. Place your answers between lines beginning with 3 back-quotes, which tells Markdown they should be literal text.  Write only the command(s) someone would type, **no** command line prompt (like `$` or `cmd>`).  Example:
>    ```
>    git init
>    ```  
> 3. **Test that your answers are correct!** There is **no excuse** for submitting an incorrect answer, since you can verify your answers by experimentation.    
> 4. After the heading [Using Git](#using-git), create a hyperlink to each section (Basics, Adding and Changing Things, Undoing Changes, etc.). One line per link.     
> 5. **Delete these instructions and all "TODO" lines.**    
> 6. Verify that your Markdown formatting is correct (points deducted for bad formatting).  VS Code and IntelliJ have markdown previewers, and you can preview your files on Github.
>    - Better VS Code Markdown Preview is the "Markdown Preview Enhanced" extension.

## Using Git

> TODO: Create a table of contents here.  Create a clickable link to each part of this document or other file containing the questions and answers. Each link should display on a separate line.

[Basics](#basics)    
[Adding and Changing Things](#adding-and-changing-things)
[Next Section (Fix This)](#next-section)
[Next Section (Fix This)](#next-next-section)
[Commands for Remotes](remote-commands.md)   
[Resources](#resources)

#### Note on Paths

In this file, directory paths are written with a forward slash as on MacOS, Linux, and the Windows-Bash shell: `/dir1/dir2/somefile`.    
To use these commands in the MS Windows command prompt, substitute a backslash `\dir1\dir2\somefile`.


## Basics

1. When using Git locally, what are these?  Define each one in a sentence
   * Staging area -
   * Working copy -
   * master -
   * HEAD -

2. When you install git on a new machine (or in a new user account) you should perform these 2 git commands to tell git your name and email.  These values are used in commits that you make:
   ```
   # Git configuration commands for a new account


   ```

3. There are 2 ways to create a local Git repository.  What are they?
   - todo: briefly describe first way
   - todo: briefly describe second way

4. When you create a git repository by entering `git init`, Git will create a "hidden" directory for the local repository.  Where is the directory for this local repository (relative to the directory where you typed "git init")?



## Adding and Changing Things

Suppose your working copy of a repository contains these files and directories:
```
README.md
out/
    a.exe
src/a.py
    b.py
    c.py
test/
    test_a.py
    ...
```     
> TODO: Write the git command to perform each of these:

1. Add README.md and *everything* in the `src` directory to the git staging area.


2. Add `test/test_a.py` to the staging area (but not any other files).


3. List the files in the staging area.


4. Remove `test/test_a.py` from the staging area. (Useful if you accidentally add something you don't want to commit.)


5. Commit everything in the staging area to the repository.



6. Describe 2 steps to configure the repository so git ignores all files in the `out/` directory:
   - step one
   - step two

7. Command to move `a.py` and `b.py`, so that they are moved in your working copy and in the git repository.


8. Commit this change with the message "moved src directory":


9. Command to add **all changed files** (but not untracked files) to the staging area using a single command.

    (After doing this you should enter "git status" to verify you didn't add unintended files.)

10. **Delete** the file `c.py` from your working copy **and** the repository:



## Undo Changes and Recover Files

> TODO: enter the git command to do each of these

1.  Display the differences between your *working copy* of `a.py` and the `a.py` in the *local repository* (HEAD revision):

2. Display the differences between your *working copy* of `a.py` and the version in the *staging area*. (But, if a.py is not in the staging area this will compare working copy to HEAD revision):

3. Display the differences between `a.py` in the staging area and the repository.

4. If `main.py` has been added to the staging area (`git add main.py`), remove it from the staging area:

5. **Recover a file:** Command to replace your working copy of `a.py` with the most recent (HEAD) version in the repository.  This also works if you have deleted your working copy of this file.


6. **Undo a commit:** Suppose you want to discard some commit(s) and move both HEAD and "master" to an earlier revision (an earlier commit)  Suppose the git commit graph looks like this (aaaa, etc, are the commit ids)
   ```
   aaaa ---> bbbb ---> cccc ---> dddd [HEAD -> master]
   ``` 
   The command to reset HEAD and master to the commit id `bbbb`:


7. **Go back in time:** Using the above example, the command to replace your working copy with the files from commit with id `aaaa`:


    Notes:
    - Git won't let you do this if you have uncommitted changes to any "tracked" files.
    - Untracked files are ignored, so after doing this command they will still be in your working copy.
 

## Viewing Commits

1. Show the history of a repository, using one line per commit:
   ```
   git log --oneline
   ```
   Some versions of git have an *alias* "log1" for this (`git log1`).

2. Show the history (as above) including *all* branches in the repository and include a graph connecting the commits:


3. To list all the files in the current branch of the repository, enter:


## Branch and Merge

1. Create a new branch named `dev-foo`:
 
2. Display the name of your current branch:

3. List the names of **all** branches, including remote branches:

4. Switch your working copy to the branch named `dev-foo`:

5. **Merge:** To merge the work from `dev-foo` into the master branch, perform these steps:
   > TODO: write a description of the steps and the git commands
   1. step one
      ```
      git do something
      ```
   2. step two
      ```
      git do something else
      ```


6. Describe under what conditions a merge may fail.




## Favorites

> TODO: Add at least 1 git task or situation that you'd like to remember, and the git command(s) to do it.


---
## Resources

> TODO: Add your favorite Git resources (at least 1)

[Pro Git Online Book][ProGit] Chapters 2 & 3 contain the essentials. Free e-book available.     
[Visual Git Reference](https://marklodato.github.io/visual-git-guide) one page with illustrations of git commands.

Try Git:

[Learn Git Interactive Tutorial][LearnGitInteractive] excellent visual tutorial.   
[Git Visualizer][VisualizeGit] execute Git commands in a web browser and see the results as a graph.    

[ProGit]: https://www.git-scm.com/book/en/v2 "Pro Git online book on Git-scm.com"
[ProGitPdf]: https://progit2.s3.amazonaws.com/en/2016-03-22-f3531/progit-en.1084.pdf "Pro Git v.2 PDF on AWS. Longer, book format."
[LearnGitInteractive]: https://learngitbranching.js.org "Interactive graphical git tutorial"
[VisualizeGit]: http://git-school.github.io/visualizing-git/ "Online tools draws a graph of commits in a repo as you type"
[markdown-cheatsheet]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[github-markdown]: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax