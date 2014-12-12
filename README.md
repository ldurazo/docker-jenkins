docker-jenkins
==============

1.- Install docker.

     wget -qO- https://get.docker.io/gpg | sudo apt-key add -
     
     sudo sh -c "echo deb http://get.docker.io/ubuntu docker main > /etc/apt/sources.list.d/docker.list"
     
     sudo apt-get update
     
     sudo apt-get install lxc-docker
     
     (Version should be 1.3 or up)

2.- Pull the image from dockerhub

     sudo docker pull ldurazo/jenkins

3.- Run the image, this will open the terminal as root user

     sudo docker run -i -t ldurazo/jenkins /bin/bash

4.- As root in container: 
     
     sudo service jenkins start


In another terminal...

5.- this will list all the runing containers, grab the id for next step

     sudo docker ps -a
     
6.- Get the ip address of the running container
     
     sudo docker inspect {container-id} | grep IPAddress

7.- with the IP obtained in docker open up port 8080 in your browser. (i.e. http://172.17.0.7:8080/)


NOTE:
Under construction, probably only localhosts will open this connection.
Most of commands that needs the container id will work with the first four characters.

please refer to the following docker hub repository: https://registry.hub.docker.com/u/ldurazo/jenkins/
