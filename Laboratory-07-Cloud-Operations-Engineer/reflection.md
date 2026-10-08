# Mission Reflection

Checking the host server's resources is important even when containers look healthy because every container shares the same physical machine. If the host runs out of RAM, disk space, or CPU, the containers on it will slow down or crash no matter how well they are configured. A full disk, for example, can stop logs from being written and make applications fail without warning.

If a user cannot log into a web application, the docker logs command would be my first step. It shows the requests the application received and the status codes it returned, so I can look for errors such as 401, 403, or 500 around the time of the complaint. This points me to the cause much faster than guessing.

Logs and metrics answer different questions. Logs, like the ones in Checkpoint 4, are a record of events: who requested what and what happened, including my deliberate 404 error. Metrics, like docker stats in Checkpoint 5, are numbers that describe performance, such as CPU percentage, memory usage, and network I/O. Logs tell me what happened, while metrics tell me how healthy the system is.

Large enterprise companies cannot watch thousands of containers by hand. They use monitoring tools such as Prometheus, which collects metrics from every container automatically, and Grafana, which turns that data into dashboards and sends alerts when something goes wrong.

My troubleshooting ability has improved a lot during this mission. Before, I would not have known where to begin when something broke. Now I know to check the host with free, df, and top, then inspect the container with logs and stats, and use the evidence to find the cause instead of guessing.
