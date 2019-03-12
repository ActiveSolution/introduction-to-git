# Handling conflicts

## Using the command line

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise4
    ```

2. Make some changes to the code. This time, make some changes to the contents of an existing paragraph.  
    \-

3. `commit` your changes.
    ```
    git add --update
    git commit -m"Updated a paragraph"
    ```

4. `checkout` the `master` branch.
    ```
    git checkout master
    ```

5. "Simulate" that someone else has made conflicting changes and pushed them to the `master` branch while we were working on our new feature.
    - Make new changes to the same paragraph that you changed in 2.  
        \-
    - Commit them in the `master` branch.
        ```
        git add --update
        git commit -m"Someone else made changes"
        ```

6. `merge` your new branch into `master`.
    ```
    git merge feature/exercise4
    ```

7. Oh no! Conflicts. Let's resolve them.
    I recommend using a GUI tool to resolve conflicts, see some alternatives [here](https://git-scm.com/downloads/guis/)

8. `commit` your resolved changes.
    ```
    git commit -m"Fixed merge conflicts"
    ```

9. `push` your changes.
    ```
    git push
    ```

10. Go to your Azure DevOps repository and verify that your changes have been pushed to the `master` branch.  
    \-
