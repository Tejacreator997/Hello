
#docker inspect volume testvol1
 
User the volume to specific container ?

#docker run -it --name=srv01 --mount source=testvol1,destination=/data centos
 
Check the Container data with below command?

#ls
 
You will get data directory
 
Then navigate to data directory?

#cd data
 
Create inside one test file.txt?

#touch testfile.txt
 
update some info in testfile.txt?

#echo "Hello DevOps" >> testfile.txt
 
Check the data is updated or not?

#cat testfile.txt
 
Exit from the container?

#exit
 
Check list the dicker containers?

#docker ps -a
 
Find the mountpoint location ?

#docker volume ls
 
Note down "mountpoint" location path
 
Mount the mountpoint location path

#cd /var/lib/docker/volumes/testvol1/_data
 
Now check your testfile in the mountpoint path?

#ls
 
testfile.txt
 
Now remove the container?

#docker ps -a
 
#docker rm srv01
 
Now check volume is removed or not?

#docker volume ls 

testvol1
 
Note: testvol1 is not deleted even after remove the container
 
Check the data is available in testfile?

#cat testfile.txt
 
exit from mountpoint location? /var/lib/docker/volumes/testvol1/_data

#cd ..
 
Now create new container and mount to existing volume testvol1?

#docker run -it --name=srv02 --mount source=testvol1,destination=/data centos
 
Now we are in container2
 
Check list the files in container2?

#ls
 
Go to data folder?

#cd data
 
Check ls?

#ls
 
testfile.txt
 
Check the data in testfile

#cat testfile.txt
 
I can share the same volume to different container3?

first exit from container2

#exit
 
share the volume container3?

#docker run -it --volumes-from srv02 --name srv03 centos /bin/bash
 
 
How to remove volume?

#docker volume rm <volume name>
