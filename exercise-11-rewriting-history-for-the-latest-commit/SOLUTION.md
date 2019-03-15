# Rewriting history - Add/modify your latest commit

*Disclaimer: Rewriting history is usually not a good thing to do if the history is public, i.e. if you have pushed it to a remote repository.*

*Disclaimer2: If you have commited any secrets (passwords, api-keys etc.) and pushed them to a public remote repository, you should consider them leaked. Rewriting history at that point will not guarantee that they have not been compromised.* 

It is possible to make modification to your last commit, e.g. make additional changes to a file, add/remove a file or change the commit message.

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise11
    ```

2. Make some changes to the code.  
    \-

3. `commit` your changes.
    ```
    git add . 
    git commit -m"Changes"
    ```

4. Make additional changes and `amend` them to your last commit and update the commit message.
    Make another change to your code, then amend them:
    ```
    git commit --amend -m"A new message"
    ```
    or if you want to keep the old commit message:
    ```
    git commit --amend --no-edit
    ```
