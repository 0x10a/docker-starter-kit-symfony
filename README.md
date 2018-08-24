# Docker Starter kit Symfony 4

Stack to start a new project with Symfony 4 and Docker.

This stack comes with:
Apache
MySQL
PHP 7.2.3
PHPMyAdmin
ELK (Elasticsearch Logstash and Kibana) 

# Installation

## 1. Docker installation

Docker for Windows is the Community Edition (CE) of Docker for Microsoft Windows. To download Docker for Windows, head to the [Docker Store](https://store.docker.com/editions/community/docker-ce-desktop-windows).

## 2. Git installation

Download the latest version of Git for Windows [here](https://git-scm.com/download/win).

## 3. Clone this repository

Once Git is up and running you can now clone this repository on your local machine.

```bash
git clone https://github.com/0x10a/docker-starter-kit-symfony
```

## 4. Build with docker

Docker will execute all configurations and create all needed containers.

```bash
$ docker-compose build
```

When it’s done, you can launch your containers !

```bash
$ docker-compose up -d
```

## 5. Symfony 4 installation

Connect to the PHP container as user:dev

```bash
$ docker exec -it -u dev sf4_php bash
```

Once your are inside the PHP container, you can move to the home directory

```bash
$ cd /home/wwwroot/sf4
```

Now we can install Symfony 4

```bash
$ composer create-project symfony/skeleton .
```

Now Symfony 4 is up and running @ http://localhost
To access to PhpMyAdmin: http://localhost:8080

# MySQL configuration

```
MYSQL_ROOT_PASSWORD: root
MYSQL_DATABASE: sf4
MYSQL_USER: sf4
MYSQL_PASSWORD: sf4
```

# Contributing
For contributing, feel free to create a Pull Request on GitHub, please write a description which gives the context and/or explains why you are creating it.
