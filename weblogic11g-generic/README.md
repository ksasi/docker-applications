WebLogic on Docker
===============
Docker configurations to facilitate installation, configuration, and environment setup for developers. This project includes [dockerfiles](weblogic11g-generic/) for both WebLogic 11g 10.3.6 with JDK 7 on OracleLinux 6.5.

## Based on Official Oracle Linux Docker images
For more information please read the [Docker Images from Oracle Linux](https://registry.hub.docker.com/_/oraclelinux/) page.

## How to build and run
This project offers Dockerfiles for WebLogic 11g (10.3.6).See below for instructions and usage.

### Building WebLogic Images

Follow this procedure:

1.Checkout the GitHub docker-applications repository

$ git checkout git@ggithub.com/ksasi/docker-applications.git

2.Go to the weblogic11g-generic folder

$ cd weblogic11g-generic

3.[Download](http://www.oracle.com/technetwork/middleware/weblogic/downloads/wls-main-097127.html) and drop Oracle WebLogic Server 11gR1 (10.3.6) generic installer(For 64-bit JVM) in this folder

4.Execute the following as root

docker build -t weblogic:10.3.6 .


## License
To download and run WebLogic 11g Distribution regardless of inside or outside a Docker container you must agree and accept the [OTN Free Developer License Terms](http://www.oracle.com/technetwork/licenses/wls-dev-license-1703567.html).

To download and run Oracle JDK regardless of inside or outside a DOcker container, you must agree and accept the [Oracle Binary Code License Agreement for Java SE](http://www.oracle.com/technetwork/java/javase/terms/license/index.html).

All scripts and files hosted in this project and GitHub [docker-applications/weblogic11g-generic](./) repository required to build the Docker images are, unless otherwise noted, released under the Common Development and Distribution License (CDDL) 1.0 and GNU Public License 2.0 licenses.