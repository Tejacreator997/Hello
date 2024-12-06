
# Use official base image of ubuntu OS

FROM ubuntu:20.04
 
#Update the ubuntu OS

RUN apt-get update
 
#install jdk11

RUN apt-get install -y default-jdk
 
#Install wget 

RUN apt-get install wget -y
 
#Set environment variables

ENV JAVA_HOME /usr/lib/jvm/jdk-11

ENV CATALINA_HOME /opt/tomcat
 
#Download tomcat software in ubuntu OS 

RUN wget https://dlcdn.apache.org/tomcat/tomcat-11/v11.0.0-M17/bin/apache-tomcat-11.0.0-M17.tar.gz
 
#un tar the tar.gz file

RUN tar -zxvf apache-tomcat-11.0.0-M17.tar.gz
 
#Delete the tar.gz file from /usr/local/tomcat

RUN rm -rf apache-tomcat-11.0.0-M17.tar.gz
 
#Create tomcat directory in /opt/tomcat

RUN mkdir /opt/tomcat

