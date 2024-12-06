#use official ubuntu image version 20.04
FROM ubuntu:20.04

#update the package
RUN apt-get update

#Install nginx
RUN apt-get install -y nginx

#clear the directory space
RUN apt-get clean

#copy the webiste content in container
COPY  . /var/www/html/

#Expose the port number
EXPOSE 80
EXPOSE 443

#Start the nginx container
CMD ["nginx" ,"-g","daemon off;"]
