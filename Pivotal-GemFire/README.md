Pivotal-GemFire on Docker
===============
Docker configurations to facilitate installation, configuration, and environment setup for developers. This project includes [dockerfiles](./) for pivotal-gemfire 8.1.0 with JDK 7 on Ubuntu 14.04.

## Based on Official Ubuntu Docker images
For more information please read the [Docker Images for Ubuntu](https://registry.hub.docker.com/_/ubuntu/) page.

## How to build and run
This project offers Dockerfiles for pivotal-gemfire 8.1.0.See below for instructions and usage.

### Building pivotal-gemfire Images

Follow this procedure:

1.Checkout the GitHub docker-applications repository

$ git checkout git@ggithub.com/ksasi/docker-applications.git

2.Go to the Pivotal-GemFire folder

$ cd Pivotal-GemFire

3.[Download](https://network.pivotal.io/products/pivotal-gemfire) and drop Pivotal GemFire 8.1.0* Linux Debian Installer in this folder

4.Execute the following as root

docker build -t gemfire:8.1.0 .


## License
To download and run pivotal-gemfire 8.1.0 regardless of inside or outside a Docker container you must agree and accept the EULA.

To download and run Oracle JDK regardless of inside or outside a Docker container, you must agree and accept the [Oracle Binary Code License Agreement for Java SE](http://www.oracle.com/technetwork/java/javase/terms/license/index.html).

All scripts and files hosted in this project and GitHub [docker-applications/Pivotal-GemFire](./) repository required to build the Docker images are, unless otherwise noted, released under the Common Development and Distribution License (CDDL) 1.0 and GNU Public License 2.0 licenses.