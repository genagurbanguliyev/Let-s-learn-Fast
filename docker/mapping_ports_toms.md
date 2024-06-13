## Mapping ports
```sh
docker run -p 8080:80 nginx
```

 - `run` - create and run container
 - `-p` - publish port
 - `8080` - external port [port of your computer]
 - `80` - internal port [port of container]
 - `nginx` - name of image

## Mapping toms
```sh
docker run -v ${PWd}:/usr/share/nginx/html nginx
```

- `-v` (volume)- connection toms
- `${PWD}`- directory to locale folder (from computer). `${PWD}` gets your location into terminal for now. instead it you can write the Absolute directory to project
- `/usr/share/nginx/html` - directory to folder inside of the container

> Mapping toms and ports together:
```sh
docker run -v /User/username/Desktop/projectfolder:/usr/share/nginx/html -p 8080:80 -d nginx
```
