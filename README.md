#  Docker

This is an introduction to docker. On the following pages you will see multiple docker commands used daily as well some advanced docker commands. At the end of this whole document you can find some more links to other sides and references I found useful.

--------

## Intro 

Docker is a tool to run your application inside of a container. 
A container exists of an image which you can write by your own with a Dockerfile or you can use a prebuild image already write for you. As soon as you build the image and run it, it starts a container which uses the host system unlike a vm. 

**Image**: A Docker image is a file, this file itself is build by a file named Dockerfile. You can not edit an existing file but you can add a layer to it.
 
**Container**: A Docker container is an isolated environment in the host machine, which only includes stuff it needs to run your application. You can start, stop and interact with them. 

