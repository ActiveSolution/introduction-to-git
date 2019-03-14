# Finding lost commits

Sometimes you accidentally remove a commit and later realise that you should't have. Is that code lost forever now?  
No, as long as your code has been commited you can usually recover it.

1. Create a new feature `branch`.

2. Make some changes and `commit` your changes. Repeat a few times to add several commits to your branch. 

4. `checkout` the `master` branch.

5. Delete your feature branch.

6. Verify that the branch and its commits are gone.

7. Use `reflog` to find the commit hash of the commit you want to recover.

8. Recover the lost commit using `cherry-pick` or simply by using `checkout` and the commit hash you found in the `reflog`.