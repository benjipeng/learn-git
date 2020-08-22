# Branching Operations
## “HEAD”
`HEAD` is the symbolic name for the currently checked out commit -- **it's the commmit that are being worked on top of.**
> By default, `HEAD` points to the most recent commit in the working branch/tree.

`git checkout <commit>` will detach `HEAD` from branch and attach to the commit.

A `branch` is an independent line of devlopment.
## `git branch`
- [x] `git branch <branch-name>`: Creates a new branch that has `{branch-name}`.
- [x] `git branch`: Equals to `git branch --list`
- [x] `git branch -d <branch>`: Deletes the specified `<branch>`, replace `-d` flag with `-D` flag for force deletion.
- [x] `git branch -m <branch>`: Rename the current branch.
- [x] `git branch -a`: List all remote branches.
- [x] `git branch -f <branch>`: Force branching to the `HEAD`

  
Will dive into more details laters.
## `git checkout`
`git checkout` can checkout the `<new-branch>` that is created by `git branch`. Additionally:
- [x] `git checkout -b <new-branch>`: Creates `<new-branch>` off the current `HEAD` and checkout into it.
- [x] `git checkout -b <new-branch> <existing-branch>`: Create `<new-branch>` off `<existing-branch>` instead of off teh current `HEAD` pointer.

## Git Reset
`git reset` reverts changes by moving a branch reference backwards in time to an older commit. In this sense you can think of it as "rewriting history;" git reset will move a branch backwards as if the commit had never been made in the first place.

# Git Rebase
>`Rebasing` takes a set of commits, "copies" them, and plops them down somewhere else.

>The Advantage of rebasing is that it can make a nice linear sequence of commits, making the commit log / history of the repository a lot cleaner.

`git rebase <branch>` rebase the current branch onto `<branch>`.