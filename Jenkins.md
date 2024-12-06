
echo "jeknins job running for to know work directory"

pwd
 
echo " jenkins job is for to know which computer user is logged in"

whoami

echo "change directory rajesh"
cd rajesh
echo "download software package"
wget wget https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.17/bin/apache-tomcat-10.1.17.tar.gz
#!/bin/bash

mkdir rajireddy

cd ravi

wget https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.17/bin/apache-tomcat-10.1.17.tar.gz 

tar xvzf apache-tomcat-10.1.17.tar.gz

rm -rf apache-tomcat-10.1.17.tar.gz

mv apache-tomcat-10.1.17/ tomcat

sudo yum install java -y

java -version

ls -al

cd tomcat

cd bin

sh startup.sh