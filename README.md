# docker_tutorial

## Terminology

- Images: The blueprints of our application which form the basis of containers. 
An image can be downloaded with the docker pull command.
(e.g., $ docker pull busybox)
    - Base images: images that have no parent image, usually OS like images, 
    such as ubuntu, busybox or debian.
    - Child images: images that build on base images and add additional 
    functionality.

    - Official images: images that are officially maintained and supported by 
    the folks at Docker. These are typically one word long. 
    In the list of images above, the python, ubuntu, busybox 
    and hello-world images are official images.
    - User images: images created and shared by users like you. 
    They build on base images and add additional functionality. 
    Typically, these are formatted as user/image-name.

- Containers: Created from Docker images and run the actual application.
We create a container using docker run. (e.g., $ docker run busybox)
A list of running containers can be seen using the docker ps command.
(e.g., $ docker ps)

- Docker Engine: Docker Engine is a client-server application with the following 
components:
    - A server which is a type of long-running program called a daemon process.
        ($ dockerd ...)
    - A REST API which specifies interfaces that programs can use to talk to
        the daemon and instruct it what to do.
    - A command line interface (CLI) client
        ($ docker ...)
![alt text](https://docs.docker.com/engine/images/engine-components-flow.png "Docker Engine")
The CLI uses the Docker REST API to control or interact with the Docker daemon 
through scripting or direct CLI commands. Many other Docker applications use the 
underlying API and CLI.
The Docker daemon creates and manages Docker objects, such as images, 
containers, networks, and volumes.

- Docker Host: a physical system or virtual machine running Linux. 
This can be your laptop, server or virtual machine in your data center, 
or computing resource provided by a cloud provider.

- Docker Daemon: The background service running on the host that manages
building, running and distributing Docker containers.
The daemon is the process that runs in the operating system
which clients talk to.

- Docker Client: The command line tool that allows the user to interact with 
the daemon. More generally, there can be other forms of clients too, such as 
Kitematic which provide a GUI to the users.

- Docker Hub: A registry of Docker images. You can think of the registry 
as a directory of all available Docker images. If required, one can host 
their own Docker registries and can use them for pulling images.
