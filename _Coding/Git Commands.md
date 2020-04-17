# Useful Git Commands

## Remove remote branches that no longer exist

```[shell]
git remote prune origin --dry-run
```

## See when a file was deleted

```[shell]
git log --full-history -1 -- path\to\file
```

## See files that have changed between two branches

```[shell]
git diff --name-only branch1 branch2
```

## Remotes

```[shell]
git remote add origin https://github.com/jonathantwite/kontent-boats-vue.git
```

```[shell]
git remote remove origin
```

## Set upstream

```[shell]
git push -u origin master
```

## User

```[shell]
git config user.email "13119611+jonathantwite@users.noreply.github.com"
```

```[shell]
git config user.name "jonathantwite"
```

## Add changes to local commit

```[shell]
git add .
git commit --amend -no-edit
```

## Connect to different repos

### See all remotes

```[shell]
git remove -v
```

### Add/remove another remote

```[shell]
git remote add trainingrepo https://github.com/jonathantwite/dc-training.git
git remote remove trainingrepo
```

### Push specific branch to different branch on remote

```[shell]
git push trainingrepo publish:master
```
