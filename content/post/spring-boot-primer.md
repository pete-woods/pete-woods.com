---
title: Spring Boot 2.0 primer
date: 2018-08-09
categories:
  - programming
tags:
  - Java
  - Docker
thumbnailImagePosition: left
thumbnailImage: /images/start-journey-thumbnail.jpg
---

Spring Boot is a very popular Java framework for creating standalone, production
ready web applications. In this series of blog posts, we are going to walk through using Spring
Boot 2.0 to build and deploy a simple CRUD REST application.

<!--more-->

We're going to make use of modern Spring technologies such as [Spring Security Oauth2 JOSE](https://docs.spring.io/spring-security/site/docs/5.0.0.RELEASE/reference/htmlsingle/#spring-security-oauth2-jose),
[Spring Cloud AWS](http://cloud.spring.io/spring-cloud-aws/spring-cloud-aws.html), and
[Spring Actuator](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#production-ready),
powered by [Micrometer](https://micrometer.io/).

We're going use [Docker](https://www.docker.com/) to package up the application for deployment,
and to orchestrate the various dependencies we have in our development pipeline.

The source code for the project we will be building is available [here](https://github.com/surevine/spring-rest-example).

The topics we're going to cover are listed below.

# Docker

We'll start by talking about how we orchestrate the development environment, to get us up
and running with MariaDB and Redis effortlessly.

- Building Docker image with Spotify's Dockerfile Maven plugin.
- Composing Docker compose.

# Spring Boot

Once we have our development environment up and running, we'll move over to talking about
how we actually build the application using Spring Boot.

- Spring as a Java container abstraction - switching to Undertow.
- Using `application.yml` as the interface to Docker compose.
- OIDC (OAuth2) authentication with Spring Security JOSE and Google.
- Using Swagger with SpringFox.
- Spring Data JPA with:
  - Liquibase
  - QueryDSL
  - Auditing
- Building a media server with `ResourceHttpRequestHandler`.
- Using Spring Cloud AWS for S3
- Using Spring Cloud AWS with Spring Boot Actuator for putting metrics into CloudWatch.
- Using Spring Session with Redis for Spring Security authentication state.
  - Configuration to support AWS ElastiCache.


