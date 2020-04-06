# git-aliases

_Personal `git` aliases_

**NOTE**: Most people create short aliases to save time, aliases in this repo optimize for legibility and to make certain operations more explicit.

## Installing

```sh
$ git clone git@github.com:pnavarrc/git-aliases.git
$ git config --global --add include.path "$(pwd)/git-aliases/git-aliases"
```

## Usage

### Branches

#### `git create-branch ` _`<branch name>`_

Creates a branch from the current branch.

#### `git rename-branch `_`<new branch name>`_

Renames the current branch to _`new branch name`_

#### `git current-branch`

Displays the name of the current branch

#### `git push-current-branch`

Pushes the current branch to `origin`

#### `git list-merged-branches `_`<branch name>`_

### Commits

#### `git quick-commit <commit-message>`

Create a signed commit, adding unstaged changes.

#### `git skipci <commit message>`

Change the commit message to skip the Travis build. It’s equivalent to call `git commit -am '[skip ci] commit message'`.

#### `git amend-commit-message <commit message>`

Replaces the commit message of the last commit

#### `git qc <commit-message>`

Alias for [`quick-commit`](#git-quick-commit-commit-message)

#### `git unstage <file>`

Remove `file` from the staging area.

#### `git undo-commit`

Resets to the previous commit, leaving the working tree unchanged (`git reset --soft HEAD~1`).

### Logs

#### `git log-branch`

List the commits in the current branch that are not in the `master` branch. 

### Other Commands

### `git standup`

Show the commit messages in the last 24 hours. Adapted from https://bitbucket.org/tpettersen/git-aliases

## Learn More

- [Git Aliases (docs)](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
- [Tim Pettersen Aliases](https://bitbucket.org/tpettersen/git-aliases)
