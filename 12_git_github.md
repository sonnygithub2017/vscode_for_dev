* initialize or remove git repository
  - initialize git repository with git init (another way is use `git clone`)
    - open folder in vscode
    - right click > open in integrated terminal
    - initialize it if repo not exists
        ```bash
        git status
        # if not, initialize
        git init
        ```
  - remove git repository: in the integrated terminal: `rm -rf .git`
* check file status before commit
  - terminal: `git status`
  - vscode: source control:
    - U: untracked files, new files not added to git
    - A: added files, files that have been added to staging area
    - M: modified files, files that have been changed
    - D: deleted files, files that have been deleted
* staging and commit
  - staging: add files to staging area, ready to be committed
    - terminal: `git add <file>` or `git add .` (add all files)
    - vscode: source control > `+` icon (stage changes)
  - unstage: remove files from staging area
    - terminal: `git restore --staged <file>` or `git reset <file>`
    - vscode: source control > `-` icon (unstage changes)
  - commit: save changes to git repository
    - terminal: `git commit -m "<message>"`
    - vscode: source control > type "commit message" > commit button
* discard changes in working directory
  - terminal: `git restore <file>` or `git checkout -- <file>`
  - vscode: source control > select the file > `discard changes` icon
* uncommit files view: list or folder
  - vscode: source control > CHANGES > view button (toggle between list and folder view)
* commit history and file history
  - commit history
    - terminal: `git log --oneline --graph` (view commit history)
    - vscode: source control > GRAPH > view commit history
  - file history
    - terminal: `git log --oneline --graph <file>` (view commit history for a specific file)
    - vscode: Explorer > open file in editor > TIMELINE > filter for `git history` > view file commit history
* connect to remote repository (github)
  - github:
    - create an account with username and email
    - authentication (https or ssh) setup: see https://github.com/sonnygithub2017/git-github/blob/main/git_github_by_colt/09_connect_github.md
    - create a new repository, like `vscode_for_dev`, copy remote repo URL: like `https://github.com/sonnygithub2017/vscode_for_dev.git`
  - `git remote add` way
    - terminal:
      - add remote: `git remote add origin <remote repository url>`
      - check: `git remote -v` (verify the remote repository)
    - vscode:
      - add: source control > REPOSITORIES > select your repo > three dots > remote > add remote > enter `<remote repository URL>` and then type `origin` > enter
  - `git clone` way
    - terminal: vscode open folder in vscode > right click > open in integrated terminal > `git clone <remote repository url>`
    - UI: vscode > view > command palette > git clone > enter `<remote repository URL>` > select folder to clone the repo
* push and pull
  - push: upload local changes to remote repository
    - terminal: `git push origin <branch>` (default branch is `main`)
    - vscode: source control > REPOSITORIES > select your repo > three dots > `pull,push` > `push to` > provide remote
  - pull: download changes from remote repository to local repository
    - terminal: `git pull origin <branch>`
    - vscode: source control > REPOSITORIES > select your repo > three dots > `pull,push` > `pull from` > provide remote
* create branch
  - terminal:
    - create new branch from current branch: `git checkout -b <branch name>`
    - create new branch from a specific branch: `git checkout -b <branch name> <base branch>`
  - vscode:
    - create new branch from current branch: source control > REPOSITORIES > select your repo > three dots > `branch` > `create branch` > enter `<branch name>`
    - create new branch from a specific branch: source control > REPOSITORIES > select your repo > three dots > `branch` > `create branch from` > enter `<base branch>` and then enter `<branch name>`
    - or from status bar: click on the current branch name > `create new branch` or `create new branch from` > enter `<branch name>` or select `<base branch>` and then enter `<branch name>`
* switch (checkout) branch
  - terminal: `git checkout <branch name>`
  - vscode: source control > REPOSITORIES > select your repo > three dots  > `checkout to` > enter `<branch name>`
  - or from status bar: click on the current branch name  > select `<branch name>` to switch to it
* push local branch to remote (remote may not have the branch)
  - first need to switch to the branch you want to push, like `feature` branch: `git checkout feature`
  - terminal: `git push origin feature`
  - vscode: source control > REPOSITORIES > select your repo > three dots > `pull,push` > `push to` > provide remote (origin)
* pull remote branch to local
  - local branch have not created:
    - terminal:
      - `git fetch origin` (fetch remote including all branches)
      - `git checkout -b <branch name> origin/<branch>` (create local branch from remote branch)
    - vscode:
      - source control > REPOSITORIES > select your repo > three dots > `pull,push` > `fetch from all remotes` or `fetch` (from default remote, like `origin`)
      - source control > REPOSITORIES > select your repo > three dots > `create branch from` > select `origin/<branch>` > type  `<branch name>`
  - branch is already created, just need to switch to it
    - terminal: `git checkout <branch name>` and then `git pull origin <branch name>`
    - vscode: source control > REPOSITORIES > select your repo > three dots > `pull,push` > `pull from` > provide remote branch (origin/<branch>)
* merge branch
  - terminal:
    - switch to receiving branch, like main: `git checkout main`
    - merge: `git merge <feature>` (merge feature branch into current branch)
  - vscode:
    - source control > REPOSITORIES > select your repo > three dots > `checkout to` > enter `<branch name>` (switch to receiving branch)
    - source control > REPOSITORIES > select your repo > three dots > `branch` >  `merge branch` > enter `<feature branch name>` (merge the feature branch into current branch)
* rebase branch (update base to current branch)
  - terminal:
    - switch to receiving branch like feature: `git checkout feature`
    - rebase: `git rebase main` (update new base from main)
  - vscode:
    - source control > REPOSITORIES > select your repo > three dots > `checkout to` > enter `feature` (switch to the branch you want to rebase)
    - source control > REPOSITORIES > select your repo > three dots > `branch` >  `rebase branch` > enter `main` (rebase the main branch onto feature branch)
* delete local branch
  - first switch to another branch, like main: `git checkout main`
  - terminal:
    - delete local branch: `git branch -d <branch name>` (delete local branch)
  - vscode:
    - source control > REPOSITORIES > select your repo > three dots > `branch` > `delete branch` > enter `<branch name>` (delete local branch)
* git output window
  - terminal: `git log --oneline --graph` (view commit history)
  - vscode: view > output > select `git` from the dropdown > view git output window