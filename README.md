# git-aliases

_Personal `git` aliases_

**NOTE**: Most people create short aliases to save time, aliases in this repo optimize for legibility and to make certain operations more explicit.

## How to Add the Aliases

```sh
$ git clone git@github.com:pnavarrc/git-aliases.git
$ git config --global --add include.path "$(pwd)/git-aliases/git-aliases"
```

## Aliases

### Branch Management

| Alias |  Description | Git Equivalent |
|--|--|---|
| `create-branch <branch-name>` | Creates a branch from the current branch | `git checkout -b <branch-name>` |
| `rename-branch <new-branch-name>` | Renames the current branch | `git branch -m <new-branch-name>` |
| `current-branch` | Displays the name of the current branch | `git symbolic-ref --quiet --short HEAD` |
| `push-current-branch` | Push the current branch to `origin` | `git push -u <local-branch-name>` |
| `list-merged-branches <branch-name>` | List branches merged into the branch `branch-name` | `git branch --merged $1 \| grep --invert-match '\\*'` |

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

### Other Commands

### `git standup`

Show the commit messages in the last 24 hours. Adapted from https://bitbucket.org/tpettersen/git-aliases

## Learn More

- [Git Aliases (docs)](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
- [Tim Pettersen Aliases](https://bitbucket.org/tpettersen/git-aliases)
