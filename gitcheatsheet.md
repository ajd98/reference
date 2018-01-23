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
| Remove files that were never added to the git repository | `git clean -fr` |

Note that after moving or removing a file, you will need to commit the change using `git commit -m "commit message"`. It is not necessary to run `git add <filename>` on this file before commiting the move/remove operation.

