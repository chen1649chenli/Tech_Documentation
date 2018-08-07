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

-------------------------Docker for Application---------------------------------------------------
* start Tomcat in docker using port 8888  
```docker run -d -it -p 8888:8080 tomcat:8.0```
