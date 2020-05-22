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


#############	START JENKINS #############
1) from redhat
	- systemctl start jenkins
2) turn all the firewall off
	- systemctl stop firewalld
	- systemctl disable firewalld
	- setenforce 0

#############	JOB CREATION ON JENKINS #############

1) To build the trigger on commit
In the post-commit file add the command
	- curl --user "username:password" trigger_url

2) command to copy files & create docker

sudo cp * dir_name

if sudo docker ps | grep container_name
then
echo "already running"
else sudo docker run -dit -v dir_name:image_dir_name -p 8084:80 
fi