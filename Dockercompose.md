# Docker compose command 

To create the network,volumes,build images and start all the services as defined in the compose.yaml use 
```bash
docker compose up
```
In detached mode
```bash
docker compose up -d
```
To just stop all the containers defined in the compose.yaml file 
```bash
docker compose stop
```

To stops all the container and remove conatiner and network created by the compose use
```bash
docker compose down
```
To remove volume also use
```bash
docker compose down -v
```


To only build the image defined  in compose.yaml use 
```bash
docker compose build
```
To list all the conatainers managed by this Compose project 
```bash
docker compose ps
```
To show the logs of all the services
```bash
docker compose logs
```
follow logs:
```bash
docker compose logs -f
```
specific service:
```bash
docker compose log web
```
To execute a command inside a running contianer :
```bash
docker compose exec web sh
```

To restart one or more services
```bash
docker compose restart
docker compose restart service_name
```




























