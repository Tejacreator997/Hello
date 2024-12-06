
Create Docker image from Dockerfile
-----------------------------------
 
1. login to docker client machine.
 
2. Open ubuntu virtual machine terminal.
 
3. Login to adminstrator mode 

	>sudo su 

	Install docker in ubuntu virtual machine

	>apt install docker.io

	Check docker is installed or not 

	>docker --version

	or

	>docker version
 
4. Check present working directory 

	>pwd
 
5. Check any files or directory is available in the present working directory

	>ls

	or

	>ll
 
6. 	Create a new directory is "Image1"

	>mkdir Image1

7. Change the directory path to Image1

	>cd Image1

8. Create Dockerfile 

	>vim Dockerfile

9. Write the Dockerfile 

	- press "i" key enter into "INSERT" mode 

	- Enter first line is

	FROM tomcat:7

	- Press escape "esc" and save and quit

	:wq!

10. Create image from Dockerfile
 
	>docker build . --tag Image1:1

11. Add MAINTAINER information in Dockerfile and create image
 
	>vim Dockerfile

	- press "i" key enter into "INSERT" mode 

	- Enter second line is

	MAINTAINER Rajesh

	- Press escape "esc" and save and quit

	:wq!

	Create image from Dockerfile
 
	>docker build . -t image1:latest


12. Add LABEL information in Dockerfile and create image
 
	>vim Dockerfile

	- press "i" key enter into "INSERT" mode 

	- Enter 3rd line is

	LABEL "Support_Team"="DevOps Team"

	- Press escape "esc" and save and quit

	:wq!

	Create image from Dockerfile
 
	>docker build . -t image1:1

13. ADD syntax for adding file in Tomcat with Dockerfile and create image
 
	>vim Dockerfile

	- press "i" key enter into "INSERT" mode 

	- Enter 4th line is

	ADD h1 /usr/local/tomcat

	- Press escape "esc" and save and quit

	:wq!

	Create image from Dockerfile
 
	>docker build . -t image1:2

14. ADD syntax for adding tar file in Tomcat with Dockerfile and create image
 
	>vim Dockerfile

	- press "i" key enter into "INSERT" mode 

	- Enter 4th line is

	ADD  /usr/local/tomcat

	- Press escape "esc" and save and quit

	:wq!

	Create image from Dockerfile
 
	>docker build . -t image1:3


	Note: Download any tar zip file from internet 

	ex: 

	wget https://getsamplefiles.com/download/tar/sample-3.tar