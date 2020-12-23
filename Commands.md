git status : Shows the git status of tracked/modified/etc.. files
git init . : Initializes an empty git repo to the current directory

git add : Adds a new or modified file to the stagging area (tracks the file)
git add filename : Adds a specific file
git add . : Wildcard for adding all files

git commit : Commits changes and new files from the stagging area to the local git repo,
			 will also open default editor for message entry
git commit -m "Enter Message" : Allows adding the commit message or description
git commit -add : Adds a modified file to the stagging area and automatically commits it


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

Making aliases:
git config --global alis.YourAliasNAme "commands you want to mapp"
Example:
git config --global alias.hist "log --oneline --graph --decorate --all"
This example will make an alias which we can use as ' git hist ' and would run the specified alias code

Common and usefull Git Bash commands

> file.format : Create a new file from git bash
touch file.format : Create a new file with specified format
start filename : Opens the specified file with its' default editor
ls -al : Lists all the files in the current directory even hidden formats