# Docker Deployment Log — Checkpoint 5: Container Lifecycle

## Commands Executed

### 1. List running containers
```bash
docker ps
```
**Output:**
```
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS                                     NAMES
c3c9d57d08cd   nginx     "/docker-entrypoint.…"   8 minutes ago   Up 8 minutes   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   my-nginx
```
**Explanation:** Lists all currently running containers — confirms `my-nginx` was up and had been running for 8 minutes with port 8080 mapped to container port 80.

### 2. Stop the running container
```bash
docker stop my-nginx
```
**Output:**
```
my-nginx
```
**Explanation:** Gracefully stops the `my-nginx` container; Docker prints the container name to confirm it was stopped.

### 3. Verify it is stopped
```bash
docker ps -a
```
**Output:**
```
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS                              PORTS     NAMES
c3c9d57d08cd   nginx     "/docker-entrypoint.…"   8 minutes ago   Exited (0) Less than a second ago             my-nginx
```
**Explanation:** Lists all containers, including stopped ones — confirms `my-nginx` has a status of `Exited (0)`, meaning it stopped cleanly, and its port mapping is no longer active.

### 4. Remove the container completely
```bash
docker rm my-nginx
```
**Output:**
```
my-nginx
```
**Explanation:** Permanently deletes the stopped `my-nginx` container from the host; Docker confirms removal by printing the container name.
