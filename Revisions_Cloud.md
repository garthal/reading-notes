# Git

![Workflow](https://krishnaiitd.github.io/gitcommands/images/GitWorkflow-3.png)

## Configurtation

1. git config --global
    * user.name 'example'
    - user.email 'example'

2. git config --list 


## Importing 

1. git init
2. git add
3. git add LICENSE
4. git cimmit -m "any message here"

## Cloning 

1. git clone \<URL> ./Location

## Workflow

1. git status
    * On branch master
2. git add *filename*
    * single file
3. git add *
    * all files

## Committing All Changes

1. git commit -a
    * Commits a snapshot of all modifications to tracked files in the working directory.

## Pushing Changes

1. git push origin master
    * Pushes changes from local master branch to the remote respository name orgin.

## Stashing changes

1. git stash 
    * Temporarily removes changes and hides them.
2. git stash apply
    * Retrieves hidden changes

## Remote Repos

1. git remote 
    * Provides short names
2. git remote -v
    * view remote urls to their short name

## Adding remotes 

1. git remote add shortname url

## Fetching 
> Fetching entails pulling dta thet you dont have from the remote project.

1. git fetch *remote-name* 
2. git fetch orgin
    * Used for cloned repositories

## Pushing 
> To push changes upstream for sharing you would use the following *push* command.

1. git push *remote-name* *Branch-name*

## Renaiming Removing Remotes 
> To rename a remotes short name use the *remote rename* command

1. git remote rename *old* *new*
    * renames 
2. git remote rm *new*
    * removes remote

## Commit Mistakes 
> You can use the amend command when you need to alter a commit message or forgot to add some files.

1. git commit --amend

## Unstaging a File

1. git reset Head index.html

## Undo a Committed Snapshot
> To undo changes resulting from a particular commit, use the git revert command. This command appends a new commit that undoes changes introduced by a specific commit.

1. git commit -m "example"
2. git revert HEAD

## Unmodifying a File 
> To have a file return to its state when you last committed.

1. git checkout -- *filename* 

## Creating a new Branch 

1. git branch *test*
    * Creates a new branch named test that points toward your most recent commit.

## Switching Branches 
>Switching to another branch use the git checkout command, it moves the HEAD pointer to the new branch.

1. git checkout *test*

## Creating a Branch at Checkout.
> It is possible to create a new branch at time of checkout.

1. git checkout -b *test*

## List Branches
> Lists available branches

1. git branch

## Fast-Forward Merging 
> Fast forward merging takes your current branches pointer and moves it forward to the most recent commit for the branch being merged in - there is no divergent work to merge together because the latter branch is directly upstream in relation to the former one.

1. git checkout master
2. git merge *test*
    * after this it would point to a new commit 2 to 3 

## No Fast-Forward
> Used to protect historical data and instead of moving the pointer forward, a new commit object is created.

1. git merge test --no-ff

## Three-way Merge 
> In cases of branches diverging, fast-forward merges are not an option. A three-way merge can be used however. This type of merge involves the two latest commit snapshots pointed to by both branches, and their common ancestor. 

1. git checkout *master*
2. git merge *test*

## Fetch and Merge 
> *git pull* can easily fetch and merge remote changes to your remote directory.

## Deleting Branches 
> After branches are merged they are no longer needed they can be easily deleted with *-d* 

1. git branch -d *test* 

## Merge Conflicts
> When two files being merged that both have changes in identical sections of a file Git will not be able to complete the merge cleanly. 
>> These issues must be dealt with manually.

## Preview Changes 
> To preview changes for merging use the *diff* command.

1. git diff *Source* *Target* 

## See Latest Commits 
> Used to view the newest commits for each branch.

1. git branch -v
2. git branch --merged 
3. git branch --no-merged

## Rebasing 
> An alternative to merging.

## The Basics 
> Rebasing starts with a common ancestor of two branches: the one you're on and the one you're rebasing onto. Then the diffs resulting from each commit of your current branch are saved to temporary files, and the current branch gets reset to the same commit as that of the branch you are rebasing onto. Last but not least, all changes get applied to the branch you are rebasing onto.
>> The process essentially rewrites a projects history by replaying all changes committed on one branch to another one leading to cleaner application of commits on a remote branch and a linear history.

1. git checkout test 
2. git rebase master


## Rebase vs. Merge

*Pro-merge argument*
* The true commit history of a repository should not be altered because it's a record of occurrences.

*Pro-rebase argument*
* Commit histories should be polished and well edited.

## Log 
> *git log* can be used to view snapshots. You can use the command to see a projects history, use a filter, and find specific modifications. 

1. git log
2. git log -n 3
3. git log --stat
4. git log -p
5. git log --grep="updated"
6. git log --author="Smith"
7. git log index.html
8. git log --online

# Q&A

1. What is Version Control?

> Version control allows software dev teams the ability to breakdown a large progect so devs can work on them simaltaniously. This concept allows the team to track changes and then merge them all together to create the final project. Version control allows for point in time snapshots allowing teams to rollback changes if necessary or individuals to try new ideas and features without impacting the source code.

2. What is cloning in Git?

> Cloning a repository allows a user to create a local copy of an entire repository.

`git clone *URL*`

3. What is the command to track and stage files?

`git add`

4. What is the command to take a snapshot of your changed files?

`git commit` 

5. What is the command to send your changed files to Github?

`git push`%   
