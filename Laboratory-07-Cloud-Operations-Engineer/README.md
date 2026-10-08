# Laboratory 7: The Cloud Operations Engineer

## Mission Overview

In this mission, I acted as a Cloud Operations (SRE) Engineer at CloudNova Technologies. I established a performance baseline for a Linux host, deployed an Nginx web server in a container, generated test traffic, and used logs and real-time metrics to verify that the application is healthy and ready for a surge in users.

## Objectives

- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container and track its real-time performance using Docker metrics.
- Generate web traffic and extract application access logs for analysis.
- Translate raw performance data into a readable technical report using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio.

## Monitoring Commands Executed

```bash
free -h                                                  # check memory usage
df -h                                                    # check disk storage
top                                                      # view processes and CPU load
docker run -d --name client-website -p 8080:80 nginx     # deploy Nginx
curl http://localhost:8080                               # simulate a user (x3)
curl http://localhost:8080/hidden-admin-page             # trigger a 404 error
docker logs client-website                               # view application logs
docker stats                                             # view live container metrics
```

## Skills Learned

- Establishing a host performance baseline with free, df, and top
- Deploying a containerized web server
- Simulating web traffic and HTTP errors with curl
- Reading application access logs to find specific status codes
- Monitoring container CPU and memory with docker stats
- Documenting system health in Markdown
