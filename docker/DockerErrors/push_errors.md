## requested access to the resource is denied:
 ```
docker push payload_cms_next14:1.0
The push refers to repository [docker.io/library/payload_cms_next14]
f68d0b059aa8: Preparing 
efabfe1fb2af: Preparing 
32ee1dc2f44e: Preparing 
cbe3a5ca19f1: Preparing 
2208e0a70b08: Preparing 
edeaab47fd31: Waiting 
29ddfb506e6b: Waiting 
1dd574bd2c87: Waiting 
d101fffc6eaf: Waiting 
994393dc58e7: Waiting 
denied: requested access to the resource is denied

```
***
firstly check that you login docker:

```
# you may need log out first `docker logout` ref. https://stackoverflow.com/a/53835882/248616
docker login
```

According to the [docs](https://docs.docker.com/engine/getstarted/step_six/#/step-1-tag-and-push-the-image):

```
You need to include the namespace for Docker Hub to associate it with your account.
The namespace is the same as your Docker Hub account name.
You need to rename the image to YOUR_DOCKERHUB_NAME/docker-whale.
```

So, this means you have to **tag** your image before pushing:

```
docker tag firstimage YOUR_DOCKERHUB_NAME/firstimage
```

and then you should be able to push it.

```
docker push YOUR_DOCKERHUB_NAME/firstimage
```