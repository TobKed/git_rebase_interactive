# Foundations

## Commands

* [`git commit –all / git commit -a`](#git-commit-all-git-commit-a)
* [`git commit --amend`](#git-commit-amend)
* [`git reflog`](#git-reflog)
* [`git adog`](#git-adog)
* [`git bdog`](#git-bdog)


## `git commit –all / git commit -a`

!!! quote "quote from _<https://git-scm.com/docs/git-commit#Documentation/git-commit.txt--a>_"

    **-a<br>
    --all**
    
    Tell the command to automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected.


!!! tip
    
    ```shell
    $ git commit -am "Meaingful message"
    ```

## `git commit --amend`

A convienient way to edit most recent commit.

!!! tip
    
    ```shell
    $ git commit --amend
    $ git commit --amend --no-edit
    $ git commit -a --amend --no-edit
    ```

## `git reflog`

!!! quote "quote from _<https://www.atlassian.com/git/tutorials/rewriting-history/git-reflog>_"

    Git keeps track of updates to the tip of branches using a mechanism called reference logs, or "reflogs."

!!! tip
    
    ```shell
    $ git reflog
    645670d (HEAD -> docs, origin/docs) HEAD@{0}: commit (amend): Add docs
    22e7f0a HEAD@{1}: commit (amend): Add docs
    ea96a12 HEAD@{2}: commit (amend): Add docs
    32e1a3e HEAD@{3}: rebase (finish): returning to refs/heads/docs
    32e1a3e HEAD@{4}: rebase (fixup): Add basic docs
    81ec1df HEAD@{5}: rebase (start): checkout origin/master
    e574581 HEAD@{6}: checkout: moving from master to docs
    ```

## `git adog`

![adog](https://i.stack.imgur.com/ElVkf.jpg)

_source <https://stackoverflow.com/a/35075021>_

!!! info "`.gitconfig`"
    
    ```shell
    [alias]
        adog = log --all --decorate --oneline --graph
    ```

!!! info

    ```shell
    $ git adog
    * 9cc057f (origin/datastudio-sql-user, datastudio-sql-user) Datastudio sql user
    * 9b238ce (HEAD -> budgeting-k8s, origin/master, master) Add gke cluster (#3)
    | * fae80dc (refs/stash) On master: autostash
    |/|
    | * f507a23 index on master: d9b7ec4 Add db backups (#2)
    |/
    | * fbf294e (origin/add-k8s, add-k8s) fixup! fixup! Add gke cluster
    ```

## `git bdog`

Show all commits from current branch to the parent branch.

!!! info "`.gitconfig`"
    
    ```shell
    [alias]
        bdog = "!f() { git log $1..@ --decorate --oneline --graph; unset -f f; }; f"
    ```

!!! tip
    
    ```shell
    $ git bdog master
    ```
