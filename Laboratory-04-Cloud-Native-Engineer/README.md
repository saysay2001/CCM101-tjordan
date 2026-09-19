# Laboratory 04 - Cloud-Native Engineer

## Mission Overview

This laboratory introduces the fundamentals of containerization using Docker. The mission focused on understanding the differences between Virtual Machines and containers, verifying a Docker environment, deploying an Nginx web server, and managing the container lifecycle. Through these activities, I experienced how containers can provide a faster and more lightweight approach to deploying web applications.

## Objectives

The objectives of this laboratory are to:

* Understand the differences between Virtual Machines and containers.
* Verify that Docker is installed and running.
* Pull and run an official Nginx Docker image.
* Use port mapping to access a web server running inside a container.
* Verify a running web server using an HTTP request.
* Manage the basic lifecycle of a Docker container.
* Document Docker commands and their functions.
* Develop practical skills in cloud-native technologies and containerization.

## Docker Commands Executed

### Checkpoint 3 - Verify Docker Environment

```bash
docker --version
docker info
docker ps
```

### Checkpoint 4 - Deploy Nginx Container

```bash
docker pull nginx
docker run -d -p 8080:80 --name nginx-server nginx
docker ps
curl http://localhost:8080
```

### Checkpoint 5 - Container Lifecycle

```bash
docker ps
docker stop nginx-server
docker ps
docker ps -a
docker rm nginx-server
docker ps -a
```

## Skills Learned

Through this laboratory, I learned how to work with Docker from the command line and gained a basic understanding of containerized application deployment. I learned how to download Docker images, create and run containers, map network ports, and verify whether a web application is working. I also learned how to stop, inspect, and remove containers using Docker commands. Additionally, I improved my understanding of the differences between traditional Virtual Machines and lightweight containers.

## Challenges Encountered

One challenge was becoming familiar with Docker commands and understanding the difference between a Docker image and a running container. Another challenge was understanding how port mapping works when accessing a service inside a container. I also had to carefully follow the container lifecycle because the Nginx container needed to remain running while testing it with `curl`, before it could be stopped and removed. Taking screenshots and organizing them in the correct `screenshots` folder also required careful attention to the laboratory requirements.
