# Reverting remote commits

Oh no, did you commit something you shouldn't have?  
What, you have already pushed it to a remote repository?  
Then you need to `revert` them.

*Disclaimer: If you have commited any secrets (passwords, api-keys etc.) and pushed them to a public remote repository, you should consider them leaked. Reverting the change will not remove them from the repository*

1. Make some changes to the code.  
    \-  

2. `commit` your changes.
    ```
    git add .
    git commit -m"Changes"
    ```

3. `push` your changes.
    ```
    git push
    ```

4. Create a new commit to reverse the changes of the last commit using the `revert` command.
    Run `git log` to view the commit hashes. Copy the commit hash for the commit you want to add from the feature branch, for example for "add first file". (You don't need to copy the full hash, you just need enough of it to uniquely identify it)
    ```
    git revert f393d1f
    ```
    You can revert any commit, not just the latest commit but in that case there may be conflicts that need to be resolved. After resolving you continue the revert by running
    ```
    git revert --continue
    ``` 
    If you end up in a conflicted state you can always abort the revert process by running
    ```
    git revert --abort
    ```

5. `push` your commit to revert the changes in the remote repository.
    ```
    git push
    ```

