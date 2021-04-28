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
- git merge and merge conflicts
- best practice to resolve git merge conflicts
- best practices of git and github