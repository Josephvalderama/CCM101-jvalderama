# Docker Compose Guide

This guide explains the `docker-compose.yml` file used to deploy a Nextcloud and MariaDB stack.

## The Compose File

```yaml
version: '3'
services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?

The `services:` block is the top-level section that defines every container in the application stack. Each entry under it (here, `database` and `app`) describes one container, including the image it uses, the ports it exposes, and its environment variables. Docker Compose reads this block to know which containers to create and how to configure them.

## How did the Nextcloud app container know how to find the database container?

Docker Compose automatically places all services in the same network, and each service name becomes a hostname on that network. The `MYSQL_HOST=database` variable tells Nextcloud to connect to a host named `database`, which matches the name of the MariaDB service. Docker resolves that name to the database container's address, so no IP address needs to be configured manually.

## What is the difference between `docker run` and `docker-compose up -d`?

| `docker run` | `docker-compose up -d` |
|---|---|
| Starts a single container per command | Starts all containers defined in the YAML file |
| Options (ports, variables, names) are typed manually each time | Options are saved in a reusable file |
| Networking between containers must be set up manually | Creates a shared network automatically |
| Prone to typing errors and hard to reproduce | Repeatable and can be version-controlled in Git |

`docker-compose up -d` is an example of Infrastructure as Code, because the whole deployment is described in a file instead of typed command by command. The `-d` flag runs the containers in the background (detached mode).
