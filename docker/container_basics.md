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
## Remove docker container

###### Remove container
```sh
docker rm <container_id_or_name>
	
# Remove a Running Container
docker rm -f <container_id_or_name>

# Remove Multiple Containers
docker rm <container_id_1> <container_id_2> <container_id_3>

# remove all stopped containers
docker container prune
```

###### run container, if stop it removes automatically: [[container_running_basics#remove container automatically when it stops]]
***
###### execute a command in a running container
```sh
docker exec -it <id_or_name_container> bash
```
 -  exec : execute a command in a running container
 - -it [-i -t]: option to connect an interactive terminal
 - bash : name of process, you can write what process you want to run

***
## Copy file(folder)
```sh
docker cp container_id:/path/to/save/model /path/to/save/model/on/host
```