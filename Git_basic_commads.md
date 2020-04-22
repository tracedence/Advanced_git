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



