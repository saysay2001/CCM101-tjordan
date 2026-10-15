# Laboratory 07 – Cloud Operations Engineer

## 1. Mission Overview

This laboratory focuses on the responsibilities of a Cloud Operations Engineer in monitoring server health, deploying a web server container, generating web traffic, analyzing application logs, and monitoring container resource consumption. The activities demonstrate how basic monitoring and observability help maintain application performance and reliability.

## 2. Objectives

- Establish a baseline of the host server's RAM and disk storage.
- Deploy an Nginx web server using Docker.
- Simulate successful HTTP requests and generate a 404 Not Found error.
- Retrieve and analyze application logs to identify successful and failed requests.
- Monitor the container's CPU usage, memory consumption, and network activity using Docker stats.
- Document the commands, observations, and results of the laboratory activities.

## 3. Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Checks RAM usage and availability. |
| `df -h /` | Checks the root filesystem's total and available disk space. |
| `top` | Monitors CPU utilization, system load, and running processes. |
| `docker run -d --name clientwebsite -p 8080:80 nginx` | Deploys an Nginx container in the background and maps port 8080 to port 80. |
| `docker ps` | Lists running containers. |
| `curl http://localhost:8080` | Simulates a successful visit to the website. |
| `curl http://localhost:8080/hidden-admin-page` | Simulates a request to a nonexistent page, producing a 404 response. |
| `docker logs clientwebsite` | Retrieves the container's logs for troubleshooting. |
| `docker stats` | Monitors live container resource consumption. |

## 4. Skills Learned

- **System Monitoring:** Learned how to check RAM, disk storage, CPU usage, and running processes in Ubuntu.
- **Container Deployment:** Learned how to run an Nginx web server using Docker and map network ports.
- **Traffic Simulation:** Practiced sending HTTP requests with curl and identifying successful and failed responses.
- **Application Logging:** Learned how to retrieve and interpret container logs to investigate HTTP errors.
- **Resource Monitoring:** Used Docker stats to monitor CPU, memory, network I/O, and process counts.
- **Technical Documentation:** Practiced recording monitoring results, saving screenshots, and documenting technical procedures in Markdown.

## 5. Monitoring Results

The host system baseline showed 1.9 GiB of total RAM and 19 GB of root filesystem storage, with approximately 13 GB of disk space available.

The Nginx container, named `clientwebsite`, was successfully monitored using Docker stats. At the time of measurement, it used 0.00% CPU and 2.723 MiB of memory, representing 0.14% of its 1.859 GiB memory limit.

The website was tested with three successful HTTP requests and one request to a nonexistent page, which was expected to return HTTP 404.

## 6. Screenshots

The following screenshots document the laboratory activities:

- `screenshots/memory-check.png`
- `screenshots/disk-check.png`
- `screenshots/install-nginx.png`
- `screenshots/simulation1.png`
- `screenshots/simulation2.png`
- `screenshots/docker-logs.png`
- `screenshots/container-metrics.png`
