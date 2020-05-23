# Git sheet

[Git](http://git-scm.com) - is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency

## 1. [Configure tooling](#configure-tooling)
## 2. [Create repositories](#create-repositories)
## 3. [The .gitignore file](#the-gitignore-file)
## 4. [Synchronize changes](#synchronize-changes)
## 5. [Branches](#branches)
## 6. [Make changes](#make-changes)
## 7. [Redo commits](#redo-commits)

## Glossary

1. **git**: an open source, distributed version-control system

2. **GitHub**: a platform for hosting and collaborating on Git repositories

3. **commit**: a Git object, a snapshot of your entire repository compressed into a SHA

4. **branch**: a lightweight movable pointer to a commit

5. **clone**: a local version of a repository, including all commits and branches

6. **remote**: a common repository on GitHub that all team members use to exchange their changes

7. **fork**: a copy of a repository on GitHub owned by a different user

8. **pull request**: a place to compare and discuss the differences introduced on a branch with reviews, comments, integrated tests, and more

9. **HEAD**: representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits when using ```git checkout```

## Configure tooling
(Configure user information for all local repositories)

1. Sets the name you want attached to your commit transactions
```
$ git config --global user.name "[name]"
```
2. Sets the email you want attached to your commit transactions
```
$ git config --global user.email "[email address]"
```
3. Enables helpful colorization of command line output
```
$ git config --global color.ui auto
```

## Create repositories
(When starting out with a new repository, you only need to do it once; either locally, then push to GitHub, or by cloning an existing repository)

1. Initializes the git in your folder
```
$ git init
```
2. After using the git init command, link the local repository to an empty GitHub repository using the following command(turn an existing directory into a Git repository):
```
$ git remote add origin [url]
```
3. Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits
```
$ git clone [url]
```

## The .gitignore file

Sometimes it may be a good idea to exclude files from being tracked with Git. This is typically done in a special file named .gitignore. You can find helpful templates for .gitignore files at [GitHub](http://github.com/github/gitignore).

## Synchronize changes
(Synchronize your local repository with the remote repository)

1. Downloads all history from the remote tracking branches
```
$ git fetch
```
2. Combines remote tracking branches into current local branch
```
$ git merge
```
3. Uploads all local branch commits to GitHub
```
$ git push
```
4. Updates your current local working branch with all new commits from the corresponding remote branch on GitHub (**git pull** is a combination of ```git fetch``` and ```git merge```)
```
$ git pull
```

## Branches
(Branches are an important part of working with Git. Any commits you make will be made on the branch you’re currently “checked out” to)

1. Use it to see which branch that is and in which state are you now
```
$ git status
```
2. Creates a new branch
```
$ git branch [branch-name]
```
3. Switches to the specified branch and updates the working directory
```
$ git checkout [branch-name]
```
4. Combines the specified branch’s history into the current branch. This is usually done in pull requests, but is an important Git operation
```
$ git merge [branch]
```
5. Deletes the specified branch in local
```
$ git branch -d [branch-name]
```
6. Deletes the specified branch from remote repository and local
```
$ git branch -D [branch-name]
```

## Make changes
(Browse and inspect the evolution of project files)

1. Lists version history for the current branch
```
$ git log
```
2. Lists version history for a file, including renames
```
$ git log --follow [file]
```
3. Shows content differences between two branches
```
$ git diff [first-branch]...[second-branch]
```
4. Outputs metadata and content changes of the specified commit
```
$ git show [commit]
```
5. Snapshots the file in preparation for versioning
```
$ git add [file]
```
6. Records file snapshots permanently in version history
```
$ git commit -m"[descriptive message]"
```

## Redo commits
(Erase mistakes and craft replacement history)

1. Undoes all commits after ```[commit]```, preserving changes locally
```
$ git reset [commit]
```
2. Discards all history and changes back to the specified commit
```
$ git reset --hard [commit]
```
