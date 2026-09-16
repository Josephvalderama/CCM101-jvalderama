# Laboratory 04: Cloud-Native Engineer

## Mission Overview
This lab covers the transition from traditional Virtual Machines to containerized applications using Docker. It includes researching VM vs. container architecture, deploying a live Nginx container, and managing its lifecycle.

## Objectives
- Differentiate between VMs and Containers
- Access a Docker-enabled environment using KillerCoda
- Execute fundamental Docker CLI commands
- Pull, run, manage, and terminate a containerized application (Nginx)
- Document container operations in Markdown

## Docker Commands Executed
```bash
docker --version
docker info
docker pull nginx
docker run -d -p 8080:80 --name my-nginx nginx
curl http://localhost:8080
docker ps
docker stop my-nginx
docker ps -a
docker rm my-nginx
```

## Skills Learned
- Verifying a Docker environment's installation and status
- Pulling images from Docker Hub
- Running containers in detached mode with port mapping
- Managing the full container lifecycle (list, stop, verify, remove)


## Challenges Encountered
While verifying the Nginx container, clicking the `curl http://localhost:8080` command link in the KillerCoda lesson instructions opened a new tab in my own local browser instead of running in the terminal. This caused a "site can't be reached / ERR_CONNECTION_REFUSED" error, since `localhost` on my own machine has nothing running on port 8080 — the container was actually running on KillerCoda's remote VM. I resolved this by typing the `curl http://localhost:8080` command directly into the KillerCoda terminal instead of clicking the link, which correctly returned the "Welcome to nginx!" HTML output. This taught me that `localhost` always refers to whichever machine the command is executed on, not the machine displaying the browser.
