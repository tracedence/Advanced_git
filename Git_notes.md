Git stash
    -> Git stash way to save uncommited work.
    -> safe from destructive operations like switching between branches in the middle of work

    --> By default git only stashes changes only of those files which are already tracked

    Commands:
    --> git stash => save the uncommited work
    --> git stash list => show what stash 
    --> git stash show stash@{0} => show the content of this stash
    --> git stash apply => moved content from stash to staging
    --> git stash apply stash@{0} => moved only particular stash to staging
    --> Never perform git stash list and then git stash to any new file => it will delete that new file
                  if file already present then it will delete new added content.


    git stash Advanced Command
    --> git stash --include-untracked ==>keep untracked files
    --> git stash --all keep all files(even ignored ones )
    --> git stash save "name of stash" ==> name stashes for easy references
    
    # Advanced stashing for cleaning stash
    --> git stash pop ==> Remove the last stash and apply the changes(it will not remove the stash if there will be merge conflict)
    --> git stash drop ==> Remove the last stash
    --> git stash drop stash@{n} ==> remove the nth stash
    --> git stash clear ==> remove all stashes
