# Common `Docker` ommands

## Show images
    $ docker images - show all images
## Show containers
    $ docker ps - show active containers 
    {-a all containers, 
    -q show id's}
## Show volumes 
    $ docker volume ls
---
## Build image
    $ docker build -t 'tag_name' '/path/' - build image from Dockerfile
## Remove image
    $ docker rmi 'docker_image_id' - remove docker image
    $ docker rmi $(docker images -aq) - remove all images
## Run container
    $ docker run 'tag_name' - run Docker container from image 
    {--name 'container_name' - for naming container,
    -d - execute container in background mode,
    --rm - remove container afteer executing,
    -v 'volume_name:absolute_path',
    -p 8080:8080 - port in computer and in container}
## Stop container
    $ docker stop 'container_id' - stop executing container
## Remove container
    $ docker rm 'container_id' - remove container
    $ docker rm $(docker ps -aq) - remove all containers

## Create volume
    $ docker volume create 'volume_name'
    
## Example
    1. $ docker build -t test_docker . - create docker image
    2. $ docker images - show all images
    3. $ docker run --rm --name web -p 8080:8080 -v volume_web:/usr/src/app/resources test_docker - run container
    4. $ docker ps -a - show all containers


