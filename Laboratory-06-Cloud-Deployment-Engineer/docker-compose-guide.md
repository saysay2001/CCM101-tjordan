# Docker Compose Guide – Nextcloud Deployment

## 1. Introduction

Docker Compose is a tool used to configure and manage multiple Docker containers through a YAML file. In this mission, I used Docker Compose to deploy Nextcloud and its database as a private cloud environment.

The `docker-compose.yml` file contains the configuration needed to start and connect the application services.

## 2. What Does the `services:` Block Do?

The `services:` block defines the containers that Docker Compose will create and manage. In my Nextcloud deployment, it defines the Nextcloud application and the database service.

Each service has its own configuration, such as the Docker image, environment variables, ports, and storage settings.

The Nextcloud service provides the web interface where users can access and manage files. The database service stores the information required by the application.

Using the `services:` block allows Docker Compose to manage these related containers together instead of requiring separate commands for each container.

## 3. How Does Nextcloud Find the Database Container?

Nextcloud uses the `MYSQL_HOST` environment variable to identify the database server.

For example:

```yaml
environment:
  MYSQL_HOST: db
```

In this example, `db` is the name of the database service defined in the `docker-compose.yml` file.

Docker Compose creates a network for the services, allowing containers to communicate using their service names. Therefore, Nextcloud can use `db` as the database hostname instead of needing to know the database container's IP address.

The value of `MYSQL_HOST` must match the database service name in the YAML configuration. This allows Nextcloud to locate the database and communicate with it.

## 4. Difference Between `docker run` and `docker-compose up -d`

### Docker Run

The `docker run` command creates and starts an individual container using a specified image and configuration options.

Example:

```bash
docker run -d -p 8080:80 --name nextcloud nextcloud
```

This command starts a Nextcloud container in the background and maps port 8080 on the host to port 80 inside the container. Any required database would need to be configured separately unless it was already available.

### Docker Compose Up -d

The `docker-compose up -d` command starts the services defined in the `docker-compose.yml` file in the background.

It can create and manage multiple related containers, configure their networking, and apply their environment variables and other settings from one configuration file.

### Main Difference

The main difference is that `docker run` is commonly used to start an individual container, while `docker-compose up -d` manages an application composed of multiple services.

For example, Docker Compose can start both Nextcloud and its database using one command. The `-d` option runs the containers in detached mode, allowing the terminal to be used for other tasks.

## 5. Conclusion

This mission helped me understand how Docker Compose simplifies the deployment of a private cloud application. The `services:` block defines the containers, the `MYSQL_HOST` environment variable allows Nextcloud to locate its database, and the `docker-compose up -d` command starts the connected services together. These features make multi-container applications easier to configure, deploy, and manage.
