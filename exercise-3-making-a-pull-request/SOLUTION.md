# Making a pull request

## Using the command line

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise3
    ```

2. Make some changes to the code. For example, add another paragraph in `Program.cs`.  
    \-

3. `commit` your changes.
    ```
    git add --update
    git commit -m"Added a new paragraph"
    ```

4. Go to Azure DevOps and create a new `pull request` from your feature `branch`.
TODO

5. Approve the `pull request`, optionally delete the feature `branch` when prompted.
TODO

6. Go to your Azure DevOps repository and verify that your changes are now in the `master` branch.

7. Go to your local repository and `pull` the latest changes from the `master` branch.
    ```
    git checkout master
    git pull
    git branch -D feature/exercise3
    ```

## Using Visual Studio
TODO

1. Create a new feature `branch`.

2. Make some changes to the code. For example, add another paragraph in `Program.cs`.  
    \-

3. `commit` your changes.

4. Go to Azure DevOps and create a new `pull request` from your feature `branch`.

5. Approve the `pull request`, optionally delete the feature `branch` when prompted.

6. Go to your Azure DevOps repository and verify that your changes are now in the `master` branch.

7. Go to your local repository and `pull` the latest changes from the `master` branch.