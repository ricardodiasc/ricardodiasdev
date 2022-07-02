---
title: Multistage build Java images
date: "2022-05-18T22:40:32.169Z"
description: "How to configure a docker image to build  the project and the docker image to your java project"
enabled: true
---

Starting the works in this


## Multilevel docker build

It is possible do define in a dockerfile a multilevel docker build.

```Dockerfile
FROM maven:3.8.6-eclise-temurin-18 as builder

RUN mvn clean install 

FROM eclipse-temurin:18-alpine

EXEC java -jar app.jar


```



## Default configuration and size

Let start with just a basic docker configuration with a full JDK 8 installation.

```Dockerfile
FROM maven:3.8.6-eclise-temurin-18

FROM eclipse-temurin:18-alpine

EXEC java -jar app.jar


```



## Level 1 - Customizing your jvm

## Level 2 - Using native compilation

## Quarkus

## Spring

## Oracle driver for jdbc

