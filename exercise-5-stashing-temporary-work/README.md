# Stashing temporary work

Some times you might be working on a new feature when suddenly something else demands your attention, e.g. a bug fix in production.

1. Create a new feature `branch`.

2. Make some unfinished changes to the code. Maybe the code does not even compile at this point.

Now when something else requires your attention you have 2 options. `commit` your changes or `stash` them.
  - If you're working on a local feature branch there is usually no issue with commiting your changes
  - If, for some reason, you do not want to commmit your changes, but also you do not want to loose them you can instead save your temporary work by stashing it.

3. `stash` your temporary work. The `stash` command is not available without extensions in Visual Studio 2017.

4. `checkout` the `master` branch and make a "hotfix" and `commit` and `push` your changes.

5. `checkout` your feature branch.

6. `pop` the changes

7. Continue working on your changed code.