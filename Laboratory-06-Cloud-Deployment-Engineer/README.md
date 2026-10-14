# Laboratory 06: The Cloud Deployment Engineer

## Mission Overview

This laboratory demonstrates how to deploy a private cloud environment using Docker Compose and Nextcloud. The deployment uses separate containers for the Nextcloud web application and its database. These services communicate through Docker Compose networking, allowing the application to access its database.

The mission also demonstrates how to access the Nextcloud installation page through a browser and how to shut down the deployment safely.

## Objectives

- Understand the purpose of Docker Compose.
- Create and configure a `docker-compose.yml` file.
- Deploy Nextcloud and its database as connected services.
- Understand environment variables and container networking.
- Access the Nextcloud installation page through port 8080.
- Stop and remove the deployed containers using Docker Compose.
- Document the deployment configuration and commands.

## Commands Executed

### 1. Create the Project Directory

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
```

### 2. Create the Docker Compose Configuration

```bash
nano docker-compose.yml
```

This command creates or opens the YAML configuration file used to define the application services.

### 3. Start the Deployment

```bash
docker-compose up -d
```

This command creates and starts the configured services in the background.

### 4. Check Container Status

```bash
docker-compose ps
```

This command displays the status of the services managed by Docker Compose.

### 5. Access the Nextcloud Web Interface

Open port `8080` using the KillerCoda Playground's Traffic / Ports or Custom Ports feature.

The Nextcloud installation page should appear in the browser.

### 6. Stop and Remove the Deployment

```bash
docker-compose down
```

Run this command from the directory containing the `docker-compose.yml` file. It stops and removes the Compose-managed containers and network.

## Documentation

See [`docker-compose-guide.md`](docker-compose-guide.md) for an explanation of the services block, database connectivity, and the difference between `docker run` and `docker-compose up -d`.

## Screenshots and Evidence

- `nextcloudweb.png` — Screenshot of the Nextcloud installation page.
- `composeteardown.png` — Screenshot showing the completed container shutdown and removal.

## Conclusion

This mission provided practical experience in deploying a private cloud application using Docker Compose. It demonstrated how related containers communicate, how the deployment can be accessed through a web browser, and how infrastructure can be managed using configuration files and terminal commands.
