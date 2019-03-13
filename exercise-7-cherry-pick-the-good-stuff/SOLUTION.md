# `cherry-pick` the good stuff only.

Sometimes work on a feature branch may be cancelled and never merged into `master` but we may like to use parts of the code from the branch.

<img src="../images/cherry_pick1.png" height="200">
<img src="../images/cherry_pick2.png" height="200">

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise7
    ```

2. Make some changes and `commit` your changes. Repeat a few times to add several commits to your branch.  
    For example, add 3 files text1.txt, text2.txt, text3.txt.
    ```
    git add text1.txt
    git commit -m"Add first file"
    git add text2.txt
    git commit -m"Add second file"
    git add text3.txt
    git commit -m"Add third file"
    ```

4. `checkout` the `master` branch.

5. Select a commit from your feature branch and `cherry-pick` it to add it to the master branch.
    Run `git log` to view the commit hashes. Copy the commit hash for the commit you want to add from the feature branch, for example for "add first file". (You don't need to copy the full hash, you just need enough of it to uniquely identify it)
    ```
    git cherry-pick 494e36c
    ```

6. `push` your changes.
    ```
    git push
    ```

7. Optionally delete your local feature `branch`.
    If you try running `git branch -d feature/exercise6" you will get an error message this time, telling you that the branch is not fully merged. 
    To delete the branch anyway you need a capital D to "force" delete the branch. 
    ```
    git branch -D feature/exercise7
    ```

8. Go to your Azure devops repository and verify that your changes have been pushed to the `master` branch.  
    \-
