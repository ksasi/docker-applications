# LICENSE GPL 2.0
#Set the base image :
FROM ubuntu:14.04


#File Author/Maintainer :
MAINTAINER Sasikanth Kotti <kotti.sasikanth@gmail.com>


#Set workdir to /opt/gemfire :
WORKDIR /opt/pivotal

RUN apt-get update && apt-get install -y wget

#Obtain/download Java SE Development Kit 7u75 using wget :
RUN wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/7u75-b13/jdk-7u75-l
inux-x64.tar.gz

#Set permissions to gemfire directory to perform operations :
RUN chmod 777 /opt/pivotal


#Setup jdk1.7.0_75 and create softlink :
RUN gunzip jdk-7u75-linux-x64.tar.gz
RUN tar -xvf jdk-7u75-linux-x64.tar
RUN ln -s jdk1.7.0_75 current_java
RUN rm jdk-7u75-linux-x64.tar


#Add gemfire installation file
ADD ./pivotal-gemfire_8.1.0-50625_all.deb /opt/pivotal/

#Set the username to root :
USER root

#Install pivotal gemfire :
RUN dpkg -i pivotal-gemfire_8.1.0-50625_all.deb


#Setup environment variables :
ENV JAVA_HOME /opt/pivotal/current_java
ENV PATH $PATH:/opt/pivotal/current_java:/opt/pivotal/current_java/bin:/opt/pivotal/Pivotal_GemFire_810/bin
ENV GEMFIRE /opt/pivotal/Pivotal_GemFire_810
ENV GF_JAVA /opt/pivotal/current_java/bin/java
