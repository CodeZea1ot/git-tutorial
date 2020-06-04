# Git/Github Tutorial by Code_Zealot

This repository is meant to be a resource that will help you learn how to use git/github from the command line.

#### Warning: Git. Is Hard.

## Global Configuration
**These commands are used to configure your global git environment. This information will be used in your commits.**

| Command | Description |
|---------|-------------|
|    `$ git config --global user.name "John Smith"`    | Sets the author's name|
| `$ git config --global user.email "some@email.com"` | Sets the author's email |


## How to create a new project with git
1. Login to Github.com
2. Create a new remote repository on Github.com
3. Navigate to the directory you would like to clone your remote repository
	- `$ cd some/directory/path/here`
4. Clone the remote repository to the current working directory
5. Begin your workflow

## How to add an existing project to git
1. Login to Github.com
2. Create a new remote repository on Github.com
3. Copy the provided url for this remote repository
	- Will be needed in step 8
2. Navigate to the directory of your existing project
	- `$ cd some/directory/path/here`
5. Initialize git within the local project directory
	- `$ git init`
6. Add the files/directories to the Staging Area
	- `$ git add .`
7. Commit the files/directories in the Staging Area to the local repository created with `git init`
	- `$ git commit -m "<commit_message_here>"`
8. Add a remote repository to the project
	- `$ git remote add origin <https://github.com/remote_repo_url_here>`
9. Push the local repository to the remote repository
	- `$ git push origin master`

## Standard Workflow
It is best practice to follow this standard workflow when working with git/github, especially when collaborating with other developers. New features should always be developed within a new branch and then merged into master branch when production ready.
```
//Check the status of your project
$ git status

//Check to see if your local repository is up to date. If not, pulls the new files/directories from the remote repository.
$ git pull

//After you have made changes to your file(s), add them to the Staging Area so you can prepare to commit them to the local repository
$ git add example.txt

//When you are finished working on your task, send the files/directories in the Staging Area to the local repository. Be sure to provide a commit message that makes sense and is clear.
$ git commit -m "Changes to example.txt"

//Push your local changes to the remote repository
$ git push origin <branch>
```

## Branches and Merging
All new features should be developed within a singular branch. Once the feature is production ready, the branch that it was developed on should then be merged into the master branch.
```
//Create a new branch for your feature and switch to it
$ git checkout -b <my_new_branch_here>

//Follow standard workflow best practices until the branch is ready to be merged into the production master branch.

//When ready to merge, switch to the master branch
$ git checkout master

//Check to see if your local repository is up to date. If not, pulls the new files/directories from the remote repository.
$ git pull

//Merge the feature branch into the master branch
$ git merge <my_new_branch_here>

//Now that the branch is no longer needed, remove the branch
$ git branch -d <my_new_branch_here>

```

## Commmand Reference
**Here are some commonly used git commands and a brief description of what they do**

| Command | Description |
|---------|-------------|
|    `$ git status`     |   Returns information pertaining to the state of your project and its contents          |
|  `$ git init`       |     Creates a new local repository in the current working directory        |
|     `$ git add <file_name_here.extension>`    |     Adds a particular file to the Staging Area        |
| `$ git add .`| Adds all files and directories to the Staging Area|
| `$ git add -A`|Adds all files and directories to the Staging Area, while also handling deleted, moved, or renamed files/directories, etc |
|`$ git clone https://github.com/some_repo_url_here` | Clones an existing Github repository to the current working directory (Note: This creates a local repository within a subdirectory that is given the name of the cloned repository)|
|`$ git commit -m "<commit_message_here>"` | Adds all files/directories that are currently in the Staging Area to the local repository |
|`$ git remote add origin <https://github.com/some_repo_url_here>` |Adds a remote repository that you can push to and pull from |
| `$ git remote -v` |Returns a list of remote repositories |
|`$ git pull` | Fetches and merges files/directories from the lastest commit of the remote repository to your local repository|
|`$ git push origin master` |Pushes your local repository to the remote repository |
| `$ git branch`| Lists all available branches and returns which branch you are currently on|
|`$ git checkout -b <branch_name_here>` |Creates a new branche and switches you from your current branch to the new branch in one command |
| `$ git checkout <branch_name_here>`|Switches you from your current branch to the named branch |
|`$ git branch -d <branch_name_here>` |Deletes the specified branch |


## Other notes
**You can add a file called `.gitignore` to the root of your reposatory to make git ignore certain files/directorys. See [here](https://git-scm.com/docs/gitignore) for more info
