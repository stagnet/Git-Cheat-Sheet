# Git-Cheat-Sheet
A cheat sheet for uncommon Git commands

## Configuration
| Command | Description |
| - | - |
| `git config --global user.name "foo"`     | Set user name |
| `git config --global user.email "foo"`    | Set user email |

## Branches
| Command | Description |
| - | - |
| `git branch foo`                          | Create a new branch |
| `git checkout foo`                        | Switch to a branch |
| `git merge foo`                           | Merge branch into current branch |

## Pulling
| Command | Description |
| - | - |
| `git pull --rebase --prune`               | Get latest, rebase any changes not checked in and delete branches that no longer exist | 

## Staged Changes
| Command | Description |
| - | - |
| `git mv file1.txt file2.txt`              | Move/rename file |
| `git rm --cached file.txt`                | Unstage file |
| `git rm --force file.txt`                 | Unstage and delete file |
| `git reset HEAD`                          | Unstage changes |
| `git reset --hard HEAD`                   | Unstage and delete changes |

## Changing Commits
| Command | Description |
| - | - |
| `git reset 5720fdf`                        | Reset current branch but not working area to commit |
| `git reset --hard 5720fdf`                 | Reset current branch and working area to commit |
| `git commit --amend -m "New message"`      | Change the last commit message |
| `git revert 5720fdf`                       | Revert a commit |
| `git rebase --interactive [origin/master]` | Rebase a PR (`git pull` first) |
| `git rebase --interactive sa78d6s`         | Rebase to a particular commit |
| `git rebase --continue`                    | Continue an interactive rebase |
| `git rebase --abort`                       | Cancel an interactive rebase |

## Compare
| Command | Description |
| - | - |
| `git diff`                                | See difference between working area and current branch |
| `git diff HEAD HEAD~2`                    | See difference between te current commit and two previous commits |
| `git diff master other`                   | See difference between two branches |

## View
| Command | Description |
| - | - |
| `git log`                                 | See commit list |
| `git log --patch`                         | See commit list and line changes |
| `git log --decorate --graph --oneline`    | See commit visualization |
| `git log --grep foo`                      | See commits with foo in the message |
| `git show HEAD`                           | Show the current commit |
| `git show HEAD^` or `git show HEAD~1`     | Show the previous commit |
| `git show HEAD^^` or `git show HEAD~2`    | Show the commit going back two commits |
| `git show master`                         | Show the last commit in a branch |
| `git show 5720fdf`                        | Show named commit |
| `git blame file.txt`                      | See who changed each line and when |

## Stash
| Command | Description |
| - | - |
| `git stash push -m "Message"`             | Stash staged files |
| `git stash --include-untracked`           | Stash working area and staged files |
| `git stash list`                          | List stashes |
| `git stash apply`                         | Moved last stash to working area |
| `git stash apply 0`                       | Moved named stash to working area |
| `git stash clear`                         | Clear the stash |

## Remote
| Command | Description |
| - | - |
| `git remote -v`                           | List remote repositories |
| `git remote show origin`                  | Show remote repository details |
| `git remote add upstream <url>`           | Add remote upstream repository |
| `git fetch upstream`                      | Fetch all remote branches |
| `git rebase upstream/master`              | Refresh master branch from upstream |
| `git remote -v`                           | List remote repositories |
| `git push --tags`                         | Push tags to remote repository |
