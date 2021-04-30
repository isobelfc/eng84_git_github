# Git and Github

- stages of git on local host
  - working directory
    - the project directory on the local system
    - hidden `.git` folder created after `git init` means that git is aware of the files, but is not tracking them yet
  - staging area
    - we need to select the files to be tracked by git
    - `git add` adds files to the staging area
    - the process of adding the files to the staging area is `indexing` and the `index` is made up of the added files
  - git directory and local repository
    - we commit the files with a commit message
    - information related to the commit, such as author, filenames, date and time, and commit message, is stored in the git directory
    - the files themselves are stored in the local repository
    
![local git stages diagram](https://cdn-anlbg.nitrocdn.com/dKKErbUyoNysjatCgltCzbTJJilTMwLi/assets/static/optimized/rev-4b21c3b/wp-content/gallery/git/Git-Commit.png)

- how to reset/cancel if you have already run `git add .`
  - `git reset` to remove all files from list
  - `git reset filename` to remove one particular file
- what is a git staging area
  - where files are added, grouped, and organised ready to be committed to git
- workflow and the stages
  - files are worked on on the local machine
  - when these are ready to be commit, they are added to the staging area with `git add`
  - the files from the staging area are committed to the local repository, with a message explaining the commit
  - the local repository can then be pushed to a remote repository such as github, by adding the address of the remote repository with `git remote add origin` and then using `git push`
  - if multiple users are working on a project, or you want to leave the main branch unchanged until a feature is complete, branches can be made
  - commits to a branch do not alter the contents of any other branch
  - one branch can be merged into another to combine the data in each
- git merge and merge conflicts
  - a merge integrates separate branches back together into a single branch
  - a fast-forward merge is when the current branch has not been edited since the target branch was created, and therefore only needs to move the current branch tip up to the target branch tip
  - a three-way merge occurs when both branches have been edited, and compares the top branch tips and their common ancestor
  - most of the time, it automatically integrates the latest changes, by comparing the two branch tips and their common ancestor
  - however, when the same lines of code have been edited in both branches, it cannot tell which version should be kept
  - this is a merge conflict
- best practice to resolve git merge conflicts
  - git will output a message stating there is a conflict
  - we can see where the conflicts are
  - the most direct way to resolve is to edit one of the files
- best practices of git and github
  - commit often (but only once the code works)
  - don't commit dependencies, only what the dependencies are
  - don't commit local config files, or any other files that potentially contain private information
  - test changes before committing
  - write useful commit messages
  - make use of branches
  - don't allow pushes directly to the main branch
  - make sure `.gitignore` file is set up