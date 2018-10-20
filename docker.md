## Hello World Example  
* start a docker container using "docker run image_id:tag"  

```docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG…]```  
Example: ``` docker run -d -p 80:80 --name pintail-whoami --rm pintailai/pintail-whoami:0.0.1 ```  
1. run — Specify the run command to tell Docker you want to run a new container  
2. -d — Tells docker to run the new container in detached mode. This will force the container to run in the background rather than locking up your terminal window  
3. -p — tells Docker what ports to map from the container to your host OS. The format is {host-os-port:container-port}. In this case docker will map port 80 from your host OS to port 80 inside the container  
4. '- - name' — names the container “pintail-whoami”  
5. pintail/pintail-whoami:0.0.1 — this last argument indicates the specific image you would like to start. For images hosted on Docker Hub the format is {organization_name}/{image_name}:{version}
6. --rm remove the container after it exits


---------------------------------------------------------
* check running docker  
``` docker ps```

* check all docker in local box, including the ones that have been stopped  
```docker ps -a```

* docker inspect displays the low level information about a container or image  
```docker inspect 28b3e4a98989```

* check container logs  
```docker logs 28b3e4a98989```

* stop container  
```docker stop [OPTIONS] CONTAINER [CONTAINER…]```

* remove container  
```docker rm [OPTIONS] CONTAINER [CONTAINER…]```

* view images  
```docker images```

* remove images  
```docker rmi [OPTIONS] IMAGE [IMAGE...]```

-------------------------Docker for Application ---------------------------------------------
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
