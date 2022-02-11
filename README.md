#learninggit
1. git config --global user.name <prefer username of github>
2. git config --global user.email <prefer email associated to your github account>
3. git config -l/--list
4. git config --global --list/-l
5. git clone <github public repo url> #public repo do not need authentication, else you need to learn about authentocation mechanism
6. git satus
7. git add <filename> #to add a specific file in staging area
8. git add . #to add all the untracked files to staging area recursively(Recursive means -> all files in working directory also the files inside directory of working directory)

8.1. git add -A  #when ever we are moving a file from one location to other this will help in getting file into staged area by updating the status as renamed, refer screenshot 8.1 below

8.2. git add -u  #when ever we are renaming a file from filesystem this will help in getting file into staged area by updating the status as renamed, refer screenshot 8.1 below

9. git commit -m "your commit message"

9.1. git commit -am "your commit message"  #-am used togather when we are editing already existing file to get the content added to staging area and commit togather

10. git init #is a command initialize a raw git repository in with blank directory or directory may contains data already

10.1. git init <foldername>

10.2.  git init #already inside a directory having some data 

11. git ls-files   #this will tell you about all the tracked files. the moment we do "git add" for a file it becomes trackable by git in repo.
12. git reset HEAD <filename>  #this command will help to move the file back to working directory from staging area
13. git checkout -- <filename>  #this will completely revert the change whatever we have edit or any file added.
14. git mv <oldfilename> <newfilename>   #this is used to rename the file in such a way that it get directly into staging area.
15. git log

15.1. git log --abbrev-commit   #this shortens the SHA identifier version

15.2. git log --oneline --graph --decorate

15.3. git log -- <filename>  #this will provide history for the specific file

16. git diff

16.1. git diff #to show diff between working dir and last commit in repo on localhost/where repo is cloned, but this will show all current differences, which will be difficult to analyze all the changes made

16.2. git diff -- <filename>/<path>  #this can help in limiting the diff to a particular path or a set of files

16.3. git diff --staged  HEAD <filename> #this is to get diff between content in staged area and last commit, HEAD can be any commit ID/HEAD/origin/master

16.4. git diff <any commit id 1> <any commit id 2>  #this will help in analyzing diff between any last two commits in git

16.5. git diff HEAD HEAD^ #this helps in showing diff between latest commit(HEAD) and latest but one(HEAD -1)

16.6. git diff HEAD origin/master OR  git diff master origin/master  #this will help in analyzing difference between local repo changes and remote repo,where master/HEAD commit is latest commit in local repo and origin/master is state of remote repo > refer screenshot 16.6 below

17. git branch  #this will show the branches on local

17.1. git branch -a #this will show th branches on local as well as remote

17.2. git branch <somebranchname> #it will create a branch with the passed name and if branch is existing it will say "fatal: A branch named '<somebranchname>' already exists."

18. git checkout #to checkout the code for that branch

18.1. git checkout -b <branchname> #this command will help in switching to branch after getting created, if branch does not exists.

19. git merge #this command helps in merging from a branch to other

19.1. git merge <destination branch> <source branch> #to merge first switch to the branch where we want to merge, means destination branch, this by default perform the fast forward merge

19.2. git merge <destination branch> <source branch> --no-ff  #merging with --no-ff option disables the fastforward merge and display all the commits done in branch and complete tree in git decorated log

19.3. testing auto merge

19.3.1. chnage in master

19.3.2 change in branch learnbranchingmerging 

19.3.3 chnages in branch1

20. git rebase #this helps to display  and manage all the commits to anyother branch or ideally in master branch

20.1. git rebase <branchname>  #if we want to get branch commits to master, switch to master branch and do "git rebase <branchname>"

20.2 git pull --rebase origin master

21. git fetch #this will pull the chnages from remote repo in staging area and not merge in working dir, to merge that you a type of rebasing as in section 20.2

22. git statsh #this helps to save your current work as a refrence commit and set/keep you at origin/master can clean working dir.
