# Git Tutorial

Simple git tutorial with main tricks and practices to help you get going.

## Some theory

Git history is a directed acyclic graph.
Each node of the graph points to a commit.


## Aliases

Please add it (or anything like it) to your `~/.gitconfig` file:

```
[alias]
lg1 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
lg2 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all
lg = !"git lg1"
```

## Important Commands!

### `git help`
You can use `git help <command>` or `git help -a` to see a list of commands with help available.

### `git rebase` for cut and paste
`git help rebase` :trollface:

Anyway, `git checkout <new-branch>` and then `git rebase <target-branch>` should put all commits from `<new-branch>` 
on top of `<target-branch>`.

If you want a little bit more flexibility `git rebase --onto <target-branch> <commit-range>` should do the trick.
`<target-branch>` is where the range of commits will be applied to.
`<commit-range>` is a commit interval that is open on the left.
This means that if `<commit-range> == 4d45edc c252711`, every commit from `4d45edc` (not included) to `c252711` (inclusive) will be rebased.

### `git rebase` for fancy stuff
You can always use `git rebase -i <base-commit>` to fix messed up histories.
Let's try it on the `feat/messed-up` branch.
This is an iterative command and comes with a tutorial embeded.
