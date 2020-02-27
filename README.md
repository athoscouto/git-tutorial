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

### `git cherry-pick`

`git cherry-pick <commit-list>` applies the change each listed commit introduces, recording a new commit for each.
If you screwed it up, you can always `git cherry-pick --abort`.

Let's try `git cherry-pick 29e1a3a`.
