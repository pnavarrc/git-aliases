# `git-aliases`

> Git aliases for humans

This is a small collection of [Git aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases) designed to be descriptive and easy to remember.

## Table of contents

- [Getting started](#getting-started)
- [Aliases](#aliases)
  - [🌱 Working with branches](#-working-with-branches)
    - [Creating a branch](#creating-a-branch)
    - [Renaming a branch](#renaming-a-branch)
    - [Deleting a branch](#deleting-a-branch)
    - [Switching branches](#switching-branches)
    - [Show the name of the current branch](#show-the-name-of-the-current-branch)
  - [🔄 Syncing changes](#-syncing-changes)
    - [Push the current branch](#push-the-current-branch)
  - [🏷 Working with tags](#-working-with-tags)
    - [Listing all tags](#listing-all-tags)
    - [Create a new tag](#create-a-new-tag)
    - [Push tags to origin](#push-tags-to-origin)
  - [📝 Making (and fixing)changes](#-making-and-undoing-changes)
    - [Rewriting the commit message](#rewriting-the-commit-message)
    - [Undo a commit](#undo-a-commit)
    - [Un-add a file](#undo-adding-a-file)
    - [Create an empty commit](#create-an-empty-commit)
  - [Working with remotes](#working-with-remotes)
    - [Listing your remotes](#listing-your-remotes)
    - [Adding a remote](#adding-a-remote)
    - [Removing a remote](#removing-a-remote)
  - [Other commands](#other-commands)
  - [What did I do yesterday?](#what-did-i-do-yesterday)
- [📚 Learn more](#-learn-more)

## Getting started

If you like the aliases in this repo you can just install them locally and use them:

```sh
git clone git@github.com:pnavarrc/git-aliases.git
git config --global --add include.path "$(pwd)/git-aliases/git-aliases"
```

If you prefer to customize them, you can fork the repo and add your own aliases, or you can [create an issue](https://github.com/pnavarrc/git-aliases/issues) or [submit a pull request](https://github.com/pnavarrc/git-aliases/pulls) if you think that the command could be useful for others.

## Aliases

### 🌱 Working with branches

#### Creating a branch

Creates a branch from the current branch.

```sh
git create-branch <branch-name> # or alternatively
git new-branch <branch-name>
```

This is equivalent to `git branch -b <branch-name>`. If you want to prefix the branch name with your local username:

```sh
git my-new-branch branch-name
```

This will create a new branch named `username/branch-name`. It relies on the environment variable `$USER`.

#### Renaming a branch

Renames the current branch to `new name`.

```sh
git rename-branch <new-name>
```

#### Deleting a branch

Deletes the branch `branch-name`. Note that it won't delete the current branch, you need to switch branched before deleting the branch.

```sh
git delete-branch <branch-name>
```

#### Switching branches

Switches to `branch-name`

```sh
git switch-branch <branch-name>
```

To switch to the previous branch, run:

```sh
git prev-branch
```

This is equivalent to run `git checkout -`.

#### Show the name of the current branch

```sh
git current-branch
```

### 🔄 Syncing Changes

#### Push the current branch

Pushes the current branch and latest changes to `origin`

```sh
git push-current-branch
```

The following commands pull changes from `origin` to the `main` and `develop` branches respectively. It doesn't push changes to avoid pushing changes to important branches by mistake (you can use `git push-current-branch` for this)

```sh
git update-main
git update-develop
```

### 🏷 Working with tags

#### Listing all tags

```sh
git list-tags
```

#### Create a new tag

Create a new tag and open the editor to write the tag message and notes.

```sh
git create-tag v1.2.3
git new-tag v1.2.3
```

#### Push tags to origin

```sh
git push-tags
```

### 📝 Making (and undoing) changes

#### Rewriting the commit message

Replaces the commit message of the last commit with `new commit message`.

```sh
git amend-commit-message <new commit message>  # or
git rewrite-commit-message <new commit message>
```

#### Undo a commit

Resets to the previous commit, leaving the working tree unchanged.

```sh
git undo-commit
```

#### Undo adding a file

Removes a file accidentally added to Git (specifically, added to the staging area) _before_ creating a commit.

```sh
git undo-add <file>  # or
git unstage <file>
```

#### Create an empty commit

An emtpy commit can help re-trigger a CI automation without making any changes to the code.

```sh
git create-empty-commit <commit message>  # or
git empty-commit <commit message>
```

This is equivalent of `git commit --allow-empty -m <commit message>`.

### Working with remotes

#### Listing your remotes

```sh
git list-remotes
```

#### Adding a remote

```sh
git add-remote <name> <url>
```

#### Removing a remote

```sh
git remove-remote <name>
```

### Other commands

### What did I do yesterday?

Show the commit messages in the last 24 hours. Adapted from https://bitbucket.org/tpettersen/git-aliases

```sh
git standup
```

## 📚 Learn more

- [Git Aliases (docs)](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
- [Tim Pettersen Aliases](https://bitbucket.org/tpettersen/git-aliases)
