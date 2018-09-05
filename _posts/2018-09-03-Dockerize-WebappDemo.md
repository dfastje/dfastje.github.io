---
layout: post 
title: "Dockerizing my WebappDemo" 
date: 2018-09-03
---
## Overview:  
I would like to Dockerize my webapp demo. 

## Steps with references:   

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04  
https://spring.io/guides/gs/spring-boot-docker/  
https://runnable.com/docker/java/dockerize-your-java-application  
https://dzone.com/articles/run-simple-jar-application-in-docker-container-1  
https://hub.docker.com/_/openjdk/  
https://www.youtube.com/watch?v=FlSup_eelYE  
  
####Dockerfile added:
```$xslt
FROM openjdk:8
MAINTAINER DFastjeWork@gmail.com
EXPOSE 8090
COPY target/webappdemo-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java", "-jar", "app.jar"]
```

####pom.xml plugin added:
```$xslt
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-jar-plugin</artifactId>
    <version>3.1.0</version>
    <configuration>
        <archive>
            <index>true</index>
            <manifest>
                <addClasspath>true</addClasspath>
                <mainClass>com.byelkawolf.webappdemo.WebappdemoApplication</mainClass>
            </manifest>
        </archive>
    </configuration>
</plugin>
```
  
####Build and Run:
```$xslt
docker build -f Dockerfile -t docker-example-webapp .
docker images
docker run -p 8090:8090 docker-example-webapp
```

## Conclusion:
The demo webapp ran successfully from the docker container. The next steps that I will either be to enter the docker 
container while it is running to familiarize myself with the openjdk:8 image that I used or to deploy the container on 
an EC2 with ECS managing the containers. 