---
layout: post 
title: "Embedded H2 DB in Springboot with SPRING INITIALIZR" 
date: 2018-09-11
---
## Overview:  
I need an easy database so I am going through an H2 Embedded DB in springboot.

## Steps with references:   
 
http://www.springboottutorial.com/spring-boot-and-spring-jdbc-with-h2

  
#### Spring Initializer Dependencies: https://start.spring.io/
```$xslt
H2
Web
JDBC
DevTools
Lombok
```

#### application.properties configurations:
```$xslt
# Enabling H2 Console
spring.h2.console.enabled=true
```

#### Build and Run:
```$xslt
mvn clean package
mvn spring-boot:run
```

#### Access H2 Console: http://localhost:8080/h2-console
```$xslt
Saved Settings: Generic H2 (Embedded)
Setting Name:   Generic H2 (Embedded)
Driver Class:   org.h2.Driver
JDBC URL:       jdbc:h2:mem:testdb
User Name:      sa
Password:        
```

## Conclusion:
I now have the embedded H2 DB running from my Spring Boot application. 
The next step in this process will be to create the schema for the DB. 