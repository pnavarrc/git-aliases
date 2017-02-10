# git-aliases

Personal `git` aliases

<a href="https://zenhub.com"><img src="https://raw.githubusercontent.com/ZenHubIO/support/master/zenhub-badge.png"></a>

## How to Add the Aliases

```
git clone git@github.com:pnavarrc/git-aliases.git
git config --global --add include.path "$(pwd)/git-aliases/.gitaliases"
```

## Aliases

#### Standup

`git standup`

Show the commit messages between 12pm yesterday and 12pm today. Adapted from https://bitbucket.org/tpettersen/git-aliases

#### Skip CI (Travis)

`git skipci <commit message>`

Change the commit message to skip the Travis build. It’s equivalent to call `git commit -am '[skip ci] commit message'`.

## Learn More

[Git Aliases (docs)](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
[Tim Pettersen Aliases](https://bitbucket.org/tpettersen/git-aliases)
