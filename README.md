# git-training-anurag


Name - Anurag Chandra

Training Batch - AFDP Batch 2026 Path-2

Date - 9-July-26

Project - A Simple Portfolio Website using HTML, CSS, Javascript.


# What happens if you forget a .gitignore on first commit?

    The unnecessary files that should be ignored might get pushed into remote like node modules or other dependencies 

# How to fix it retroactively?

    We have to untrack those files that have been unnecessarily committed and to do that :-
     1. save the current changes - git commit -am "msg"
     2. clear the git index - git rm -r --cached
     3. Now stage the files - git add .
    After doing these the files in gitignore will never be tracked

# During merging of feature/add-navigation branch to main

    It was not a fast forward merge but,
    The merge was a 3-way merge because we have new commits in feature branch and also we have a new commit in main branch so thats why it was a 3-way merge not a fast forward merge