# Git commands

## install

```sh
apt install git git-gui
```

## commands gui

```sh
git gui
git gui blame {path_to_file}
```

git log
```sh
gitk
gitk modules/auth/models/multifactor-authentication.go
```


## Config

```sh
git config --global user.email {email}
git config --global user.name {username}
git config --global core.editor vim

git config --local --list
```

## basic commands

get all commits and branches
```sh
git fetch --all
```

show changed files in commit
```sh
git diff-tree --no-commit-id --name-only -r {hash_commit}
```

show changes in commit
```sh
git show {hash_commit}
git show {hash} -- {path_file}
```

show changes in commit (for merged commit use this)
```sh
git diff {hash_commit}~
```

show changes files in commit
```sh
git diff --name-status {hash_commit}~
```

show changes last 5 commit
```sh
git show HEAD~5
```

Show changes NOT indexed
```sh
git diff
```

Show changes indexed
```sh
git diff --staged
```


roll back changes in the file to the last commit
```sh
git checkout {path_file}
```

roll back changes in a file to a specific commit
```sh
git checkout {hash_commit} {path_file}
```

cancel file indexing (unstage)
```sh
git reset HEAD {path_file}
```

rename last commit message
```sh
git commit --amend -m 'new commit message'
```

deleting the file from the git and locally
```sh
git rm {path_file}
```

deleting the file ONLY from the git
```sh
git rm --cached {path_file}
```

## git remote

get repo
```sh
git remote -v
```

set new remote url
```sh
git remote set-url origin git@github.com:{USERNAME}/{REPOSITORY}.git
```

```sh
git remote add github-origin git@github.com:{USERNAME}/{REPOSITORY}.git
```

add new origin
```sh
git remote rename origin old-origin
git remote add origin {repo}
git push --set-upstream origin {branch}
```


## git reset last commit

```sh
git reset HEAD~1
# or
git reset --hard HEAD~1
git reset --hard {commit_hash}

git reset --soft {commit_hash}
```

```sh
git push origin {branch} --force
```

## git merge only one commit from branch

```sh
git cherry-pick {commit_hash}
```

## git tag

after commit code
```sh
git tag -a {tag_name} -m "{message}" -l {hash_commit}
git push origin {tag_name}
git push origin {branch} --tags

# create tag with edit message
git tag -a {tag_name} -e
```

show message
```sh
git tag -n3
```

sort tags
```sh
git tag -l | sort -V
git tag -l --sort=v:refname
```

delete tag local
```sh
git tag -d {tag_name}
```

## merge

abort merge
```sh
git reset --hard HEAD
```

or
```sh
git merge --abort
```

## submodules

init submodules
```sh
git submodule update --init
```

```sh
git submodule update -f --recursive
```

### set branch

```sh
git submodule set-branch --branch {branch} -- {path_to_submodule}
git submodule update --remote
```

### add

```sh
git submodule add -b {branch} --reference {repository} {path_to_submodule}
```

### change url

```sh
git submodule set-url -- {path} {newurl}
```


## stash

```sh
git stash
git stash list
git stash apply
git stash apply stash@{2}
git stash drop stash@{n}
git stash pop stash@{0}

git stash show stash@{0}
# show diff
git stash show -p stash@{0}
```

git stash by name
```sh
git stash push -m "my_stash"
git stash list
git stash apply my_stash_name
```

## branch

branch rename
```sh
git branch -m {oldname} {newname}
# or
git branch -m {newname}
```

### compare branch

compare current branch with other branch
```sh
git diff {branch_name}
```

compare two branch
```sh
git diff {branch_1}..{branch_2}
```

list files changes
```sh
git diff --name-only {branch_name}
```

diff file
```sh
git diff {branch_name} {file_name}
git diff {hash} {file_name}
```


### diff file between two commits

```sh
git diff {hash_old}:{path_file} {hash}:{path_file}
git diff {hash_old} {hash} -- {path_file}
```

### file history

```sh
git log -- {path_file}
git log --patch -- {path_file}
```

### delete branch

local
```sh
git branch -D {branch_name}
```

remote
```sh
git push -d origin {branch_name}
```

## squash

```sh
git rebase -i {hash_commit or HEAD~number}
```
and replace "pick" on the second and subsequent commits with "squash" or "fixup"

example,
view 5 commits from the current HEAD in the past the command
```sh
git rebase -i HEAD~5
```

## Remove untracked files from the working tree

```sh
git clean -n -d
git clean -f
```

## difftool

```sh
git config diff.tool vimdiff
git difftool {branch_name}
git difftool {hash_commit}
```

## clone fast

```sh
git clone --depth 1 {repository}
```
