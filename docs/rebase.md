# Rebase

![rebase](https://wac-cdn.atlassian.com/dam/jcr:4e576671-1b7f-43db-afb5-cf8db8df8e4a/01%20What%20is%20git%20rebase.svg?cdnVersion=963)

_source <https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase>_

!!! quote "quote from _<https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase>_"

    Rebasing is the process of moving or combining a sequence of commits to a new base commit.

!!! quote "quote from _<https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase>_"

    From a content perspective, rebasing is changing the base of your branch from one commit to another making it appear as if you'd created your branch from a different commit. 
    Internally, Git accomplishes this by creating new commits and applying them to the specified base. 
    It's very important to understand that even though the branch looks the same, it's composed of entirely new commits.

!!! quote "quote from _<https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase>_"

    You want to get the latest updates to the main branch in your feature branch, but you want to keep your branch's history clean so it appears as if you've been working off the latest main branch.

!!! tip
    
    ```shell
    $ git fetch –all
    $ git rebase origin/master
    ```
