## Start-Stop
###### Start container
```sh
docker start <container_id_or_name>
```
###### Stop container
```sh
docker stop <container_id_or_name>
```

***
## Run skills
*Cr = create*
###### Create & run container with your own specific name container:
```sh
docker run -d --name my_nginx nginx
```
- -d (detached) : runs the container in background
- --name <new_name> : creates your specific name to the container

###### remove container automatically when it stops
```sh
docker run --rm nginx
```
 - `--rm` - when container stop nginx container removes automatically
