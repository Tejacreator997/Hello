
Docker networking Commands:
 
1. List the Docker Networks
 
#docker network ls
 
2. Creating docker network.
 
#docker network create -d bridge MyBridgeNetwork
 
#docker network create -d host MyHostNetwork
 
#docker network create -d none MyNoneWork
 
3. Removing the docker network
 
#docker network rm MyBridgeNetwork
 
4. Getting Information about a network
 
#docker network inspect MyBridgeNetwork
 
5. Getting information about a Docker Container
 
#docker inspect <cotainer id>
 
6 How to connect container to specific network
 
#docker network connect <network name> <container id>
 
7.Disconnecting a container from a network
 
#docker network disconnect <network name> <container id>