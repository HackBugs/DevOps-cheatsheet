# New-docker-installation-setup

This documentation about docker
Author : HackBugs

Documentation : All About docker installation And setup and how to configure
----------------------------------------------------------------------------------
1 - Devops:
-------------

https://app.eraser.io/workspace/5bTzpbKkfb3PdcgYZ4Je

- In devops same like a datagard mean we make replica and duplicate of production database
same like we make replica and duplicate make make of aur environments where development working
we can make a container and of that container we can mutiple replicas and can share of each new deveploper 

- That means I want to work on a project where more than 50 or 100 programmers are working together. If 50 new people join the company, they will want to work on that project and start creating code. However, before writing code, they need to set up the required environment for that technology. For example, if I need to set up Android Studio for developing an application, the issue could arise if my teammates are using an older version of Android Studio. When I install Android Studio, it might be the latest version, and trying to run the project code could result in errors due to version differences. Additionally, my team might be using different operating systems like macOS, Linux, or Windows, which can also lead to environment setup errors.

Thats why we use of "Docker"

"Docker image and docker container"
Docker "image" is like class and docker "container" like object

Simple real prectical example of docker container and docker image
- Docker image means operation system it could be ubuntu or linux or mac anything only OS
- Docker container is act like virtual mechine not exctly vitual machine bec virtual machine is occupied more storage and container 
occupied less but is work same like virtual machine container is environment where i can install os, packeges, softwars etc which we 
install on one operating system

with docker can build the container
and of container we can make duplicate containers like local environment
and can use of that container to build and deploy projects without environment issues
------------------------------------------------------------------------------------------------
FROM ubuntu

RUN apt-get update
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -
RUN apt-get upgrade -y
RUN apt-get install -y nodejs

COPY package.json package.json
COPY package-lock.json package-lock.json
COPY main.js main.js

RUN npm install

ENTRYPOINT [ "node", "main.js" ]
------------------------------------------------------------------------------------------------
Container or virtual machine manager, such as: 
Docker, QEMU, Hyperkit, Hyper-V, KVM, Parallels, Podman, VirtualBox, or VMware Fusion/Workstation
------------------------------------------------------------------------------------------------

2 - Kubernetes:
----------------
