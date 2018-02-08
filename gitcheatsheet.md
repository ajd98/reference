# git "cheat sheet"

## Setting up a new repository

| Task       | Command    |
|------------|------------|
| Initialize a new git repository | `git init` |
| Set the remote for the repository | `git remote add origin https://github.com/<username>/<repositoryname>.git`  |
| Push the repository to the remote and set up tracking | `git push -u origin master` |
| Set the email to be associated with commits (only necessary for your first repository) | `git config user.email <email>` |
| Set the name to be associated with commits (only necessary for your first repository) | `git config user.name <name>` |

## Adding and modifying files

| Task       | Command    |
|------------|------------|
| Add a new file | `git add <filename>` |
| Stage a file for committing (must be done after editing a file and before committing the changes) | `git add <filename>` |
| Commit (or "save") changes | `git commit -m "commit message" ` | 
| Move a file | `git mv <current file name> <new file name>` | 
| Remove a file | `git rm <filename>` |
| Restore a file to its state at the most recent commit | `git checkout -- <filename>` |
| Remove files that were never added to the git repository | `git clean -fd` |
| Check what changes have been made but not commited | `git diff <filename>` |
| Check the history of committed changes | `git log` |

Note that after moving or removing a file, you will need to commit the change using `git commit -m "commit message"`. It is not necessary to run `git add <filename>` on this file before commiting the move/remove operation.

## Staying up-to-date with a remote repository

| Task       | Command    |
|------------|------------|
| Copy any commited changes from your local repository to the remote repository | `git push` |
| Copy any changes from the remote repository to your local repository | `git pull` |

## Working with branches

| Task       | Command    |
|------------|------------|
| Create a new branch | `git checkout -b <branchname>` |
| Switch to a branch that already exists | `git checkout <branchname>` |
| Apply changes in one branch to another branch | `git checkout <basebranch>`, then `git merge <featurebranch>` |
| Push a new branch to remote and set upstream tracking | `git push -u origin <branchname>` |

Notes: Often, git repositories have a `master` branch, which contains a "main" version of the code; this code is also often working (rather than broken due to unfinished changes).  Changes are implemented in feature branches, the purpose of which is to compartmentalize development of a particular feature or bug fix.  Feature branches are merged into `master` as they are completed.  GitHub has a "pull request" feature that may be used to request merges of one branch into another branch--this feature will alert other developers associated with the repository that a merge is being requested, and those developers can then review the changes, comment on the changes, and ultimately approve the changes.
