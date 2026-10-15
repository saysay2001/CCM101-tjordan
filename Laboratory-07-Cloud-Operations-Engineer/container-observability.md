# Container Observability Report

## 1. Failed HTTP Request Log

Paste the exact log line showing the HTTP 404 error here.

## 2. Why Application Logs Are Important

Application logs help cloud engineers identify errors, trace failed requests, and understand what happened when an application encounters a problem. They make troubleshooting faster by providing evidence about the source and timing of errors, helping engineers resolve issues and maintain reliable services.

## 3. Screenshot

- `screenshots/docker-logs.png`
## 4. Real-Time Container Metrics

- **Container Name:** clientwebsite
- **Container ID:** 77bea08ce699
- **CPU Usage:** 0.00%
- **Memory Usage:** 2.723MiB
- **Memory Limit:** 1.859GiB
- **Memory Usage Percentage:** 0.14%
- **Network I/O:** 3.75kB received / 5.21kB sent
- **Block I/O:** 0B read / 12.3kB written
- **Processes (PIDs):** 2

### Observation

The Docker stats output shows that the clientwebsite container was using 0.00% CPU and only 2.723MiB of memory, equivalent to 0.14% of its memory limit. These results indicate that the Nginx container was consuming minimal resources at the time of monitoring.

### Screenshot

- `screenshots/container-metrics.png`
