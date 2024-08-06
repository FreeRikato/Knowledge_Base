The video starts with how essential are containers and containerization in CI/CD (Github actions). First, The concepts of virtualization is important to understand:

- A host machine that could be local with static IP, in cloud or datacenter with its own CPU, RAM and Hard drive (I/O)
- A part of the host machine with CPU, RAM and Hard drive is used to create a new machine (virtualize a new machine) with a full OS for itself
- Hypervisors are responsible for the life cycles of these virtual machines. It is a software used to run multiple virtual machine on a single physical machine.

![[../Files/Pasted image 20240805220840.png]]


Now that we have understood virtualization, let's move on to understanding containers and containerization.

If there are processes running on the host machine and we want to isolate particular processes that cannot mess up with others, this can be done using containers. The processes can be containerized with chroot and rlimit. Docker is a program that manages the lifecycle of containers: Add, run & interact with them.

so basically containers are lightweight environments to isolate and run specific process in the host machine.

Things to understand still
1. Dockerfile
2. docker build
3. Docker image
4. docker run
5. Docker container