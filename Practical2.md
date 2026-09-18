# INT363 - Practical 2
# Spring Boot with Docker

## Aim
To create a simple Spring Boot web application, test it locally, package it as a JAR file, create a Docker image, and run the Spring Boot application inside a Docker container.

## Spring Boot Endpoint

GET /hello

Expected response:

Hello from Spring Boot with Docker!

## Project Configuration

Project: Maven
Language: Java
Group: com.example
Artifact: demo
Name: demo
Package: com.example.demo
Packaging: Jar
Java: 21
Dependency: Spring Web

## HelloController.java

package com.example.demo;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/hello")
    public String hello() {
        return "Hello from Spring Boot with Docker!";
    }
}

## Run Spring Boot Locally

.\mvnw.cmd spring-boot:run

## Test Locally

http://localhost:8080/hello

Expected:
Hello from Spring Boot with Docker!

## Build JAR

.\mvnw.cmd clean package -DskipTests

## Check JAR

dir target

## Dockerfile

FROM eclipse-temurin:21-jre

WORKDIR /app

COPY target/*.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]

## Build Docker Image

docker build -t springboot-docker-demo .

## Check Docker Images

docker images

## Run Docker Container

docker run -d --name springboot-container -p 9090:8080 springboot-docker-demo

## Check Running Container

docker ps

## Test Dockerized Application

http://localhost:9090/hello

Expected:
Hello from Spring Boot with Docker!

## View Container Logs

docker logs springboot-container

## Stop Container

docker stop springboot-container

## Check All Containers

docker ps -a

## Remove Container

docker rm springboot-container

## Complete Workflow

Spring Boot Project
        ↓
HelloController
        ↓
Run Locally
        ↓
Build JAR
        ↓
Dockerfile
        ↓
Docker Image
        ↓
Docker Container
        ↓
localhost:9090/hello
