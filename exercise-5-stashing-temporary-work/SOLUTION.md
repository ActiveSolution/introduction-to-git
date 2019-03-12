# Stashing temporary work

Some times you might be working on a new feature when suddenly something else demands your attention, e.g. a bug fix in production.

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise5
    ```

2. Make some unfinished changes to the code. Maybe the code does not even compile at this point.  
    \-

    Now when something else requires your attention you have 2 options. `commit` your changes or `stash` them.
  - If you're working on a local feature branch there is usually no issue with commiting your changes
  - If, for some reason, you do not want to commit your changes, but also you do not want to loose them you can instead save your temporary work by stashing it.

3. `stash` your temporary work.
    ```
    git stash --include-untracked -m"Working with exercise-5"
    ```
    `--include-untracked` is needed if you want to stash new files that have not yet been committed to the repository.  
    The `-m` message is optional when using `stash`.

4. `checkout` the `master` branch and make a "hotfix" and `commit` and `push` your changes.
    ```
    git checkout master
    ```
    *\*Modify some files to Make a bugfix\**
    ```
    git add .
    git commit -m"Bugfix"
    git push
    ```

5. `checkout` your feature branch.
    ```
    git checkout feature/exercise5
    ```
    To be up to date with master branch it is a good idea to `rebase` (or `merge`) the hotfix changes from master into your feature branch at this point.
    ```
    git rebase master
    ```

6. `pop` the changes  
    You can first view your stashed changes,
    ```
    git stash list
    ```
    and then `pop` them
    ```
    git stash pop
    ```
    At this stage there can be merge conflicts that need to be resolved if conflicting changes have been made in the working directory to files that were also in the stash.

7. Continue working on your changed code.  
    \-