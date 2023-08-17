# Java Web Service Stack Local R&D Environment Manual and Auto Setup

## Introduction
This project focuses on establishing a research and development (R&D) application stack for serving Java web applications, allowing for both manual and automated setups. Vagrant is utilized to facilitate this configuration.

For setup details, explore the following directories:

- The directory for manually set up: [Manual setup](vagrant/manual)
- The directory for automated set up: [Automated setup](vagrant/auto)

The content is organized into the following sections:

- [Java Web Service Stack Local R\&D Environment Manual and Auto Setup](#java-web-service-stack-local-rd-environment-manual-and-auto-setup)
  - [Introduction](#introduction)
  - [Prerequisite](#prerequisite)
  - [Architecture Stack](#architecture-stack)
  - [Manual Provisioning](#manual-provisioning)
  - [Automated Provisioning](#automated-provisioning)

## Prerequisite

To proceed, ensure you have the following tools and resources available:

- Oracle VM Virtualbox (version: 7.0.8 r156879)
- Vagrant (version: 2.3.7)
- Vagrant plugins:
  - ```vagrant plugin install vagrant-hostmanager```
- Git bash or equivalent editor

## Architecture Stack
The diagram below outlines the server components included in this project setup. The configuration involves setting up five distinct services:



- Nginx: A reverse proxy server
- Tomcat: Java web application backend server
- Memcache: Database caching service
- RabbitMQ: Message queueing broker
- MySQL: SQL database to store user info

![Architecture Stack](images/architecture-stack.png)


The Java application, a simple login website deployed on Tomcat, authenticates users by checking against user credentials stored in the MySQL database. For swift retrieval, user information is also cached in a memcache caching service. The source code structure of the Java web application is located in the [src](src) directory.

## Manual Provisioning
Please refer to [README.md](vagrant/manual/README.md) for detailed steps.

## Automated Provisioning
Please refer to [README.md](vagrant/auto/README.md) for detailed info.

