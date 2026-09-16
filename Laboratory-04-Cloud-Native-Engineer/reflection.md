# Mission 4 Reflection

Deploying a container with Docker is dramatically faster than setting up a Virtual Machine. Installing an OS on a VM involves booting a hypervisor, allocating virtual hardware, and waiting minutes for the guest operating system to initialize before any application can even be installed. In contrast, running `docker run` on an already-pulled image takes seconds, because the container shares the host's kernel and only needs to start a single isolated process rather than an entire OS.

Port mapping (`-p 8080:80`) is necessary because a container's internal network is isolated from the host by default. Nginx listens on port 80 *inside* the container, but that port is not automatically reachable from outside. Mapping host port 8080 to container port 80 creates a bridge so that requests sent to `localhost:8080` on the host are forwarded into the container, letting us actually reach the web server.

When you run `docker rm`, any data that was stored inside the container's writable layer is permanently deleted, since that layer is destroyed along with the container. This is why containers are considered ephemeral — for real persistent data, you need to use Docker volumes or bind mounts, which live outside the container's lifecycle.

Containerization changes the relationship between developers and IT operations by removing the "it works on my machine" problem. Because the container packages the application with all its dependencies, developers can hand operations teams a single artifact that behaves identically in development, testing, and production. This shrinks the gap between writing code and deploying it, and is a major reason Docker became foundational to modern DevOps practices — it lets both teams work from the same reproducible unit.

My GitHub portfolio is steadily evolving into a demonstration of practical cloud skills rather than just theory. Each lab adds a new capability — from basic cloud concepts to infrastructure blueprints, multi-cloud comparisons, and now container orchestration — building a body of work that shows growth from a beginner to someone comfortable operating in cloud-native environments.
