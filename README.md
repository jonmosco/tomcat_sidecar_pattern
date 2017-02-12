###Tomcat webapplication deployment

###This is a POC for putting the sidecar container pattern to use

Deploys the sample.war from a container to a mounted VOLUME exposed
inside the tomcat container in /usr/local/tomcat/webapps/

##Sidecar Container Pattern

###Side Container

busybox for the base image
