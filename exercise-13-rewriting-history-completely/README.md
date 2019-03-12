# Rewriting history completely

*Disclaimer: Rewriting history is usually not a good thing to do if the history is public, i.e. if you have pushed it to a remote repository.*

*Disclaimer2: If you have commited any secrets (passwords, api-keys etc.) and pushed them to a public remote repository, you should consider them leaked. Rewriting history at that point will not guarantee that they have not been compromised.* 

Using git's interactive `rebase` functionality you can essentially make any conceivable changes to your history, let's try it out.

1. Create a new feature `branch`.

2. Make some changes to your code, for example add 3 files in 3 separate commits.

At this point you may realise that file number 2 never should have been committed at all. And maybe the commits should really have been just 1 commit.

3. ´rebase´ your changes interactively to make the suggested changes.