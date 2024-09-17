See [INSTRUCTIONS](INSTRUCTIONS.md) for instructions on completing this file.

## Using Git

[Basics](#basics)    
[Adding and Changing Things](#adding-and-changing-things)    
[Undo Changes and Recover Files](#undo-changes-and-recover-files)    
[Branch and Merge](#branch-and-merge)        
[Commands for Remotes](remote-commands.md)    
[Favorites](#favorites)     
[Resources](#resources)

#### Note on Paths

In this file, directory paths are written with a forward slash as on MacOS, Linux, and the Windows-Bash shell: `/dir1/dir2/somefile`.    


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

3. There are 2 ways to create a local Git repository.  Briefly descibe each one:
   - todo: describe first way to create a local repo
   - todo: describe second way to create a local repo


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

1. Add README.md and *everything* in the `src` directory to the git staging area.
   ```
   todo  your answer
   ```

2. Add `test/test_a.py` to the staging area (but not any other files).
   ```
   todo  your answer
   ```

3. List the names of files in the staging area.
   ```
   todo  your answer
   ```

4. Remove `README.md` from the staging area. This is **very useful** if you accidentally add something you don't want to commit.
   ```
   todo  your answer
   ```

5. Commit everything in the staging area to the repository.
   ```
   todo  your answer
   ```

6. For a Python project, name *at least 3* files or directories that you should not commit to git:
   - 
   - 
   -


7. Command to move all the .py files from the `src` dir to the top-level directory of this repository. This command moves them in your working copy *and* in the git repo (when you commit the change):
   ```
   todo
   ```


## Undo Changes and Recover Files

**TODO** enter the git command to do each of these. Use triple-backquote marks around text for git commands.

1.  Display the differences between your *working copy* of `a.py` and the `a.py` in the *local repository* (HEAD revision):


2. Display the differences between your *working copy* of `a.py` and the version in the *staging area*. (But, if a.py is not in the staging area this will compare working copy to HEAD revision):


3. **View changes to be committed:** Display the differences between files in the staging area and the versions in the repository. (You can also specify a file name to compare just one file.) 


4. **Undo "git add":** If `main.py` has been added to the staging area (`git add main.py`), remove it from the staging area:


5. **Recover a file:** Command to replace your working copy of `a.py` with the most recent (HEAD) version in the repository.  This also works if you have deleted your working copy of this file.


6. **Undo a commit:** Suppose you want to discard some commit(s) and move both HEAD and "master" to an earlier revision (an earlier commit)  Suppose the git commit graph looks like this (`aaaa`, etc, are the commit ids)
   ```
   aaaa ---> bbbb ---> cccc ---> dddd [HEAD -> master]
   ``` 
   The command to reset HEAD and master to the commit id `bbbb`:


7. **Checkout old code:** Using the above example, the command to replace your working copy with the files from commit with id `aaaa`:
   ```
   todo your answer
   ```
    Note:
    - Git won't let you do this if you have uncommitted changes to any "tracked" files.
 


## Branch and Merge

**TODO** Write 4 numbered items for common branch-and-merge tasks you would like to remember and show the git command to do each one. (You are write *more* than 4 if you want.)



## Favorites

**TODO** Describe *at least* 1 git task that (a) that you'd like to remember, or (b) you think is really useful, and the git command(s) to do it.



---
## Resources

[Pro Git Online Book][ProGit] Chapters 2 & 3 contain the essentials. Downloadable PDF is also available.     
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
[vscode-markdown-preview-enhanced]: https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced
