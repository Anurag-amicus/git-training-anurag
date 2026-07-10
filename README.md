# git-training-anurag


Name - Anurag Chandra

Training Batch - AFDP Batch 2026 Path-2

Date - 9-July-26

Project - A Simple Portfolio Website using HTML, CSS, Javascript.


# What happens if you forget a .gitignore on first commit?

    The unnecessary files that should be ignored might get pushed into remote like node 
    modules or other dependencies 

# How to fix it retroactively?

    We have to untrack those files that have been unnecessarily committed and to do that :-
     1. save the current changes - git commit -am "msg"
     2. clear the git index - git rm -r --cached
     3. Now stage the files - git add .
    After doing these the files in gitignore will never be tracked

# During merging of feature/add-navigation branch to main

    It was not a fast forward merge but,
    The merge was a 3-way merge because we have new commits in feature branch and 
    also we have a new commit in main branch so thats why it was a 3-way merge 
    not a fast forward merge

# When should you rebase vs merge?

    When you want to update your local feature branch with new changes 
    from main branch to maintain a clean base for your branch ---- use rebase
    When you want to integrate a completed feature branch
    into stable main branch ---- use merge

# What's the golden rule of rebasing?

    Never rebase branches that have already been pushed to remote shared repository.
    And you only rebase main onto your local feature branch
    not the other way around i.e. to let your feature branch updated
    with the latest commit from main.

# Why cherry pick instead of merging the whole branch ?

    Merging would pull the entire history even when the feature branch has
    incomplete work whereas cherrypick is helpfull when there are untested features
    in the branch and you want to pick one specific fix or feature that needs to be
    push into prod immediately

# When cherrypick is appropriate ?

    When you want to pull code into hotfix from abandoned or untested feature branch
    to fix the immediate bug.