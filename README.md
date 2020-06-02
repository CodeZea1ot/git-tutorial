# Git/Github Tutorial by Code_Zealot

This repository is meant to be a resource that will help you learn how to use git/github from the command line.


##Global Configuration
**These commands are used to configure your global git environment. This information will be used in your commits.**
`$ git config --global user.name "John Smith"`
`$ git config --global user.email "some@email.com"`



## Quick Reference
**Here are some commonly used git commands and a brief description of what they do**

`$ git status`
| Returns information pertaining to the state of your project and its contents

`$ git init`
| Creates a new local repository in the pwd

`$ git add <file_name_here.extension>`
| Adds a particular file to the Staging Area

`$ git add .`
| Adds all files and directories to the Staging Area

`$ git add -A`
| Adds all files and directories to the Staging Area, while also handling deleted, moved, or renamed files/directories, etc

`$ git clone https://github.com/some_repo_url_here`
| Clones an existing Github repository to the pwd (Note: This creates a local repository within a subdirectory that is given the name of the cloned repository)

`$ git commit -m "<Commit message here>"`
| Adds all files/directories that are currently in the Staging Area to the local repository

`$ git remote add origin <https://github.com/some_repo_url_here>`
| Adds a remote repository that you can push to and pull from

`$ git remote -v`
Returns a list of remote repositories

`$ git pull`
| Pulls and merges files/directories from the lastest commit of the remote repository to your local repository

`$ git push origin master`
| Pushes your local repository to the remote repository

`$ git branch`
| Lists all available branches and returns which branch you are currently on

`$ git checkout -b <branch_name_here>`
| Creates a new branche and switches you from your current branch to the new branch in one command

`$ git checkout <branch_name_here>`
| Switches you from your current branch to the named branch

`$ git branch -d <branch_name_here>`
| Deletes the specified branch

