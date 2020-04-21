## References

references are pointer to commits

Types of references
    -> Tags & Annotated Tags
            ==> Tags
                -> simple pointer to commit
                -> if you create tag with no argument, it will point to commit where HEAD is currently pointing
                -> Command to create tag "git tag <tag_name>
            ==> Annotated tag
                -> point to commit with some additinal information like author message date
                -> command to create annotated tag "git tag -a <tag_name> -m "message to tag"
            
            --> git tag ==> list all the tags in a repo
            --> git show-ref --tags ==> list all tags and what commit they are poiniting to
            --> git tag --points-at <sha1>==> list of all tags pointing at commit
    -> branches
            ==> pointer changes as new commits are made.
            ==> branch and master will point to same commit if newly branch created
    -> HEAD
            ==> git will know what branch you're currently on and also used as parent of next commit
            ==> it can also point to commit(detached HEAD)
            ==> points to name of the branch

## Differneces between branch and tag pointer
    -> branch pointer moves with every commit
    -> tag pointer is static(doesn't change)

## HEAD_LESS/ DETACHED HEAD
    -> detached state show when you checkout a specific commit rather than branch or tag.
    -> git move HEAD pointer to this commit
    -> if made any commit in DETACHED head then there is no referencing point to these commit
            ==> if no new branch create with last commit then these commit will collected into garbage collected. 
                these commit are callled dangling commit(ref log), Git does periodic garbage collection and will
                eventuall delete any commits that don't have any references pointing to them.

    To save the work in DETACHED state
    -> By createing new branch pointing to the last commit you made in detached state
            ==> git checkout -b <new branch_name> < last commit>
            why last commit-> because last commit know all its parent
