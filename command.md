# Common `Docker` ommands

## Show image and containers
    $ docker images - show all images
    $ docker ps - show active containers 
    {-a all containers, 
    -q show id's}

## Build image
    $ docker build -t 'tag_name' '/path/' - build image from Dockerfile
## Remove image
    $ docker rmi 'docker_image_id' - remove docker image
    $ docker rmi $(docker images -aq) - remove all images
## Run container
    $ docker run 'tag_name' - run Docker container from image 
    {--name 'container_name' - for naming container,
    -d - execute container in background mode,
    --rm - remove container afteer executing}
## Stop container
    $ docker stop 'container_id' - stop executing container
## Remove container
    $ docker rm 'container_id' - remove container
    $ docker rm $(docker ps -aq) - remove all containers
    

## Example
    1. $ docker build -t test_docker . - create docker image
    2. $ docker images - show all images
    3. $ docker run --rm --name web -p 8080:8080 test_docker - run container
    4. $ docker ps -a - show all containers


