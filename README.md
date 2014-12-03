docker-jenkins
==============

1.- Install docker.

2.- sudo docker pull ldurazo/jenkins

3.- sudo docker inspect {container-id} | grep IPAddress

4.- sudo docker run -i -t ldurazo/jenkins

5.- As root in container: sudo service jenkins start

6.- with the IP obtained in docker open up port 8080 in your browser.


NOTE:
Under construction, probably only localhosts will open this connection.
Most of commands that needs the container id will work with the first four characters.
