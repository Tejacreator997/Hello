Create Docker image from
-------------------------
1.login to docker cilent machine

2.open ubuntu virtual machine terminal.

3.Login to adminstrator mode
   >sudo  sudo
   
   Install docker in ubuntu virtual machine
   >apt install docker.io
   
   Check docker installed or not
   >docker --version
   
4.Check present working directory 
   >pwd
   
5.check any files or directory is available  in the working directory
   >ls
   or
   >ll
   
6.Create a new directory
  >mkdir Image1

7.Change the directory path to Image1
  >Cd Image1
  
8.Create  Dockerfile
   >vim Dockerfile

9.Write the Dockerfile
  -press " i" Key enter into "INSERT" mode
  -Enter first line is
  -FROM tomcat:7
  -Press escape "esc" and save and quit
  :wq!
  
10.Create image from Dockerfile

  >docker build . --tag image1  
  
11.Add MAINTAINER information in Dockerfile and create image

   >vim Dockerfile
  -press " i" Key enter into "INSERT" mode
  -Enter Second line is
  MAINTAINER Ravindra
  -Press escape "esc" and save and quit
  :wq!
  
 Create image from Dockerfile
 >docker build .-tag Image1:latest

12.Add LABEL information in Dockerfile and  create image
  >vim Dockerfile
  -press " i" Key enter into "INSERT" mode
  -Enter 3rd  line is
  LABEL "Support_Team" = "DevOps Team"
  -Press escape "esc" and save and quit
  :wq!

  Create image f1rom Dockerfile
   >docker build . -t image:1:1
   
13.Add syntax for adding tar file Dockerfile and  create image
  >vim Dockerfile
  -press " i" Key enter into "INSERT" mode
  -Enter 4th  line is
  ADD h1 /usr/local/tomcat
  -Press escape "esc" and save and quit
  :wq!
  
  
  Create image f1rom Dockerfile
   >docker build . -t image:1:2
   
   
   Note :Download ant tar zip file from internet 
    
    ex: 
	wget https://getsamplefiles.com/download/tar/sample-3.tar