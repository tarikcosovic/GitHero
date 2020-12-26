git status : Shows the git status of tracked/modified/etc.. files
git init . : Initializes an empty git repo to the current directory

git add : Adds a new or modified file to the stagging area (tracks the file)
git add filename : Adds a specific file
git add . : Wildcard for adding all files

git commit : Commits changes and new files from the stagging area to the local git repo,
			 will also open default editor for message entry
git commit -m "Enter Message" : Allows adding the commit message or description
git commit -add : Adds a modified file to the stagging area and automatically commits it

*Git Remote Repository

git remote add origin url : Adds remote repository with specified name(origin) and url to repo
-git remote -v : Lists all remote repositories

git push -u origin master --tags : Pushes to origin repo from master branch, --tags sends all the tags we have to remote repo

*Git SSH 
ssh-keygen -t rsa -C "tarikcosovic@gmail.com" : Generates a private ssh key in current directory 

git rm file.format - removes the file immediately from the directory, 
					but is still in stagging (confirm via commit)
					
rm : remove a file
rm filename : specify a file to be removed
rm -f : forcefully remove a file

git mv example.txt newname.txt - renames the file and tracks it

git reset HEAD filename.format : Removes the stagged file from the stagging area
git checkout -- filename.format : Resets the modified file to the last commited copy

git log : Shows the commit logs
git log --oneline : Simplified commit log
git log --oneline --graph --decorate --all : Google these extra commands
git show : Shows the last commit and the diff with all the changes
git ls-files : Lists all the files git is tracking

git diff commitId HEAD : Previews the difference between that commit and the current master
git difftool commitId HEAD : Previews th differences in a visual tool like p4merge..
git diff / git difftool : After making a change to preview untracked/unstaged changes
git diff branch1 branch2 : Previews the differences between two branches

git branch : Previews the branches and highlights the current branch
git branch name : Creates a branch with specified name
git checout branchName : Switches to the specified branch
git checkout -b branchName : Creates a branch with specified name and automatically switches to it
git branch -d branchName : Deletes a branch with the specified name

git merge branchName : Merges the specified branch to the current branch

git tag myTag : Creates a tag with specified name
git tag --list : Lists all tags
git tag -d myTag : Delets the specified tag

git tag -a name -m "Message" : Creates an annotated tag with specified name and commit message
git show tagName : Displays the tag info

*Git Stash
Git stash is used to temporarily hide the untracked/unstaged files on a seperate 'stash' so that you can work on
other files without having to worry about stagging or commiting the previous files

git stash : Temporarily Hides untracked/unstaged files
git stash list : Lists all stashes

git stash pop : Removes all stashed files from the stash

*Git Reset
Resets the commits to specified commitId

git reset commitId --mode

modes: soft, mixed, hard

1. soft mode is the least destructive mode and will only point the HEAD to the specified commitId, making zero changes to stagged/unstagged files
2. mixed mode will point the HEAD to the specified commitId and unstagge all stagged files
3. hard mode will point the HEAD to the specified commitId and remove all unstagged and stagged files

Examples:
git reset 2dc131b --soft : non-destructive reset
git reset e37117a --mixed : mixed reset
git reset 7301ec8 --hard : destructive reset 

For special preview of all the commit and actions taken history use reflog

Example:
git reflog

*Special Markers:
HEAD - points to the last commit of current branch

*Making aliases:
git config --global alis.YourAliasNAme "commands you want to mapp"
Example:
git config --global alias.hist "log --oneline --graph --decorate --all"
This example will make an alias which we can use as ' git hist ' and would run the specified alias code

*Common and usefull Git Bash commands

> file.format : Create a new file from git bash
touch file.format : Create a new file with specified format
cat file.format : Prints the file content
start filename : Opens the specified file with its' default editor
ls -al : Lists all the files in the current directory even hidden formats
