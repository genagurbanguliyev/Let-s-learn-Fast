## login cli
if you want to push docker hub you local images you should be logined. For that:
```shell
$ docker login
username: <your-username>
password: <password or token>
```
or
```shell
$ docker login -u <username_docker_hub>
password:
```
 - For `password:` use `api-key token` from hub.docker.com `My Account > Security > Create New Access Token`

# Errors when login
 - ###### Error saving credentials: [[login_errors#Error saving credentials]]