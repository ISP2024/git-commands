> **Instructions**
> 
> 1. Answer these questions using Markdown format.   
> 2. **Test that your answers are correct!** There is **no excuse** for submitting an incorrect answer, since you can verify them by experimentation.    
> 3. Create a Table of Contents, with a link to each section (Basics, Adding and Changing Things, Undoing Changes, etc.)    
>    - Optional: you can split this file into separate files. A file for `Basics.md`, `ChangingThings.md`, etc.
> 4. Delete these instructions.    
> 5. Check that your formatting is correct (points deducted if incorrect).  VS Code and IntelliJ have markdown previewers. See Sahanon's post on Discord for better VS Code previewer.

> To display your answers as lines of *unformatted text* there are 2 ways to do it:
> - (best) put the lines between triple backquotes, as in the source for this file:    
    ```
    unformatted text
    ```
> - leave 4 spaces at start of the line (and the text on the line must **not** "look like" a Markdown numbered or bulleted item)

## Using Git

TODO: Create a table of contents here.  There should be a clickable link to each
part of the document (or other files).  Note that a link looks the same whether 
it is a link to a section in this file or a link to a section in another file.

### Note on Paths

In this file, directory paths are written with a forward slash as on MacOS, Linux, and the Windows-Bash shell: `/dir1/dir2/somefile`.  For the MS Windows command prompt, substitute a backslash: `\dir1\dir2\somefile`.


## Part 1. Basics

1. When working with Git locally, what are these?  Describe each one in a sentence
   * Staging area -
   * Working copy -
   * master -
   * HEAD -

2. A git commit includes the author's name and email.  When you install git on a new machine (or in a new user account) you should perform these 2  git commands to tell git your name and email:
    ```
    # Git configuration commands for a new account


    ```
3. There are 2 ways to create a local Git repository.  What are they?
    - todo: describe first way
    - todo: describe second way

4. If you create a git repository in a directory named "/project1" by entering `git init`, Git will create a "hidden" directory for the local repository.  Where is the directory for the local repository (write the full path)?


### Part 2. Adding and Changing Things

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

1. What is the command to add README.md and *everything* in the `src` directory to the git staging area?


2. Write the command to add `test/test_a.py` to the staging area (but not other files).


3. Write a command to list files in the staging area.



4. You decide you **don't** want to commit `test/test_a.py` to git.  The command to remove `test/test_a.py` from the staging area is:


5. The command to commit everything in the staging area to the repository is:



6. You **never** want any files in the `out/` directory to be added to git. Describe 2 steps to configure the repo so git always ignores files in the `out/` directory:
   - step one
   - step two


7. What is the command to move `a.py`, `b.py`, and `c.py` from the `src` directory to the top-level directory of the project, so that they will also moved in the git repository?


8. Commit this change with the message "moved src directory":


9. To add **all changed files** (but not untracked files) using a single command, enter:

    After doing this you should use "git status" to verify you didn't add unintended files.


10. To delete the file `c.py` from your working copy **and** the repository, enter these two commands:



11. To see differences What is the command to show all differences between your working copy and the most recent commit? (Can be kind of hard to read.)



## Part 3. Undoing Changes

1. Use an editor to make some changes to file `a`.  What is the command to view the **differences** between your working copy `a` and the current version in repository?


2. You decide you don't like the changes to `a`. What is the command to **replace** your working copy of `a` with the current version in the repository?    
    (This also works if you accidentally *delete* a file from your working copy.)


3. How do you "undo" a commit?  What is the command to move the "head" of the current branch to the **previous** commit?



## Part 4. Branch and Merge

1. What is the command to create a new branch named `dev-food`?

 

2. What is the command to print what your current branch is?



3. What command to list **all** branches including remote ones?



4. What is command to switch your working copy to a branch named `dev-food`?



5. You commit some files to `dev-food` and try to "push" them to Github, but it fails:

    ```
    cmd>  git checkout dev-food
    cmd>  git push
    fatal:  The current branch dev-food has no upstream branch. 
    ```
    Explain this error.

6. What is the command to push `dev-food` to `origin` as a new remote branch on `origin`?



7. Suppose your remote repository (Github or `origin`) has a branch named `beverages` that you don't have in your local repository.  What is the command to create a new local branch as a copy of the remote `beverages` branch that **tracks** the remote branch?
    There are many commands that do this.  For your own reference you may want to write several.


8. Consider this situation:
   - you have a local repository including a README.md file.
   - Your local repo is up-to-date with a remote Github repo (has identical README.md)
   - You edit README.md on Github using Github's web interface and save the changes.
   - On your local machine, you edit README.md, commit the changes and push it to Github.    
   What happens when you push?    
   Explain why.



## Viewing Changes and Commits

* Command to show the history of a repository in the terminal (command) window.  This form shows one line per commit, with a graph, and all branches.
    ```
    git log --oneline --graph --all
    ```
    Some versions of git have an *alias* "log1" for this (`git log1`).

* The GUI tool `gitk` or `gitk --all` displays even more info about the commit history.


* The output of `git diff` can be hard to read. To view differences more visually:

    1. View differences on Github.
    2. Meld or Diffuse to compare and merge files. `git difftool` lists more tools.
    3. `gitk` shows diffs between commits
    4. Eclipse EGit shows side-by-side diffs and can merge interactively

---
## Resources

[Learn Git Interactive Tutorial][LearnGitInteractive] excellent visual tutorial.   
[Git Visualizer][VisualizeGit] execute Git commands and see the results as a graph.    
[Pro Git Online Book][ProGit]    
[Pro Git PDF][ProGitPdf] free download

[ProGit]: https://www.git-scm.com/book/en/v2 "Pro Git online book on Git-scm.com"
[ProGitPdf]: https://progit2.s3.amazonaws.com/en/2016-03-22-f3531/progit-en.1084.pdf "Pro Git v.2 PDF on AWS. Longer, book format."
[LearnGitInteractive]: https://learngitbranching.js.org "Interactive graphical git tutorial"
[VisualizeGit]: http://git-school.github.io/visualizing-git/ "Online tools draws a graph of commits in a repo as you type"
