# Git

## Find git version

`$ git --version`

## Create or open a file from git

`$ touch [file_name.extension]`

## Set email and name

`$ git config --global user.name [username]`

`$ git config --global user.email [email]`

## Intialize repository

`$ git init`

## Adding one specific file to local repository

`$ git add [file_name.extension]`

## Adding specific files to local repository

`$ git add *.html`

## Adding all the files to local repository

`$ git add .`

## Remove files from staging area

`$ git rm --cached [file_name.extension]`

## Removing files with folders

`$ git rm -r [directory]`

## Status

`$ git status`

## Comitting using vim editor

`$ git commit`

> Enter `i` to get into insert mode.
> Remove `#` which is near the initial commit.
> Press `esc` key to get out form insert mode.
> Type `:wq` and hit enter to write and quit.

## Committing changes

`$ git commit -m "[comment]"`

## Logging the commits

`$ git log`

## Undoing last commit

`$ git rest --soft HEAD~1`

## Reseting a commit

`$ git reset [wrong_commit_parent_id]`

> Git commits are stored like a linked list structure so`[wrong_commit_parent_id]` is commit id for commit happened before the wrong commit. `$ git log` can be used to see the commit ids.

## Reverting a commit

`$ git revert [wrong_commit_parent_id]`

> Git revert is like a `$ git reset` but `$ git revert` commit the revertion as a new commit which `$ git reset` command doesn't do.

## Git ignore

`$ touch .gitignore`

## Creating branch

`$ git branch [branch_name]`

## Renaming a branch

`$ git branch -m [old_branch_name] [new_branch_name]`

`$ git branch -m [new_branch_name]`

> Renames the main branch.

## Switching between branch

`$ git checkout [branch_name]`

## Merging branch with main branch

`$ git merge [branch_name]`

> Type `i` to insert mode.
> Add a message for the merge.
> Press `esc` key to get out from insert mode.
> Type `:wq` and press enter to write and quit.

## Connecting to remote repository

`$ git remote`

`$ git remote add orgin [repository_link]`

## Changing remote repository

`$ git remote set-url origin [repository_link]`

## Pushing to github

`$ git push -u origin main`

## Pull from remote repo

`$ git pull`

## Cloning repo

`$ git clone [repository_link]`

## Setting gpg key globally

`git config --global user.signingKey [secret_key_id]`

## Sign git commits with gpg key

`git config --global commit.gpgsign true`
