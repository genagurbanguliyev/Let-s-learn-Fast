## Work with docker-image

> Docker image - 
> **Run docker image**
```sh
docker run <docker-image-id> # image-id first 3 digit you can write
```

> **Remove docker-image**
```sh
# remove docker-image
docker rmi <docker-image-id>

# remove in image run using --force
docker rmi -f <docker-image-id>
```


***
### Work with docker container

##### Start-Stop the Container
> **Stop container**
```sh
docker stop <container_id_or_name>
```

#### List docker container

> **To list only the running containers**
```sh
docker ps
```

> **To list all containers**
```sh
docker ps -a
```

> **Format the Output**
```sh
docker ps --format '{{.ID}} {{.Names}}'
```

***
#### Remove the container

> remove container
```sh
docker rm <container_id_or_name>
	
# Remove a Running Container
docker rm -f <container_id_or_name>

# Remove Multiple Containers
docker rm <container_id_1> <container_id_2> <container_id_3>

# remove all stopped containers
docker container prune
```
