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

Differneces between branch and tag pointer
    -> branch pointer moves with every commit
    -> tag pointer is static(doesn't change)