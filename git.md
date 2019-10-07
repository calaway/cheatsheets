# Git CheatSheet

## git diff
```bash
git diff # Show changes between commits, commit and working tree, etc
```

### Options
```bash
-—cached # compares the index to the repository
```

## git rebase
### Examples
```bash
# Interactively rebase the last 4 commits
git rebase -i|--interactive HEAD~4
```

## git show
### Examples
```bash
# Show changes made by the commit before the last commit
git show HEAD^
```
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

git revert <commit>
  Have git create a new commit that reverses changes made in a prior commit.

git cherry-pick <commit>
  Apply changes from a particular commit to the current branch

git cherry-pick <commit_x>..<commit_y>
  Apply changes from the range of commits from x (not included) through y (included) to the current branch
