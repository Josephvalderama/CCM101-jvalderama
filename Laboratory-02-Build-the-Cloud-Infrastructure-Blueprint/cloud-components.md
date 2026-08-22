# Cloud Infrastructure Components

## Compute Resources
*Purpose:* Compute resources supply the processing capability required to run software, perform calculations, and keep the operating system functioning. These typically come in the form of virtual machines, containers, or serverless functions.

*Why it matters in cloud computing:* Compute forms the backbone of every cloud workload — without it, applications simply can't run. Cloud platforms allow businesses to scale their processing power up (adding CPU/RAM) or out (adding more VMs) as needed, eliminating the need to buy physical servers.

*Relation to KillerCoda:* The KillerCoda environment is itself a virtual machine — an on-demand compute resource that gives me access to a complete Linux system without requiring any physical hardware of my own.

## Storage Resources
*Purpose:* Storage resources hold the operating system, application data, and files. In the cloud, this is typically split into object, block, and file storage types.

*Why it matters in cloud computing:* Cloud storage must be dependable, expandable, and accessible from any location. It overcomes the constraints of physical drives by spreading data across multiple systems to ensure durability.

*Relation to KillerCoda:* The disk space displayed through `df -h` in my environment represents a block storage volume connected to the virtual machine, functioning much like the root volume of a cloud VM on platforms such as AWS, Azure, or GCP.

## Networking Resources
*Purpose:* Networking resources enable communication among virtual machines, storage, cloud services, and users — encompassing virtual networks, routers, firewalls, and load balancers.

*Why it matters in cloud computing:* Networking is what links otherwise separate compute and storage components so they can interact and be accessed by users. Well-designed networks also help guard systems from unauthorized access.

*Relation to KillerCoda:* My environment is assigned its own hostname and IP address (retrieved via `hostname` and `hostname -I`), illustrating how it's connected within KillerCoda's cloud infrastructure so I can reach it remotely through a browser.

## Operating System
*Purpose:* The operating system controls hardware resources, executes applications, and provides the interface — in this case, a Linux terminal — through which I operate the machine.

*Why it matters in cloud computing:* Most cloud servers run on Linux because it's lightweight, dependable, and broadly supported. The OS is where cloud engineers handle configuration, security, and overall system management.

*Relation to KillerCoda:* My environment runs Ubuntu 24.04.4 LTS, verified through `cat /etc/os-release` — the same kind of Linux distribution frequently used on real cloud virtual machines in AWS EC2, Azure VMs, or Google Compute Engine.
