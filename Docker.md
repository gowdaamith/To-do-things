                                                  # DOCKER COMMAND 

Docker Container Command :
---------------------------------------------------------------------------------------------------------------

Used to run a new container 
```bash
docker run -d -p 3000:3000 image_name
```
Used to run already existing container
```bash
docker start image_name

```
Used to stop a container 

```bash
docker stop image_name
```

Used to restart the container (better then stopping and restarting it again )

```bash
docker restart image_name
```
Used to  remove a container
```bash
docker rm image_name
```
Used to force remove the container 

```bash
docker  rm -f image_name
```
List all running Containers
```bash 
docker ps
```
List all running and Stopped Containers
```bash
docker ps -a
```
Show the logs of the container stdout/stderr
```bash
docker logs image_app
```
Shows flow logs
```bash
docker logs -f  image_name
```
Accessing the container terminal / connecting into the container
```bash
docker exec -it image_name sh
```
To know full metadata about the container
```bash
docker inspect image_name
```
To see Live CPU ,Memory , Network usage
```bash
docker stats
```
To remove unused containers
```bash 
docker container prune
```

_______________________________________________________________________________________________________________

Docker Images
-------------------------------------------------------------------------------------------------------------
List all the images stored 
```bash
docker images
```
Downloada an Image from the repository 
```bash
docker pull node:18-alpine
```
Upload an image to the registry 
```bash
docker push  registry/namespace/repository:tag
```
Build an image from the dockerfile
```bash
docker build -t myapp:1.0
```
Remove a local image 
```bash
docker rmi image_name:tag / image_id
```
Create a new refference to the same image
```bash
docker tag myapp:1.0 gowdaamith:1.0
```
Image history (show the image layer and its size)
```bash
docker history image_name:1.0
```
Full metadata about the image
```bash
docker inspect  image_id / image_name and Tag
```
To remove unused images
```bash
docker images prune
```

_____________________________________________________________________________________________________________        
Docker volume
-------------------------------------------------------------------------------------------------------------
List all the docker managed  volumes on the host
```bash
docker volume ls
```
Create a named volume explicitly 
```bash
docker volume create volume_namek
```
See detailed metadata about the volume
```bash
docker volume inspect volume_name
```
Remove a Volume
```bash
docker volume rm volume_name
```
Remove Unused volume 
```bash
docker volume prune
```
_______________________________________________________________________________________________________________
Docker Network
----------------------------------------------------------------------------------------------------------------
List all Docker network 
```bash
docker network ls
```
Create a new network
```bash
docker network create  network_name
```
Inspect the network
```bash
docker network inspect network_name
```
Remove a network 
```bash
docker network rm network_name
```
Delete unused network
```bash
docker network prune
```
________________________________________________________________________________________________________________
System level command 
----------------------------------------------------------------------------------------------------------------
 To see System-wide info about the docker 
```bash
docker info
```
To see the version of the docker  use
```bash
docker version
```
To see the disk usage by the docker use 
```bash
docker system df 
```
To remove unused Docker resources 
```bash
docker system prune
```
with -a we can remove unused images (even taged ones)
```bash
docker system prune -a
```
______________________________________________________________________________________________________________

Some command 
--------------------------------------------------------------------------------------------------------------
To login
```bfash
docker login
```
for  Registry specific login
```bash
docker login ghrc.io
docker login public.ecr.aws
```
To logout
```bash
docker logout
```
To search images in Dockerhub
```bash
docker search nginx
```
To download the images from the docker hub
```bash
docker pull image_name:tag
```
Docker build on steroids
```bash
docker biuldx build .
```
```bash
docker login
docker buildx build \
  --platform linux/amd64 \
  -t gowdaamith/myapp:${BUILD_NUMBER} \
  --push .
docker logout
```

_________________________________________________________________________________________________________________
Docker Debugg command 
-----------------------------------------------------------------------------------------------------------------
copy files between the host and Container
```bash
docker cp mycontainer:/app/logs/app.log  .
docker config.json mycontainer:/app/config.json
```
To see filesystem changes in a container compared to its image
```bash
docker diff mycontianer
```
Streams real-time Docker daemon events
```bash
docker events
```
To see the process running inside the container 
```bash
docker top my_container
```
To wait until a container stops use 
```bash
docker wait container_name
```

________________________________________________________________________________________________________________
# The most important command 

```bash
docker help
```
its use as :
```bash
docker container --help
docker  image --help
docker volume --help
```









































































