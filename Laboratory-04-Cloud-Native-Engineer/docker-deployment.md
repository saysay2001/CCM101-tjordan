# The Container Lifecycle

A Cloud-Native Engineer must know how to manage the lifecycle of running containers. The following commands demonstrate how to list, stop, verify, and remove a Docker container.

## 1. List Running Containers

```bash
docker ps
```

This command lists all currently running Docker containers and displays information such as the container ID, image, status, ports, and container name.

## 2. Stop the Running Container

```bash
docker stop nginx-server
```

This command stops the running Nginx container named `nginx-server`.

## 3. Verify the Container Is Stopped

```bash
docker ps
```

This command verifies that the Nginx container is no longer running because stopped containers do not appear in the default `docker ps` output.

To confirm that the stopped container still exists, use:

```bash
docker ps -a
```

This command lists all containers, including stopped containers, and should show `nginx-server` with an `Exited` status.

## 4. Remove the Container Completely

```bash
docker rm nginx-server
```

This command permanently removes the stopped `nginx-server` container from the Docker environment.

To verify that the container has been completely removed:

```bash
docker ps -a
```

The `nginx-server` container should no longer appear in the list.

## Container Lifecycle Summary

The container lifecycle demonstrated in this checkpoint is:

**Running → Stopped → Removed**

These commands demonstrate the basic management of Docker containers, from monitoring a running container to stopping and permanently removing it.

