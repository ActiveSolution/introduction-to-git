# Handling conflicts

1. Create a new feature `branch`.

2. Make some changes to the code. This time, make some changes to the contents of an existing paragraph.

3. `commit` your changes.

4. `checkout` the `master` branch.

5. "Simulate" that someone else has made conflicting changes and pushed them to the `master` branch while we were working on our new feature.
    - Make new changes to the same paragraph that you changed in 2. 
    - Commit them in the `master` branch.

6. `merge` your new branch into `master`.

7. Oh no! Conflicts. Let's resolve them.

8. `commit` your resolved changes.

9. `push` your changes.

10. Go to your Azure DevOps repository and verify that your changes have been pushed to the `master` branch.
