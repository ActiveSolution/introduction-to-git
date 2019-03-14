# Finding lost commits

Sometimes you accidentally remove a commit and later realise that you should't have. Is that code lost forever now?  
No, as long as your code has been commited you can usually recover it.

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise10
    ```

2. Make some changes and `commit` your changes. Repeat a few times to add several commits to your branch.  
    \-  

4. `checkout` the `master` branch.
    ```
    git checkout master
    ```

5. Delete your feature branch.
    ```
    git branch -D feature/exercise10
    ```

6. Verify that the branch and its commits are gone.
    Run `git log` to verify that the commits are gone. We can add some flags to make the log output nicer looking.
    ```
    git log --oneline --graph --decorate 
    ```

7. Use `reflog` to find the commit hash of the commit you want to recover.
    ```
    git reflog
    ```

8. Recover the lost commit using `cherry-pick` or simply by using `checkout` and the commit hash you found in the `reflog`.
    ```
    git cherry-pick 0d89a4e
    ```
    or
    ```
    git checkout 0d89a4e
    ```
    But be careful when you checkout a commit directly, you will end up with a [detached HEAD](https://www.git-tower.com/learn/git/faq/detached-head-when-checkout-commit).