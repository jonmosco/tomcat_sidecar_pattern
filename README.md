##Tomcat application deployment container

###This is a POC that puts the sidecar container pattern to use

Deploys the sample.war from a container to a mounted VOLUME exposed
inside the tomcat container in /usr/local/tomcat/webapps/

##Sidecar Container Pattern

https://www.usenix.org/system/files/conference/hotcloud16/hotcloud16_burns.pdf

###Vagrant environment

This image can run locally as long as the docker engine is isntalled, and
comes with Vagrantfile VM on CentOS 7 with the latest Docker engine.

###Server Container

```docker
```
###Side Container

```docker
FROM busybox:latest
```

Build the image:
$ docker buid sidecar/

Run the container:
```
$ docker run -t -i --name sidecar_test sidecar_war
```

Keep the container running:
```
$ docker run -d --name sidecar_test03 sidecar_war tail -f /dev/null
```
