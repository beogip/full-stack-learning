# Git

## What is git?

[Git](https://git-scm.com/) is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development.

## Common commands

### Git Clone

This command is used for downloading the latest version of a remote project and copying it to the selected location on the local machine. It looks like this:

```bash
git clone <repository url>
```

To clone a specific branch, you can use

```bash
git clone <repository url> -b <branch name>
```

### Git Fetch

This Git command will get all the updates from the remote repository, including new branches.

```bash
git fetch
```

### Git Checkout

You can use the checkout command to switch the branch that you are currently working on.

```bash
git checkout <branch name>
```

If you want to create a new branch and switch to it, you can do it by using this command:

```bash
git checkout -b <branch name>
```

### Git Init

This is the command you need to use if you want to start a new empty repository or to reinitialize an existing one in the project root. It will create a .git directory with its subdirectories. It should look like this:

```bash
git init <repository name>
```

### Git Commit

This one is probably the most used Git command. After changes are done locally, you can save them by “committing” them. A commit is like local a snapshot of the current state of the branch, to which you can always come back. To create a new commit, type this command in Git Bash:

```bash
git commit -m "<commit message>"
```

### Git Push

Git push will push the locally committed changes to the remote branch. If the branch is already remotely tracked, simply use it like this (with no parameters):

```bash
git push
```

If the branch is not yet tracked, and only resides on the local machine, you need to run the command like this:

```bash
git push --set-upstream <remote branch> <branch name>
```

### Git Diff

You can use this command to see the unstaged changes on the current branch.

```bash
git diff
```

If you want to see the staged changes, run the diff command like this:

```bash
git diff --staged
```

Or you can compare two branches:

```bash
gif diff <branch1> <branch2>
```

### Git Pull

Using git pull will fetch all the changes from the remote repository and merge any remote changes in the current local branch.

```bash
git pull
```

### Git Add

This is the command you need to use to stage changed files. Remember that you need to add the files before committing. You can stage individual files:

```bash
git add <file path>
```

Or all files:

```bash
git add .
```

### Git Branch

Using git branch will list all the branches of the repository:

```bash
git branch
```

Or you can use it to create a new branch, without checking it out:

```bash
git branch <new branch>
```

To delete a branch, run it like this:

```bash
git branch -d <branch name>
```

### Git Merge

Merge a branch with the current branch

```bash
git merge <branch name>
```

## Pro tips

### Different flows

Exists different standard flows to work with git. Most used [GitFlow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) and [GithubFlow](https://docs.github.com/en/get-started/quickstart/github-flow)

### Commitizen

Angular created a standard for naming the commits known as [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). Exists several tools that facilitate the implementation. One of them is [Commitizen](https://commitizen-tools.github.io/commitizen/)
