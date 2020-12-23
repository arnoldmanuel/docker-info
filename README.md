#  Docker

This is an introduction to docker. On the following pages you will see multiple docker commands used daily as well some advanced docker commands. At the end of this whole document you can find some more links to other sides and references I found useful.

--------

## Intro 

Docker is a tool to run your application inside of a container. 
A container exists of an image which you can write by your own with a Dockerfile or you can use a prebuild image already write for you. As soon as you build the image and run it, it starts a container which uses the host system unlike a vm. 

**Image**: A Docker image is a file, this file itself is build by a file named Dockerfile. You can not edit an existing file but you can add a layer to it.
 
**Container**: A Docker container is an isolated environment in the host machine, which only includes stuff it needs to run your application. You can start, stop and interact with them. 

Containers are instances of images. 

## Docker CLI Basics

docker run command will search locallly on your machine for the image you want to run, if it can not find it docker will pull it from docker hub and after initializing it will run the image in a container 

Use pull instead of run if you only want to download the image 

```bash
docker run hello-world 
```

You can use the -d flag to run the container in detached mode.

To see which images you have currently downloaded use docker images or docker image ls

```bash
docker images 
```
```bash
docker image ls  
```

To list which containers are running run: docker container ls

```bash
docker container ls  
```

If you want to see all containers and not only the ones which are running, use the -a flag for all

```bash
docker container ls -a  
```

To remove an image you can run: docker rmi (image name)

```bash
docker rmi hello-world 
```

Sometimes you can get an error message saying that you can not delete the image. This is because the image is still referenced in the container. So before you can delte the image you might need to run docker container rm (container id or name)

```bash
docker rm 3dffr 
```