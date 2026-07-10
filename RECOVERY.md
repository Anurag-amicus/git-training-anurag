# CASE 1

  Using Revert

# Accidentally Deleted an important file

  ![Git Recovery](assets/Screenshot%202026-07-10%20121016.png)

# Recovering using revert command

  ![Git Recovery](assets/Screenshot%202026-07-10%20121726.png)

# CASE 2

  Using Reflog

# Before git reset hard

  
  This commit is essential and needs to be present
  ![Git Recovery](assets/Screenshot%202026-07-10%20124210.png)

# Accidentally used git reset hard

  Head is pushed back 1 commit so we have to use reflog and take hash for git reset hard

  ![Git recovery](assets/Screenshot%202026-07-10%20124634.png)

# When to use git revert vs reset

  git revert :: Used for public, shared branches and it creates a new commit
  for a revert that maintains a history but rollsback to previous changes.
  
  git reset :: Used for local branches that have not been pushed yet, 
  and you want to discard the changes altogether to the previous commit

  There is only one way to recover from hard reset i.e. using git reflog to
  extract recent deleted commit hash and once again reset to that hash

# Why is reset dangerous in shared branches

  using git reset --hard changes the history so if a collaborator that is working on same branch
  pulls from the remote that have a different git history it will clash with local git history.