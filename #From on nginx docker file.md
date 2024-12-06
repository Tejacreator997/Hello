#From on nginx docker file
FROM ubuntu:latest
RUN apt update
RUN apt-get install -y nginx
WORKDIR /etc/nginx
ENTRYPOINT ["/docker-entrypoint.sh"]
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

