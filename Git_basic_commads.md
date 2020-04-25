## Basic git Commands

--> git show-ref ==> shows the commits for every branch or remote branch or tag, 
                    when we checkout these references HEAD will point to these commits

--> git cat-file -p <commit> ==> will show the content(value) in that commit

--> git checkout - ==> shortcut for checkout to previous branch

--> git log ==> show the history of repo

--> git log --since="yestarday" ==> will show all commits did from yestarday to now

--> git log --name-status --follow -- <filename> ==> if code is same and file is rename, it will show all history of that file

--> git log --grep <search string> ==> list all log which have passed string

^ or ^n
    --> ^{no_args} == ^1, the first parent commit from current commit (git reset --hard HEAD^)
    --> A^1 to first parent commit
    --> A^2 to second parent commit
    --> A^^1 to grandparent first commit

~ or ~n
    --> ~{no_args} == ~1, move to first parent commit from current commit
    --> A~1 to first parent commit
    --> A~2 to first grandparent commit

--> git show <commit> ==>  show commit and content you commited

--> git show <commit> --stat ==> show the file changed in commit

--> git diff ==> show content that will be part of next commit from working directory

--> git diff --staged ==> show content that will be part  of next commit from staged area

--> git diff A(branch) B(branch) ==> will show the content of branch B which is not present in branch A.



## Basic git Commands

--> git show-ref ==> shows the commits for every branch or remote branch or tag, 
                    when we checkout these references HEAD will point to these commits

--> git cat-file -p <commit> ==> will show the content(value) in that commit

--> git checkout - ==> shortcut for checkout to previous branch

--> git log ==> show the history of repo

--> git log --since="yestarday" ==> will show all commits did from yestarday to now

--> git log --name-status --follow -- <filename> ==> if code is same and file is rename, it will show all history of that file

--> git log --grep <search string> ==> list all log which have passed string

^ or ^n
    --> ^{no_args} == ^1, the first parent commit from current commit (git reset --hard HEAD^)
    --> A^1 to first parent commit
    --> A^2 to second parent commit
    --> A^^1 to grandparent first commit

~ or ~n
    --> ~{no_args} == ~1, move to first parent commit from current commit
    --> A~1 to first parent commit
    --> A~2 to first grandparent commit

--> git show <commit> ==>  show commit and content you commited

--> git show <commit> --stat ==> show the file changed in commit

--> git diff ==> show content that will be part of next commit from working directory

--> git diff --staged ==> show content that will be part  of next commit from staged area

--> git diff A(branch) B(branch) ==> will show the content of branch B which is not present in branch A.

## Fixing Mistakes
--> To fix any mistake you should have good understand of these areas:
        1. Woking area
        2. staging area :- it's a copy of current commit. It also called index.
        3. repository area

        How to move data between them

    ## Git Checkout
        * Restore working tree files or switch branches
        * it can also move the head pointer
        * it can also checkout file without moving the pointer

        ## what happen when we checkout branch
            * Head pointer change to new branch
            * copy the commit snapshot of that branch to staging area
            * update the content of working area with new branch content.
        
        * changes in the staging area are kept unless there is any conflict while checkout for another new branch.
    
    ## git checkout --file
        * replace the working area copy with current version of copy from staging area.
        * it overwrite the content of working area file.
        * once gone no way to get them back.

## git Clean
    to clean untracked files

    ## git clean --dry-run 
        * show files which files will be deleted

    ## git clean -d --dry-run
        * show files and directories which will be deleted
    
    ## git clean -d -f 
        * will delete files and directories

## Git Reset
    by default
    * git reset --mixed

    * git reset moves the HEAD Pointer

    ## git reset --soft HEAD~
        * moves HEAD to previous commit, that's it .

    ## git reset HEAD~ or Git reset --mixed HEAD~
        * moves the HEAD to previous commit and also copy the files of that commit to staging area.
        * This command is also called unstaged command

    ## git reset --hard HEAD~
        * moves the HEAD to previous commit
        * copy the files of this commit to staging and working area & delete the new changes you made completely. 

    ## git rest <file>
        * Doesn't move HEAD pointer but copy the file from repo to staging area.

    ## git reset <commit> --file
        * doesn't move HEAD pointer but copy the file from the that commit to staging area.

## Undo a git Reset with ORIG_HEAD
    * git keep the previous value of HEAD in variable called ORIG_HEAD
    ## git reset ORIG_HEAD
        * undo the reset

## git revert <commit>
    * do the mirror copy of given commit.
    * doesn't change history