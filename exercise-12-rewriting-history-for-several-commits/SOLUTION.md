# Rewriting history - Add/modify multiple commits

*Disclaimer: Rewriting history is usually not a good thing to do if the history is public, i.e. if you have pushed it to a remote repository.*

*Disclaimer2: If you have commited any secrets (passwords, api-keys etc.) and pushed them to a public remote repository, you should consider them leaked. Rewriting history at that point will not guarantee that they have not been compromised.* 

You can make changes to several of your latest commits, e.g. you can roll back your `working directory` several commits without losing the changes you have commited.

1. Create a new feature `branch`.
    ```
    git checkout -b feature/exercise12
    ```

2. Make some changes to your code, for example add 3 files in 3 separate commits.  
    For example, create and add 3 files text1.txt, text2.txt, text3.txt.
    ```
    git add text1.txt
    git commit -m"Add first file"
    git add text2.txt
    git commit -m"Add second file"
    git add text3.txt
    git commit -m"Add third file"
    ```

At this point you may realise that there's something wrong with the file you commited first.

3. `reset` your `working directory` to the state of the first commit **without** losing your changes.
    ```
    git reset --soft HEAD~3
    ```

4. Make any corrections you like to the first file, then commit your changes again.
    After changing the file we can either commit all the changes at once:
    ```
    git add .
    git commit- m"Adding all files"
    ```
    Or if we still want separate commits for each file:
    ```
    git add text1.txt
    git commit -m"Add first file"
    git add text2.txt
    git commit -m"Add second file"
    git add text3.txt
    git commit -m"Add third file"
    ```