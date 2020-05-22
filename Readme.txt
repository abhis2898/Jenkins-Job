#############	CREATING A REPO AND INITIALIZING #############

1) Create a directory in the system
2) Create a repository on Github without initializing it
3) Do the following on the git bash
	- git init
	- git remote add origin repo_url
	- git add file_name
	- git commit file_name -m "comment"
	- git push -u origin master

#############	CREATING A HOOK FOR GIT PUSH #############

1) follow the following steps
	- go to .git/hooks/
	- create a file post-commit
	- enter the command
		#!/bin/bash/
		git push
	- save
2) On commit the code pushes to the github