# docker_home
Some basics

Check docker version

# docker version

=============================
=============================
Check how many containers are running, how many images we have got and more information

# docker info

=============================
=============================
Run  hello-world container

# docker run hello-world

To run a new container docker run
=============================
=============================
docker containers status

# docker ps  ->>  showing actually running containers 

# docker ps -a  ->> showing all containers

To see running and stopped containers docker ps --all
=============================
=============================
docker images information

# docker images

To see info about images docker images
=============================
=============================
Downloading ubuntu latest version docker images from from hub.docker.com

# docker pull ubuntu:latest

To do download images docker pull
=============================
=============================
WORKING WITH IMAGES
docker images 		-> list of downloaded images on docker host
docker pull foo 	-> download image (example docker pull ubuntu:14.04), copies images to the docker host
docker rmi foo 		-> remove image (example docker rmi repository:tag; docker rmi ubuntu:14.04) from the docker host
docker images -q	-> -q [OPTION]  -q, --quiet - Only show numeric IDs
=============================
=============================
CONTAINER LIFECYCLE
docker start <container>
docker stop <container>
docker rm <container>
------------------------------
------------------------------
docker run -d --name web -p 80:8080 nigelpoulton/pluralsight-docker-ci 
 
docker run 	-> start container
-d 			-> --detach - Run container in background and print container ID
--name web 	-> --name string - Assign a name to the container
-p 80:8080	-> maping containers  port from container 8080 to dockerhost 80
nigelpoulton/pluralsight-docker-ci		-> image name from dockerhub
------------------------------
------------------------------
docker run -it --name test ubuntu:latest /bin/bash

docker run 	-> start container
-it			-> 	-i, --interactive	Keep STDIN open even if not attached
			->	-t, --tty         	Allocate a pseudo-TTY	
--name test	->	--name string - Assign a name to the container
ubuntu:latest	-> image name from dockerhub
/bin/bash	-> run bash

+++
To exit the container without stopping press CTRL P+Q
it will switch to background 
------------------------------
------------------------------
docker stop $(docker ps -aq)

docker stop			-> stopping container
docker ps -aq		-> return CONTAINER ID running containers (-a, --all - Show all; -q, --quiet - Only show numeric IDs)
$()					-> putting data in to variable 
					(example: $(docker ps -aq) putting all running containers  id in to vatiable)

Using to stop all running containers 
------------------------------
------------------------------
docker rm $(docker ps -aq)

docker rm 			-> remove container
$(docker ps -aq)	-> variable with all containers  id to remove

To remove all containers 
=============================
=============================
RECAP - container

docker run <image>
