`git init` //initialises a new empty repo , .git a hidden folder// powers folder to be managed by git
`rm -rf .git`// to un-init the folder/ directory..
`git status`  can be on three statges as below, WORKING, STAGED, REPOSITORY area's.

UN-TRACKED -> new file has benn added that git git doesn't yet track..
`git add<file>  ` working to staging area

WORKING AREA -> Three can be a bunch of files that are not currently handled  by git. means the chnages which are done or to be done are not managed by git. A file in working area is consdered to be not in a staging area. when we do `git status` and we see bunch of `untracked files` then these are actually called in working area..

STAGING AREA -> what all files are going to be part of the next version that we will create. This staging area is the place where git knows what changes will be done from the last version to the next version.. `git add "filename"`.. to move to satging are

REPOSITORY ->Actually contains the details of all your previous registered version. And the files in this area, git already manages them and know their version history 

commit -> commit is a particular version of the project. It captures a snapshot o fthe project's staged changes and creates version out of it.
1commit =1 version 

`git commit -m "message"` add file to repo area from staging area..

After making  a commit it opens vim editor if we don't commit with msg..

`git log` list down all commits of repository. for exit 'q'.

In Git, after a file is being tracked (e.g., after you use git add), subsequent changes to that file are not automatically moved to the staging area. You need to explicitly stage the changes again by running git add after modifying the file.

`git restore <file>` To discard changes in working directory, it removes all file(un-committed) changes. To delete the dirty peice of code // to move back the clean version of code.. 
 
`git restore --staged` it removes file from  staging area and brings to working area. only works if changes are in your staging area.

--->After using `git restore --staged` & `git restore <file>` the file gets to state it had in the last commit.

`git rm --cached "filename"`--->  If you want Git to stop tracking a file but not delete it:

`git diff`  show's the diff b/w commits, can be used with commit id and without also..

 `git remote` -> list down all the remote connection names

Remote connection -> It helps you to link two git repositories for uploading and downloading changes from each otherwise.

`git remote add <name of remote> <link of the remote> `: this command helps us to add a new link to the remote repo and give a name to it

`git remote rm <name of remote> `: this command deletes a remote connection

`git remote rename <olanme> <newname> `: this command remanes the remote connection

Note: The name of the remote connection is always used to establish communication between the reposetries.
