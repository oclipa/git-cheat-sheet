<div style="display: inline-block;">
<a class="link" href="http://oclipa.github.io/">&lt; home</a>
<a class="link" href="http://oclipa.github.io/toolbox.html">&lt; toolbox</a>
</div> 

## Summary

My attempt to summarize the main features of Git:

<a href="assets/images/git.png" target="_blank"><img src="assets/images/git.png" /></a>

## Links


## A Daily Routine

| Command | Action |
| :------- | :------- |
| `git fetch origin [upstream-branch]`| Fetch all changes from the specified branch into the current branch |
| `git merge origin/[upstream-branch]`| Merge all changes from the specified branch into the current branch |
| `git branch [branch]` | Create a new branch, from the current branch, for your bug/feature/issue |
| `git switch [branch]` | Switch to the new branch |
| - | Make changes |
| `git add .`| Add any changed files to the staging index |
| `git status`| See the current status of the workspace |
| `git diff [source branch] [target branch]`| Show changes |
| `git commit -m "message"`| Make the commit have a nice, detailed message |
| `git branch -vv` | Display local branches and the remote branches to which they are mapped |
| `git push [-u] origin/[upstream-branch]`| Push your changes to an upstream branch (`-u` = create the upstream branch into which changes will be pushed) |
| `git request-pull origin/[master branch] origin/[branch]`| Request review of latest changes in current branch compared to master (typically, it is simpler to do this from a GUI tool) |
| <img width="300"/> | <img width="400"/> |

<p style="page-break-before: always"/> 

## Additional Actions

| Command | Action |
| :------- | :------- |
| `git init`| Initialize the current folder as a repository |
| `git clone [/path/to/repo]` | Clone local repository |
| `git clone [url]`| Clone a remote repository |
| `git mv [file]`| Move a file |
| `git rm [file]`| Remove/delete a file |
| `git branch -d [branch-name-here]` | Delete a branch |
| `git tag [tag] [commit ID]` | Create a tag |
| `git log`| Display the git log |
| `git restore [filename]`| Restore working copy with latest from HEAD |
| `git revert [commit ID]`| Rollback to the specified commit (preferred method for reverting a change) |
| `git reset --soft [HEAD or commit ID]`| Discarding intervening commits.<br/>Reset the HEAD to another commit but do not alter the index or working directory.<br/>All changes between original HEAD and commit will be staged. |
| `git reset --mixed [HEAD or commit ID]`| Discarding intervening commits and adds.<br/>Reset the HEAD and index to another commit but do not alter the working directory.<br/>All staged changes are removed from the index. |
| `git reset --hard [HEAD or commit ID]`| Discarding intervening commits, adds and changes to files in local worksapce.<br/>Reset the HEAD, index and workspace to another commit.<br/>All changes between original HEAD and commit will be staged<br/>Avoid using with shared repos. |
| `git commit --amend`| Allow the message for the most recent commit to be edited |
| `git rebase [branch-name]`| Similar to merge but more dangerous in shared repos.  Appends the current branch to the specified branch.  Main advantage is cleaner history. |
| `git clean -n`| Perform a dry run of clean |
| `git clean --force`| Clean all untracked files in the workspace |
| `git clean --force -d`| Clean all untracked files and directories in the workspace |
| `git clean --force -dx`| Clean all untracked **and ignored** files and directories in the workspace |
| <img width="300"/> | <img width="400"/> |

<p style="page-break-before: always"/> 
<div>   
<button type="button" class="collapsible">+ Enable SSH for GitHub</button>
<div class="content" style="display: none;" markdown="1">
The main advantage of enabling SSH, rather than just using HTTPS, is that a username and password does not need to be entered for every action.
  
1. Generate a new SSH key: 
   * `ssh-keygen -t rsa -b 4096 -C "your_github_email@example.com"`
1. Start the SSH agent: 
   * `eval $(ssh-agent -s)`
1. Add the private key to the SSH agent: 
   * `ssh-add ~/.ssh/id_rsa`
1. Copy the contents of ~/.ssh/id_rsa.pub (the public key) to the clipboard
1. On github.com, Profile Picture -> Settings -> SSH and GPG keys -> New SSH Key -> Paste the key into the Key field and give it an identifying name -> Add SSH Key
1. Test the connection: `ssh -T git@github.com`
   * If this fails, try: `ssh -T -p 443 git@ssh.github.com`
   * Further info: https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh
1. Once access is working, restart all terminals and applications that may wish to use Git via SSH (such as Visual Studio Code).
  
**Note:** The SSH agent must be running whenever you want to use SSH (so you may want to add the start-up command to your OS's start-up routines).
</div>
</div>

<div>   
<button type="button" class="collapsible">+ Further Details</button>
<div class="content" style="display: none;" markdown="1">

* [https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet](Atlassian Git Cheatsheet)
* [https://blog.thoughtram.io/git/rebase-book/2015/02/10/understanding-branches-in-git.html](Understanding Branches in Git)

</div>
</div>

&nbsp;

&nbsp;

&nbsp;

------
**Move along; nothing to see here...**

<script type="text/javascript">

    const loadCSS = (filename) => { 

       const file = document.createElement("link");
       file.setAttribute("rel", "stylesheet");
       file.setAttribute("type", "text/css");
       file.setAttribute("href", filename);
       document.head.appendChild(file);
    };

    const loadJS = (filename) => { 

       const file = document.createElement("script");
       file.setAttribute("type", "text/javascript");
       file.setAttribute("src", filename);
       document.head.appendChild(file);
    };
   
    //just call a function to load your CSS
    //this path should be relative your HTML location
    loadCSS("../collapse.css");
    loadJS("../collapse.js");

</script>


