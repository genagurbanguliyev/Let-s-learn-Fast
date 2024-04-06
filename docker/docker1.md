
> **execute a command in a running container**
```sh
docker exec -it <id_or_name_container> bash
```
 -  exec : execute a command in a running container
 - -it [-i -t]: option to connect an interactive terminal
 - bash : name of process, you can write what process you want to run

> Create container with your own specific name container:
```sh
docker run -d --name my_nginx nginx
```
- -d (detached) : runs the container in background
- --name <new_name> : creates your specific name to the container

> **remove container automatically when it stops**
```sh
docker run --rm nginx
```
 - `--rm` - when container stop nginx container removes automatically