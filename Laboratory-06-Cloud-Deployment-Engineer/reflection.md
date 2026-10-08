# Mission Reflection

Writing a docker-compose.yml file makes a cloud engineer's job much easier because everything is defined in one place. Instead of typing several long commands for each container and hoping nothing is misspelled, I wrote the setup once and deployed it with a single command. The file can also be reused, shared, and tracked in GitHub, which makes deployments consistent and repeatable.

YAML depends on spaces for its structure, so an indentation error, such as using a Tab instead of spaces, breaks the file. Docker Compose cannot read it and shows an error instead of starting the containers. I experienced this myself when my first file was pasted with broken indentation and Compose reported that a service must be a mapping, not a string. Fixing the spacing solved the problem.

Environment variables were used so that configuration such as database names, users, and passwords is kept outside the container images. Both the database and Nextcloud need matching credentials, and variables let us set them in one clear place. However, hardcoding passwords in a file is not safe for production, where secrets should be stored more securely.

Deploying a working enterprise cloud storage system in just a few minutes felt surprising and exciting. Two containers were pulled, connected, and running after one command, something that would normally take much longer to install and configure manually. It made me realize how powerful automation is.

Since Mission 1, my understanding of cloud computing has grown from basic definitions to hands-on skills. At first I saw the cloud as just online storage and services. Now I understand that it involves containers, infrastructure as code, and architectures that engineers build and manage using code. I feel more confident and want to keep learning.

