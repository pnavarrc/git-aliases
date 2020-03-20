# git-aliases

_Personal `git` aliases_

**NOTE**: Most people create short aliases to save time, aliases in this repo optimize for legibility and to make certain operations more explicit.

## How to Add the Aliases

```sh
$ git clone git@github.com:pnavarrc/git-aliases.git
$ git config --global --add include.path "$(pwd)/git-aliases/git-aliases"
```

## Aliases

### `git standup`

Show the commit messages in the last 24 hours. Adapted from https://bitbucket.org/tpettersen/git-aliases

### `git skipci <commit message>`

Change the commit message to skip the Travis build. It’s equivalent to call `git commit -am '[skip ci] commit message'`.

### `git current-branch`

Shows the name of the current branch.

### `git push-current-branch`

Push the current branch to `origin`.

### `git amend-commit-message <commit message>`

Replaces the commit message of the last commit

### `git list-merged-branches <branch>`

List local branches merged to `<branch>`. Useful to delete merged branches.

### `git quick-commit <commit-message>`

Create a signed commit, adding unstaged changes.

### `git qc <commit-message>`

Alias for [`quick-commit`](#git-quick-commit-commit-message)

### `git create-branch`

Create a branch from the current branch.

### `git unstage <file>`

Remove `file` from the staging area.

## Learn More

[Git Aliases (docs)](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
[Tim Pettersen Aliases](https://bitbucket.org/tpettersen/git-aliases)
