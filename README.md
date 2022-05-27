# What is Docker?

### **What is Container?**

- A way to package application with all the necessary dependencies and configuration.
- Portable artifact, easily shared and moved around
- Makes development and deployment process more efficient.

### **Where do containers live?**

- Container Repository
- Private Repositories
- Public repository for docker ( Docker Hub)

### **How Containers developed the process of Application Development?**

- Before Containers:
    - Installation process different on each OS environment.
    - Many steps where something could go wrong
    - Development team gives the artifact to Operations team to configure on each operating system.
    - Dependency version conflicts
    - Misunderstandings from textual guide of deployment.
- After Containers:
    - own isolated environment
    - packaged with all needed configuration
    - one command to install the app regardless of the OS.
    - Developers and Operations work together to package the application in a container
    - No environmental configuration needed on server except Docker Runtime

### **Technically What is Container?**

- Layers of images
- Mostly Linux base Image, because small in size
- Application image on top

### How to **Pull Image from Docker Hub?**

- Open Docker Hub and copy the image name
- Use the command below for example

```powershell
docker run postgres:9.6
```

- separate layers are downloaded one by one.
- Advantage is that if we have to upgrade the version, the layers that got changed gets downloaded and others remain as it is. As a result image pull is faster.
- docker run command not only downloads the image but also starts the image

```powershell
docker ps
```

using the ps commad we can see all the running containers.

### What is **Difference between docker image and Docker container?**

Docker Image:

- Image is actual package.
- It is the application with its dependencies and artifacts that can be moved around

Docker Container:

- Pull the actual image and start the application.
- It is the container environment created where the image runs.

### Docker Vs Virtual Machine

- Both are virtualization tools.
