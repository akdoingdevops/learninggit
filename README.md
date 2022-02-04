#learninggit
1. git config --global user.name <prefer username of github>
2. git config --global user.email <prefer email associated to your github account>
3. git config -l/--list
4. git config --global --list/-l
5. git clone <github public repo url> #public repo do not need authentication, else you need to learn about authentocation mechanism
6. git satus
7. git add <filename> #to add a specific file in staging area
8. git add . #to add all the untracked files to staging area recursively(Recursive means -> all files in working directory also the files inside directory of working directory)

8.1. git add -A  #when ever we are moving a file from one location to other this will help in getting file into staged area by updating the status as renamed, refer screenshot 8.1

8.2. git add -u  #when ever we are renaming a file from filesystem this will help in getting file into staged area by updating the status as renamed, refer screenshot 8.1

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

16. git
17. git 
