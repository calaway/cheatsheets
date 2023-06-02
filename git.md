# Git CheatSheet

## Subcommand Examples

### git diff
```bash
# Changes in the working tree not yet staged for the next commit.
git diff

# Changes between the index and your last commit; what you would be committing if you run "git commit" without "-a" option.
git diff --cached

# Changes in the working tree since your last commit; what you would be committing if you run "git commit -a"
git diff HEAD
```

### git rebase
```bash
# Interactively rebase the last 4 commits
git rebase (-i|--interactive) HEAD~4
```

### git restore
```bash
# Drop changes to a file in the working tree by replacing it with the copy from the repo
git restore package-lock.json

# Copy file(s) from another branch
git restore --source=my-other-branch README.md

# Copy files(s) from two versions back
git restore --source master~2 Makefile
```

### git revert
```bash
# Revert commit c780a34 and save the changes in a new commit
git revert c780a34

# Revert commit c780a34 in the working tree without creating a new commit
git revert (-n|--no-commit) c780a34

# Revert the last three commits without creating a new commit
g revert --no-commit HEAD~3..
```

### git show
```bash
# Show changes made by the commit before the last commit
git show HEAD^
```

### Other Notes
git rm —cached
  remove from index, but not working directory (i.e. unstage file)

git reset --hard <commit>
  move branch, working area, and index to commit

git reset HEAD
  unstage files

git reset --hard HEAD
  delete any changes since last commit as well as unstage any

git reset HEAD path/to/file.txt
  delete any changes to specific file since last commit in index only (cannot be used with --hard)

git checkout HEAD path/to/file.txt
  copy changes from HEAD or commit to working directory & index

git log --graph --decorate --oneline
  graph: add lines that follow branches or commit chains

  decorate: show positional references, like branches or HEAD

  oneline: one line per commit

git show HEAD~2 or git show HEAD^^
  show details on commit two before HEAD

Golden Rule:
  Never rebase shared commits. That is, once you push a commit to a shared repository, from that moment on you should avoid rebasing that commit.

git commit --amend
  Amend the prior commit with the new changes that have been staged. (Technically replaces the amended commit.)

git reflog
  Print log of changes to commit that HEAD reverence, including checkouts

git cherry-pick <commit>
  Apply changes from a particular commit to the current branch

git cherry-pick <commit_x>..<commit_y>
  Apply changes from the range of commits from x (not included) through y (included) to the current branch
