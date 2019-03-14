# Reverting local commits

Oh no, did you commit something you shouldn't have?  
As long as you haven't pushed your commits to a remote repository you can `reset` them locally.  
If you have already pushed your commits you need to instead `revert` them, see the next exercise.

1. Make some changes to the code.  
    \-  

2. `commit` your changes.
    ```
    git add .
    git commit -m"Changes"
    ```

4. Remove the commit by using the `reset` command. 
    - If you don't want to lose your changes, you just don't want them committed you can do a *soft* reset. This will keep the changes, staged in your working directory.
        ``` 
        git reset --soft HEAD^1
        ```
        Where `HEAD^1` means the *parent* commit. If you want to reset more commits you can increase the number. We will look more in depth on that feature in exercise-12.  
        Leaving out the `--soft` flag will still keep the changes, but they will no longer be staged.
    - If you do not want to keep the changes at all you can do a hard reset.
        ```
        git reset --hard HEAD^1
        ```
        This will remove the changes completely, although they will not be completely lost as we will see in exercise-10.
    

