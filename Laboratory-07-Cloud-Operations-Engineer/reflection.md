# Mission Reflection

Throughout this laboratory activity, I learned that monitoring and troubleshooting are important responsibilities of a Cloud Operations Engineer.

First, checking the host server's resources is important even if containers are running perfectly because containers still depend on the host's CPU, RAM, and disk space. If the server runs out of resources, applications may become slow, crash, or stop working properly. Monitoring the host helps identify potential problems before they affect users.

Second, the `docker logs` command helps troubleshoot login problems by showing the application's recorded activities and errors. By checking the logs, I can look for failed login attempts, application errors, or database connection problems. These details can help identify the possible cause of the issue instead of guessing what went wrong.

Third, monitoring logs and metrics have different purposes. Logs provide detailed records of events, such as successful HTTP requests and 404 errors. Metrics show numerical measurements of system performance, such as CPU usage, memory consumption, and network activity. Both are important because logs help explain what happened, while metrics help determine how well the application and server are performing.

Fourth, large enterprise companies can monitor thousands of containers using centralized monitoring tools such as Prometheus and Grafana. Prometheus collects and stores metrics from different systems, while Grafana presents the information through dashboards and visualizations. These tools help engineers monitor many containers, identify unusual resource usage, and detect problems more efficiently.

Lastly, this laboratory improved my ability to troubleshoot Linux environments by teaching me how to use commands such as `free -h`, `df -h /`, `top`, `docker logs`, and `docker stats`. I also learned how to deploy an Nginx container and simulate HTTP requests using `curl`. Through these activities, I became more confident in examining system resources, identifying errors, and understanding container performance.

Overall, this experience helped me understand that effective monitoring is not only about checking whether an application is running but also about ensuring that it remains reliable, efficient, and ready to serve users.
