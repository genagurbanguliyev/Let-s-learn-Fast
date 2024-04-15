## List docker container

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
## Remove the container

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

***
### Copy from container to local machine
```sh
docker cp container_id:/path/to/save/model /path/to/save/model/on/host
```