# Mission Reflection

In this mission I deployed MinIO, an S3-compatible object storage server, inside a Docker container, then used its web console to create a bucket and upload a file.

**Why is object storage better suited for millions of photos than a traditional block storage hard drive?** Object storage keeps each photo as an independent object with its own metadata and unique key in a flat structure. It scales out by adding capacity, is reachable over HTTP from anywhere, and costs less per gigabyte. A block storage drive is tied to one server, has a fixed size, and is harder to scale and share.

**How did Docker make it easier to deploy MinIO?** I did not have to install dependencies or configure anything by hand. One `docker run` command downloaded the image, started the server, mapped ports 9000 and 9001, and set the login credentials with environment variables. The same command would work on any machine running Docker.

**What is a "bucket"?** A bucket is a top-level container that holds objects in cloud storage. It is like a root folder, but it has its own unique name, access policies, and settings. I created a bucket named `client-photos` for the client's images.

**How do enterprises keep object storage data safe if a physical server crashes?** I think they use replication and redundancy. Data is copied across multiple disks, servers, and even data centers or regions, and techniques like erasure coding can rebuild lost pieces. If one server fails, other copies keep the data available.

**How is my confidence with the Linux command line growing?** Running Docker commands and checking containers with `docker ps` feels less intimidating now. I still need practice, but I can see how terminal commands connect to real cloud services I can open in a browser.
