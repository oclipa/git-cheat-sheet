# A Git Cheat-Sheet

## The Daily Routine

| Command ____________________________________________________ | Action _________________________________________________________________________________ |
| :------- | :------- |
| `git pull`| Pull all changes from the remote repository |
| `git checkout -b [branch-name-here]`| Create a new branch for your bug/feature/issue |
| `git add .`| Add any changed files to the staging index |
| `git status`| See the current status of the workspace |
| `git diff [source branch] [target branch]`| Show changes |
| `git commit -m "Detailed message here"`| Make the commit have a nice, detailed message |
| `git checkout master`| Switch back to the master branch when the feature is done and tested |
| `git merge [branch-name-here]`| Merge all changes into the master branch |
| `git push`| Send your changes up to the remote repository |
| <img width="300"/> | <img width="300"/> |

## Additional Actions

| Command ____________________________________________________ | Action _________________________________________________________________________________ |
| :------- | :------- |
| `git init`| Initialize the current folder as a repository |
| `git clone [/path/to/repo]` | Clone local repository |
| `git clone [url]`| Clone a remote repository |
| `git rm [file]`| Remove/delete a file |
| `git push origin [branch]` | Push changes to a specific branch |
| `git branch -d [branch-name-here]` | Delete a branch |
| `git tag [tag] [commit ID]` | Create a tag |
| `git log`| Display the git log |
| `git checkout -- [filename]`| Restore working copy with latest from HEAD |
| `git revert [commit ID]`| Rollback to the specified commit (preferred method for reverting a change) |
| `git reset --soft [HEAD or commit ID]`| Discarding intervening commits.<br/>Reset the HEAD to another commit but do not alter the index or working directory.<br/>All changes between original HEAD and commit will be staged. |
| `git reset --mixed [HEAD or commit ID]`| Discarding intervening commits and adds.<br/>Reset the HEAD and index to another commit but do not alter the working directory.<br/>All staged changes are removed from the index. |
| `git reset --hard [HEAD or commit ID]`| Discarding intervening commits, adds and changes to files in local worksapce.<br/>Reset the HEAD, index and workspace to another commit.<br/>All changes between original HEAD and commit will be staged<br/>Avoid using with shared repos. |
| `git commit --amend`| Allow the message for the most recent commit to be edited |
| `git clean -n`| Perform a dry run of clean |
| `git clean --force`| Clean all untracked files in the workspace |
| `git clean --force -d`| Clean all untracked files and directories in the workspace |
| `git clean --force -dx`| Clean all untracked **and ignored** files and directories in the workspace |
| <img width="300"/> | <img width="300"/> |

## Git Architecture &amp; Terminology

   * **Staging Index:** Add file to repo index in preparation for commit
   * **Commit:** Copy all staged files to the local repo database
   * **Push:** Copy all commited changes to the remote repo database
   * **Pull:** Copy latest changes from remote repo into local repo
   * **HEAD:** The current branch or commit referenced by the local repo
   * **Checkout:** Redirect the HEAD to point to a specific commit or branch (or fetch a specific file, which doesn't change the HEAD).
   * **Detached HEAD:** When the HEAD is pointing at a specific commit.  Changes cannot be submitted in this case. 

   


![Git Architecture](/assets/images/git-architecture.png)

## Git Workflow Diagrams

![Git Simple Workflow](/assets/images/git-simple-workflow.jpg)

![Git Check Sheet Workflow](/assets/images/git-check-sheet.jpg)

## Further Details

[Git Further Details (pdf)](/assets/pdfs/git-more-details.pdf)