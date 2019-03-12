# Making changes

## Using the command line

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise2
    ```

2. Make some changes to the code. For example, add a third paragraph in `Program.cs`.  
    \-

3. `commit` your changes.  
    There are several ways to `stage` your changes to the `index`.  
    1. Add all **modified** files to the index.
        ```
        git add --update
        ```
    2. Add all files, **modified** and **untracked** files.
        ```
        git add .
        ```
    3. Add files interactively using a menu with options.
        ```
        git add -i
        ```
    4. Add files selectively by `chunks`, selecting what chunk to commit and what to skip.
        ```
        git add -p
        ```


    Commit the files with a message.
    ```
    git commit -m"Added a paragraph"
    ```

4. `checkout` the `master` branch.
    ```
    git checkout master
    ```

5. `merge` your new branch into `master`.
    ```
    git merge feature/exercise2
    ```

6. `push` your changes.
    ```
    git push
    ```

7. Optionally delete your local feature `branch`.
    ```
    git branch -d feature/exercise2
    ```

8. Go to your Azure devops repository and verify that your changes have been pushed to the `master` branch.  
    \-


## Using Visual Studio
TODO

1. Create a new feature `branch`.

2. Make some changes to the code. For example, add a third paragraph in `Program.cs`.

3. `commit` your changes.

4. `checkout` the `master` branch.

5. `merge` your new branch into `master`.

6. `push` your changes.

7. Optionally delete your local feature `branch`.

8. Go to your Azure devops repository and verify that your changes have been pushed to the `master` branch.