## merging and fast forward

Merge commits are commits that have more than one parent.
--> merge commit is pointer to new feature that was merged

## Fast forwading
--> fast forward happen when there is no commit on the base branch and new feature added and move the master pointer to new commit, in this case 
no need of merge commit
--> git merge -no-ff ==> will force merge commit, to avoid problems that occur with fast forward.

## merge confict
--> it occur when multiple people are making changes to a branch
    
    ==> git rerere (reuse recorded resolution)
    
        --> it save how you resolve conflict
        --> next merge conflict use the same resolution
        --> useful in rebasing
        How use rerere
            -> git config rerere.enabled true ==> for current project
            -> --global flag for all projects

# testing merge command
--> for testing purpose