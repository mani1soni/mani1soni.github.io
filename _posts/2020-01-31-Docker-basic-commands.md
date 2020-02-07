---
layout: post
title:  "Essential Docker Commands"
date:   2019-10-31
desc: "Basic Docker Commands for Newbies"
keywords: "Docker,DevOps,commands,docker-commands,Tutorial,blog,mani1soni, Manish Soni"
categories: [Devops]
tags: [Docker,DevOps,commands,docker-commands,Tutorial,blog,edu_adda]
icon: icon-linux
---


<div align="center" id="top">
	<br>
	<br>
	<br>
	<img width="500" height="350" src="https://raw.githubusercontent.com/mani1soni/mani1soni.github.io/master/static/assets/img/docker.jpeg" >
	<br>
	<br>
	<br>
 
<br>
</div>

# Docker
<p> Have you ever stucked with "This code is properly running on my machine but why not on my team lead's?.<br>
So, what is the solution? <br>
Don't Worry!, Docker is here to remove your platfrom dependencies. <br>  
Docker is a set of platform as a service(PAAS) products that use OS-level virtualization to deliver software in packages called containers.
Containers are isolated from one another and bundle their own software, libraries and configuration files; they can communicate with each other through well-defined channels.
BTW i'm not going to define them deeply, I am here to present essential commands of docker that you should know while working with this. </p> 


#### Getting Started

* Search Images on Docker Hub

    ```
        $ docker search "Image Name"
    ```

* For Pull images from Docker Hub

    ```
        $ docker pull "Image Name"
    ```
    
* Running a container, always give proper name to container for future refrence.

    ```
        $ docker run --name [CONATINER_NAME] [IMAGE_NAME]
    ```
    
    you can also use many flags with this, like
    ```
        -it ==> For intrective terminal
        -d ==> For detach mode
        -p ==> For port forwading
        --restart=always ==> Autostart on rebooting machine
    ```
    
* For start , stop , delete and checking images & container

    ```
        $ docker images ==> give a list of locally stored images
    
    
     
        $ docker rmi -f [IMAGE_ID or NAME] ==> for deleting images(forcefully)
    
    
    
        $ docker rm -f [CONTAINER_ID or NAME] ==> for deleting container(forcefully)
    
    
    
        $ docker rm -f [CONTAINER_ID or NAME] `$ docker ps -aq` ==> for forcefully deleting all containers(stopped and running both). 
    
    
    
        $ docker ps ==> for running containers
    
    
    
        $ docker ps -a ==> for attached containers(all running or not running)
    
    
    
        $ docker start [CONTAINER_NAME] ==> for start a stopped container
   
    
    
        $ docker stop [CONTAINER_NAME] ==> for stop a container
    
    
    
        $ docker inspect [CONTAINER_NAME or IMAGE_NAME] ==> for inspecting them 
    ```
    
#### Executing commands in container
* For executing command
    ```
        $ docker exec -it [CONATINER_NAME] `bash/sh` or `command` ==> for executing shell or commands in interctive mode. 
    ```
* For attaching to container
    ```
        $ docker attach [CONATINER_NAME] ==> for attaching a running container.
    ```


#### Commands related to Network, logs, system_info, volume

* For Network
    ```
        $ docker network create [NETWORK_NAME] ==> for creating a network
    
    
    
        $ docker network ls ==> listing docker networks
    ```
    
* For logs

    ```
        $ docker logs [CONTAINER_NAME] ==> for all logs of container
    
    
    
        $ docker logs [CONTAINER_NAME] --tail (line_count) ==> for get specified lines 
    ```
    
* For system_info (important)
    ```
        $ docker stats ==> live status of cpu, memory and network bandwidth usage of containers
    

    
        $ docker system df -v ==> for  detail storage information of images and containers.
    
    
   
        $ docker system prune ==> for deleting dangling images and unused containers.
    ```
    
* For volume
    ```
        $ docker volume create [CONTAINER_NAME] ==> for creating a volume
    ```
    
    you can also mount a volume to the container by using `-v` flag at run time.


#### Commands related to backup, restore and building images from container

* For backup & restore
    ```
        $ docker save [IMAGE_NAME] > [IMAGE_NAME].tar ==> saving images in `tar`
    
    
    
        $ docker load < [IMAGE_NAME].tar ==> for restoring a image.
    ```
* For building images from container (sometimes baneficial)
    ```
        $ docker container commit  [CONTAINER_NAME] [IMAGE_NAME:TAG(repo_name)] ==> for commiting changes in container as image.
    ```

#### Essential points for deploying applicaions with docker

#####  _Always mount the `volumes` in containers._
#####  _Always give `name` to the container._
#####  _Use `docker network` for same networking applications._
#####  _Always use `restart policies` in all environments._
   

 _**Happy Reading**_ 

#### Connect with me 


| <img alt="Manish Soni" src="https://avatars3.githubusercontent.com/u/30206849?s=460&v=4" height="70"   />                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Manish Soni](https://mani1soni.github.io/)<br><strong>Twitter</strong>: [@manisomanish](https://twitter.com/manisomanish)<br><strong>Github</strong>: [@mani1soni](https://github.com/mani1soni)<br> <strong>Linkedin<strong>: [@manisomanish](https://www.linkedin.com/in/manisomanish)<br> _DevOps Engineer_ |






    




















