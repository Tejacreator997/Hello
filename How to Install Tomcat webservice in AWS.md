How to Install Tomcat webservice in AWS ?

1.Login  to server with admin access
$ Sudo su

2.Update the package repository  Before installing Tomcat
$ sudo yum update

3.Install java 
$sudo yum install java

4.Install java suceesfully or not 
$ java --version

5.Install Tomcat 
$ wget https://dlcdn.apache.org/tomcat/tomcat-11/v11.0.0-M18/bin/apache-tomcat-11.0.0-M18.tar.gz

6.File download or not check command
$ls

7.which location download file name 
$ pwd

8.unzip file name for Tomcat 
tar -zxvf apache-tomcat-11.0.0-M18.tar.gz

9.File download or not check command
$ ls

10.Remove the tar.gz file command
$ rm -rf apache-tomcat-11.0.0-M18.tar.gz

11.File download or not check command
$ls

12.which location download file name 
$ pwd

13.location change for Tomcat download in the web serve download
[ec2-user@ip-172-31-38-116 ~]$ cd ..
[ec2-user@ip-172-31-38-116 home]$ cd ..

14..File download or not check command
$ ls

15.Go to opt directory for Tomacat
$cd opt/

16.File download or not check command
$ ls
aws

17.Create Tomcat directory and simple said small method 
cd  /home/ec2-user/

18.File download or not check command
$ls

19.Make file opt directory for Tomcat 
$ sudo mkdir  /opt/tomcat

20.Move file opt from Tomacat directory
sudo mv apache-tomcat-11.0.0-M18/* /opt/tomcat

21.Go to opt directory for Tomacat
$cd /opt

22.File download or not check command
$ ls
aws  tomcat

23.go to Tomcat directory
$ cd tomcat/

24.File download or not check command
$ ls

BUILDING.txt     LICENSE  README.md      RUNNING.txt  conf  logs  webapps
CONTRIBUTING.md  NOTICE   RELEASE-NOTES  bin          lib   temp  work


25.Changes Permission for Tomcat 
[ec2-user@ip-172-31-38-116 tomcat]$ chmod 777 -R /opt/tomcat/
chmod: changing permissions of '/opt/tomcat/': Operation not permitted

[ec2-user@ip-172-31-38-116 tomcat]$ sudo chmod 777 -R /opt/tomcat/

26.Tomcat Web server Execute location
 $ cd bin/
 $ sudo su
# ls
 
27.Tomcat server start up 
[root@ip-172-31-38-116 bin]# sh startup.sh
Using CATALINA_BASE:   /opt/tomcat
Using CATALINA_HOME:   /opt/tomcat
Using CATALINA_TMPDIR: /opt/tomcat/temp
Using JRE_HOME:        /usr
Using CLASSPATH:       /opt/tomcat/bin/bootstrap.jar:/opt/tomcat/bin/tomcat-juli.jar
Using CATALINA_OPTS:
Tomcat started.

28.Enable Tomcat inbound rule in security group of instance in EC2
port :8080
Protocal :TCP 
source :Anywhere

29.Take Public Ip of instance and browse from any internet browse
verify :Apache Tomcat/11.0.0-M18








