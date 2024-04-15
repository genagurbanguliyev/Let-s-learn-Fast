> Creating own docker image you need Dockerfile that contains structure of image
`Dockerfile`:
```dockerfile

# base image that your project works with
FROM python:alphine

# creates /app directory thats not confuse other image file/folder. and your location was there
WORKDIR /app

# the first `.` path to your project and if you inside project root directory you can write `.` | the second `.` show path inside the image it will be `/app`
COPY . .

# run process after creation image. this process will happen in container, nor in an image
CMD ["python", "main.py"]
```

> Build docker image:
```sh
docker build .
```
 - if you in the root directory and your `Dockerfile` with this name you can put `.` Because docker automatically takes that named `Dockerfile` . But if your Dockerfile named like `Dockerfile.dev` or `Dockerfile.prod` your must show that name...
 - this builds an image with random ID

> if your want build an image with specific name and tag:
```sh
docker build -t my_dockerimage:1.0 .
```

 - `-t` - add name and tag to new created docker image/
 - `tag` - if you don't show tag(version) docker automatically create with tag `latest`