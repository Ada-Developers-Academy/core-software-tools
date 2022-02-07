# Git Cheatsheet

[ Comprehensive Git Commands Cheat Sheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)


| Command | Description |
|--|--|
| `git clone <repo>` | Clone repo located at `<repo>` onto local machine. Original repo can be located on the local filesystem or on a remote machine via HTTP or SSH. |`git clone https://github.com/AdaGold/tdd-exercise.git`|
|`git status`| List which files are staged, unstaged, and untracked |
|`git add <directory>`| Stage all changes in `<directory>` for the next commit. Replace `<directory>` with a `<file>` to change a specific file. |
| `git push`| Update the remote repo with the local commits |
|`git log`| Display the entire commit history using the default format. For customization see additional options. |
|`git diff`| Show unstaged changes between your index and working directory. |
| `git fetch` | Download commits, files, and refs from a remote repository into your local repo. |
| `git merge` | Merge the commits that have been fetched from the remote repo into the local repo. |
| `git pull` | `git fetch` and `git merge` at the same time |

[(source)](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)