# LICENSE CDDL 1.0 + GPL 2.0
#Set the base image :
FROM ksasi/oraclelinux:6.5

#File Author/Maintainer :
MAINTAINER Sasikanth Kotti <kotti.sasikanth@gmail.com>

#Update packages and install wget and man :
RUN yum update -y -q
RUN yum install -y -q wget man tar sudo
RUN useradd obiee

#Set the username to obiee :
#USER obiee

#Disable firewall :
#RUN service iptables stop
#RUN chkconfig iptables off

#Set workdir to /opt/Middleware :
WORKDIR /opt/Middleware

#Obtain/download Java SE Development Kit 7u71 using wget :
RUN wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/7u71-b14/jdk-7u71-l
inux-x64.tar.gz

#Set permissions to Middleware directory to enable obiee user perform operations :
RUN chmod 777 /opt/Middleware

#Set the username to obiee :
USER obiee

#Setup jdk1.7.0_71 and create softlink :
RUN gunzip jdk-7u71-linux-x64.tar.gz
RUN tar -xvf jdk-7u71-linux-x64.tar
RUN ln -s jdk1.7.0_71 current_java
RUN rm jdk-7u71-linux-x64.tar

#Setup environment variables for java :
ENV JAVA_HOME /opt/Middleware/current_java
ENV PATH $PATH:/opt/Middleware/current_java:/opt/Middleware/current_java/bin

#Add weblogic installation file and configuration file for silent installation :
ADD ./wls1036_generic.jar /opt/Middleware/
ADD ./silent.xml /opt/Middleware/

#Silent Installation of weblogic :
RUN java -Xmx1024m -jar wls1036_generic.jar -mode=silent -silent_xml=/opt/Middleware/silent.xml

#Set the username to root :
USER obiee
