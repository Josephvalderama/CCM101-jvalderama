# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture splits an application into two separate layers: an application (web) tier that users interact with, and a database tier that stores the data. The two tiers communicate over a network, but each one has its own job and runs independently. In this laboratory, the application tier is the Nextcloud container and the database tier is the MariaDB container, linked together using Docker Compose.

## The Web/Application Tier

The web/application tier is the part of the system that users directly interact with. Its role is to:

- Serve the user interface (the Nextcloud web pages) to the browser
- Receive and handle HTTP requests from users
- Run the application logic, such as logging in, uploading files, and sharing folders
- Send queries to the database tier whenever it needs to save or retrieve data

In this deployment, the Nextcloud container fills this role and is exposed to users through port 8080.

## The Database Tier

The database tier is responsible for storing and managing the application's persistent data. Its role is to:

- Store user accounts and login credentials
- Keep file metadata, such as file names, folders, and sharing permissions
- Store application settings and configuration
- Return the requested data to the application tier when queried

In this deployment, the MariaDB container fills this role. It is not exposed to users directly. Only the Nextcloud container communicates with it.

## Why Separate Them?

Separating the web server and the database into two containers makes the system easier to manage, scale, and secure. Each tier can be updated, restarted, or scaled independently, so a problem in one container does not necessarily bring down the other. It also improves security, since the database is not exposed to the outside world and can be backed up and protected on its own. Finally, it follows the container best practice of one service per container, which keeps each one simple, reusable, and easier to
