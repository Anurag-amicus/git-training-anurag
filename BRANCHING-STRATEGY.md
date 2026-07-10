# Branching Strategy & Workflow Documentation
 
## Chosen Strategy: Trunk-Based Development (TBD)
For this project , I have used "Trunk-Based Development" strategy to utilize short lived feature branches or topics.
 
### Why Trunk-Based Development?
* Main is frequently updated which lets other feature branch be updated to latest iteration of project.
* Faster integration of feature as branch is created only for single purpose.
 
---
 
## Trunk-Based Development Branch Diagram
 
                  [ feature/add-navigation ] ------> (Merged)
                 /                                  \
[ main / trunk ] ---------------------------------------------------------------------> (Continuous)
                | \          \                      /            /               /
                |  \          [ feature/add-footer ] ---------------[ hotfix/* (Cherry-pick)]
                |   \                                         /
                |    [ feature/add-sidebar ] -> (Rebased) ---/
                |
                \-----[ testing/stash ]
                |
                \-----[ testing/reset ]


# When to branch and from where?

  For short lived feature branches -- Directly from main

  For Bugs Hotfix -- Directly from main and cherry-pick to that bug originating branch

# Branch Naming conventions.

  I have used standard branch naming convention like

  for feature-- "feature/x-y-z"
    OR
  for Hotfix-- "hotfix/x-y-z"

# When to use merge vs rebase ?

  Merge - When you want to integrate a completed feature branch of fixed hotfix branch

  Rebase -  When you want to update your feature branch with the latest commits in main then only 
            you rebase