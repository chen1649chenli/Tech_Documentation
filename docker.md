## Hello World Example  
* start a docker container using "docker run image_id:tag"  
```docker run busybox:latest echo "hello world"```

* run a docker container in a detached mode using "-d"   
```docker run -d  busybox:latest echo "hello world"```

* run a docker container and remove the container after it exits  
```docker run -rm    busybox:latest echo "hello world"```

* run a docker container with a name  
```docker run --name hello_world    busybox:latest echo "hello world"```
---------------------------------------------------------
* check running docker  
``` docker ps```

* check all docker in local box, including the ones that have been stopped  
```docker ps -a```

* docker inspect displays the low level information about a container or image  
```docker inspect 28b3e4a98989```

* check container logs  
```docker logs 28b3e4a98989```

-------------------------Docker for Application ---------------------------------------------------
* start Tomcat in docker using port 8888  
```docker run -d -it -p 8888:8080 tomcat:8.0```
* start debian in docker   
```docker run -it debian:jessie```

-------------------------Create new Docker image by commit --------------------------------
1. use the original docker ```docker run -it debian:jessie```. This docker doesn't have git installed.
2. install git ```apt-get update && apt-get install -y git```
3. Docker commit a new image ```docker commit container_ID repository_name:tag```
4. Example ```docker commit 5412d8cbbffa chen1649chenli/debian:1.00```
5. the git installation is persisted in the new image.

-------------------------Create new Docker image by Dockerfile --------------------------------
1. Create a Docker file ```vi Dockerfile```
2. enter the following commands in the Dockerfile   
```FROM debian:jessie
RUN apt-get update      
RUN apt-get install -y git
RUN apt-get install -y vim```
3. run command ```docker build -t chen1649chenli/debian .```
