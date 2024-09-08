## Git command-line interface

To avoid duplicating information, i am not going to explain the commands below in detail. See the highly recommended Pro Git for more information,

### Basics:

    git help <command>: get help for a git command
    git init: creates a new git repo, with data stored in the .git directory
    git status: tells you what’s going on
    git add <filename>: adds files to staging area
    git commit: creates a new commit.
    Write good commit messages!
    Even more reasons to write good commit messages!
    git log: shows a flattened log of history
    git log --oneline: visualizes history as a oneliner
    git diff <filename>: show changes you made relative to the staging area
    git diff <commitID/hash> <filename>: shows differences in a file between snapshots
    git checkout <commitID/hash|branchName >: updates HEAD to a commit or branch

### Branching and merging:

    git branch: shows branches

    git branch <name>: creates a branch

    git checkout -b <name>: creates a branch and switches to it same as
        git branch <name>; git checkout <name>

    git merge <revision>: merges into current branch

    git mergetool: use a fancy tool to help resolve merge conflicts *(i highly recomande to use VS CODE conflict resolver)*

    git rebase: rebase set of patches onto a new base

### Remotes:

    git remote: list remotes

    git remote add <name> <url>: add a remote

    git push <remote> <local branch>:<remote branch>: send  objects to remote, and update remote reference

    git branch --set-upstream-to=<remote>/<remote branch>:  set up correspondence between local and remote branch

    git fetch: retrieve objects/references from a remote

    git pull: same as git fetch; git merge

    git clone: download repository from remote

### Undo:

    git commit --amend: edit a commit’s contents/message

    git reset HEAD <file>: unstage a file

    git checkout -- <file>: discard changes

    git revert <commitHash>: removes content of a sprcific commit.

### Advanced Git

    git config: Git is highly customizable

    git clone --depth=1: shallow clone, without entire version history

    git add -p: interactive staging

    git rebase -i: interactive rebasing

    git blame: show who last edited which line

    git stash: temporarily remove modifications to working directory

    git bisect: binary search history (e.g. for regressions)

    .gitignore: specify intentionally untracked files to ignore

### Miscellaneous

- GUIs: there are many GUI clients out there for Git

- Shell integration: it’s super handy to have a Git status as part of your shell prompt (zsh, bash). Often included in frameworks like Oh My Zsh.

- Editor integration: similarly to the above, handy integrations with many features. fugitive.vim is the standard one for Vim.
- Workflows: we taught you the data model, plus some basic commands; we didn’t tell you what practices to follow when working on big projects (and there are many different approaches).
