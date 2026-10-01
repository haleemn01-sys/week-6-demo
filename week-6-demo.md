# Week 6 Demo

## Build the image

```shell
# build an image using the Dockerfile in this folder (the . means "this folder")
# --tag gives your image a name, so you can use it later instead of a long random ID
docker build --tag week-6-demo .
```

## List images

```shell
docker image list
```

## Create a container from the image

```shell
# create a new container from the image (it is not running yet)
# --name gives the container a name, so you can use it in later commands
# --publish maps host_port:container_port, here host 8080 -> container 80
docker create --name week-6-demo-container --publish 8080:80 week-6-demo
```

## List all containers (including ones not running)

```shell
# --all shows every container, including ones that are stopped or not started yet
# our new container shows up here with a status of "Created"
docker container list --all
```

## Start the container

```shell
# start the container we just created
docker start week-6-demo-container
```

## List running containers

```shell
# without --all, only running containers are shown
docker container list
```
