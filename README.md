# Cheatsheets
## git

## git
Listing out only the basic commands needed for DS workflow on a daily basis.

**Sources**:

**https://www.freecodecamp.org/news/git-cheat-sheet/<br>https://phoenixnap.com/kb/git-commands-cheat-sheet**  


|Sno.|Purpose                      |git commmand                |Comments|
|----|---------                        |------------                |--------|
|    |Go to Repository folder          |``cd <repo name>``          |Git commands work only inside repo folder, not its root folder<br>``cd root``      root/<br>``git init``<br>``git clone <remote>``<br>``cd repo``      root/repo<br> ``(apply git commands here)``|
|1.  |Initialize git                   |``git init ``               |Not needed if cloned|
|2.  |Check status                     |``git status ``             ||
|3.  |Check configuration              |``git config -l``           ||
|4.  |Configure user name              |``git config --global user.name "Your Name"``||
|5.  |Configure user email             |``git config --global user.email "abc@email.com"``||
|6.  |Clone a repository               |``git clone <remote ssh key>``|To add an ssh key : <br>https://www.youtube.com/watch?v=WgZIv5HI44o|
|7.  |Clone a branch of the repository |``git clone -b <branch-name> <remote>``| This will now be the main branch|
|8.  |View all branches                |``git branch -aa``| Asterisk - current branch |
|9.  |Switch to another branch         |``git checkout <branch name>``||
|10. |Create a branch                  |``git branch <branch name>``||
|11. |Add file before commit           |``git add <filename>``|To add multiple files:<br>``git add <file1> <file2> <...>``<br>To add all files:<br>``git add .``|
|12. |Commit changes                   |``git commit -m "Title of commmit" -m "Description of commit"``|Description not mandatory|
|13. |See Commit history               |``git log``| For just oneline commit history:<br>``git log --oneline``|
|14. |Undo commmit (without deleting the existing commit)|``git revert <hashcode next to commit (after git log ---oneline)>``|This lets you pull that commit to local, and if pushed, it'll appear as a new commit<br>Use **Shift+Q** to exit the script page|
|15. |Push the changes                 |``git push``||
|16. |Pull updated repo                |``git pull``||




 
